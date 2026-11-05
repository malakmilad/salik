# Job State Machine — Salik Assist MVP

| Field | Value |
|-------|-------|
| **Version** | 1.0 |
| **Status** | Draft |
| **Author** | Engineering |
| **Last Updated** | November 5, 2026 |

## Purpose

Define the canonical job lifecycle states and legal transitions for MVP. All apps, APIs, and ops tools must use these states (Rule 35).

## Related Documents

- [PRD](../11-Product-Requirements/PRD.md)
- [SRS](./SRS.md)
- [Operations Workflow](../06-Operations/Operations-Workflow.md)
- [Business Rules](../04-Business/Business-Rules.md)

---

## States

| Code | State | Terminal? | Description |
|------|-------|-----------|-------------|
| `REQUESTED` | Requested | No | Valid request entered matching queue |
| `MATCHING` | Matching | No | Providers invited; awaiting offers |
| `OFFERS_READY` | Offers presented | No | ≥1 offer visible to customer |
| `ACCEPTED` | Offer accepted | No | Customer selected offer; awaiting provider ack |
| `EN_ROUTE` | Provider en route | No | Provider moving to customer |
| `ARRIVED` | Provider arrived | No | Within 200 m; customer notified |
| `IN_PROGRESS` | Service in progress | No | Work started |
| `COMPLETION_REQUESTED` | Completion requested | No | Provider asked customer to confirm |
| `COMPLETED` | Service completed | No | Confirmed complete; payment pending/processing |
| `PAID` | Payment processed | No | Customer charged successfully |
| `RATED` | Rated | Yes | Customer submitted rating or rating window closed |
| `CANCELLED` | Cancelled | Yes | Cancelled by customer, provider, or platform |
| `EXPIRED` | Expired | Yes | Offer window ended with no accept |
| `DISPUTED` | Disputed | No | Dispute open; may hold payout |

`RATED`, `CANCELLED`, and `EXPIRED` are terminal. `DISPUTED` may return to `PAID` / `RATED` after resolution.

---

## Transitions

```text
REQUESTED → MATCHING
MATCHING → OFFERS_READY | EXPIRED | CANCELLED
OFFERS_READY → ACCEPTED | EXPIRED | CANCELLED | MATCHING (expand/retry)
ACCEPTED → EN_ROUTE | CANCELLED
EN_ROUTE → ARRIVED | CANCELLED
ARRIVED → IN_PROGRESS | CANCELLED
IN_PROGRESS → COMPLETION_REQUESTED | CANCELLED (platform/exception only)
COMPLETION_REQUESTED → COMPLETED | IN_PROGRESS (customer rejects)
COMPLETED → PAID | DISPUTED
PAID → RATED | DISPUTED
DISPUTED → PAID | RATED | CANCELLED (rare void)
```

---

## Transition Rules

| From → To | Actor | Guards |
|-----------|-------|--------|
| REQUESTED → MATCHING | System | Geo OK, category OK, auth OK |
| MATCHING → OFFERS_READY | System | ≥1 valid offer |
| MATCHING → EXPIRED | System | 5–8 min window rules exhausted + no accept path |
| OFFERS_READY → ACCEPTED | Customer | Valid payment method; offer still live |
| ACCEPTED → EN_ROUTE | Provider | Ack within 60s; else reassign/cancel path |
| EN_ROUTE → ARRIVED | Provider | Distance ≤200 m |
| ARRIVED → IN_PROGRESS | Provider | Explicit start |
| IN_PROGRESS → COMPLETION_REQUESTED | Provider | Photos if tow / &gt;AED 500 |
| COMPLETION_REQUESTED → COMPLETED | Customer or System | Customer confirm OR 15 min no objection |
| COMPLETED → PAID | System | Charge success; price rules OK |
| * → CANCELLED | Customer/Provider/Ops | Fee schedule by stage |
| COMPLETED/PAID → DISPUTED | Customer/Provider | Within dispute window |

---

## Timers

| Timer | Duration | Action |
|-------|----------|--------|
| Provider offer response | 90s | Auto-decline invite |
| Offer window | 5 min (extend to 8 if 1 offer) | Expand radius / escalate / expire |
| Zero-offer expand | 3 min | Expand + backup pool |
| Zero-offer escalate | 5 min | Ops manual dispatch queue |
| Provider assignment ack | 60s | Ops alert / re-match |
| Free cancel grace | 3 min after accept | Fee = 0 |
| Completion auto-confirm | 15 min | Auto COMPLETED |
| Stuck job | 24 h non-terminal | Ops escalation |
| Rating window | 7 days | Auto-close → RATED without stars |

---

## Event Log (Audit)

Every transition must persist:

- `job_id`, `from_state`, `to_state`, `actor_type`, `actor_id`
- `timestamp` (UTC)
- Optional: `geo`, `reason_code`, `metadata` (fee, price delta, photo refs)

Immutable append-only log satisfies BR-M03 and Rule 35.

---

## Cancellation Stage Mapping

| Policy stage | States |
|--------------|--------|
| S0 Request open | REQUESTED, MATCHING, OFFERS_READY |
| S1 Offer accepted | ACCEPTED |
| S2 En route | EN_ROUTE |
| S3 Arrived | ARRIVED |
| S4 In progress | IN_PROGRESS, COMPLETION_REQUESTED |
