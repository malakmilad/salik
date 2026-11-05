# Service Level Agreement (SLA) — Salik Assist

| Field | Value |
|-------|-------|
| **Version** | 1.0 |
| **Status** | Draft |
| **Author** | Product & Strategy Team |
| **Last Updated** | July 4, 2026 |

## Purpose

Define explicit, measurable service level commitments Salik Assist makes to customers, providers, and B2B partners—including response times, availability targets, resolution standards, and remedies when SLAs are breached.

## Scope

Covers marketplace SLAs for B2C consumer jobs and B2B partner contracts in UAE launch geography. Provider-facing SLAs (what providers must meet) are included. Excludes internal IT system uptime SLAs.

## Related Documents

- [Operations Workflow](./Operations-Workflow.md)
- [Escalation Policy](./Escalation-Policy.md)
- [Cancellation Policy](./Cancellation-Policy.md)
- [Refund Policy](./Refund-Policy.md)
- [Provider Performance](./Provider-Performance.md)
- [Customer Support](./Customer-Support.md)

## Table of Contents

1. [SLA Overview](#sla-overview)
2. [Customer-Facing SLAs (B2C)](#customer-facing-slas-b2c)
3. [Provider-Facing SLAs](#provider-facing-slas)
4. [B2B Partner SLAs](#b2b-partner-slas)
5. [Support SLAs](#support-slas)
6. [SLA Measurement & Reporting](#sla-measurement--reporting)
7. [SLA Breach Remedies](#sla-breach-remedies)
8. [Force Majeure & Exclusions](#force-majeure--exclusions)
9. [SLA Improvement Targets](#sla-improvement-targets)
10. [Business Examples](#business-examples)
11. [Business Decisions](#business-decisions)
12. [Risks](#risks)
13. [Assumptions](#assumptions)
14. [Open Questions](#open-questions)
15. [Next Steps](#next-steps)

---

## SLA Overview

Salik Assist SLAs define **commitments** (what we promise), **measurements** (how we track), and **remedies** (what happens when we miss). SLAs differ by audience:

| Audience | Primary SLA Focus |
|----------|-------------------|
| **Customer (B2C)** | Time to offer, provider arrival, support response |
| **Provider** | Offer response time, payout speed, dispute resolution |
| **B2B Partner** | Dispatch time, job completion, reporting, billing accuracy |

**SLA philosophy:** Commit only to what we can measure and control; automate remedies where possible.

---

## Customer-Facing SLAs (B2C)

### SLA-C1: Time to First Offer

| Metric | Commitment | Measurement |
|--------|------------|-------------|
| Time from request submission to first provider offer received | **≤5 minutes** (90th percentile) | Platform timestamp |
| Time to three offers (when supply available) | **≤8 minutes** (90th percentile) | Platform timestamp |
| Zero-offer escalation trigger | **5 minutes** | Auto-escalation per [Escalation Policy](./Escalation-Policy.md) |

**Launch zone caveat:** SLAs apply within defined launch geography (Dubai metro + E11/E311 corridors). Outside zones: best-effort, no SLA commitment.

**Remedy if breached:**
- 5–8 minutes, zero offers: AED 30 service credit if customer cancels
- >8 minutes, zero offers: AED 50 service credit + free cancellation

### SLA-C2: Provider Arrival Time

| Metric | Commitment | Measurement |
|--------|------------|-------------|
| Provider arrival within committed ETA | **±15 minutes** (85% of jobs) | GPS arrival vs. offer ETA |
| Maximum acceptable delay before customer free-cancel | **+25 minutes** past committed ETA | Timestamp |
| Provider must update customer if ETA changes by | **>10 minutes** | Communication log |

**Remedy if breached:**

| Delay Past Committed ETA | Customer Remedy |
|--------------------------|-----------------|
| 15–30 minutes | AED 30 service credit (auto-applied) |
| 30–45 minutes | 25% partial refund (auto-applied) |
| >45 minutes | 50% partial refund OR free cancel + re-dispatch |
| >45 minutes + no provider communication | 100% refund if customer cancels |

### SLA-C3: Job Completion

| Metric | Commitment | Measurement |
|--------|------------|-------------|
| Accepted job completion rate | **≥95%** (platform-wide) | Completed ÷ accepted |
| Provider no-show rate | **<1%** | No-show count ÷ accepted |
| Service quality (4+ star rating) | **≥88%** at launch; **≥92%** Year 1 | Rating distribution |

**Remedy if breached (no-show):** Full refund + AED 50 credit + provider suspension. See [Refund Policy](./Refund-Policy.md).

### SLA-C4: Platform Availability

| Metric | Commitment | Measurement |
|--------|------------|-------------|
| Customer app/request channel availability | **99.5%** monthly | Uptime monitoring |
| Payment processing success rate | **≥98%** | Transaction success log |

**Remedy if breached:** Service credit AED 50 for customers with failed active job due to platform outage (verified).

---

## Provider-Facing SLAs

### SLA-P1: Offer Response Time

| Metric | Commitment | Measurement |
|--------|------------|-------------|
| Response to offer invitation | **≤90 seconds** (median) | Platform timestamp |
| Acceptance acknowledgment after customer selects offer | **≤60 seconds** | Platform timestamp |

**Consequence if breached:** Reduced matching priority; SPS impact if pattern (>30% slow responses in 7 days).

### SLA-P2: Payout Speed

| Tier | Commitment | Measurement |
|------|------------|-------------|
| Standard verified | **T+2 business days** after job completion | Payout initiation date |
| Preferred tier (SPS ≥75) | **T+1 business days** | Payout initiation date |
| Premium verified | **T+1 business days** | Payout initiation date |
| Disputed job hold | Max **7 business days** pending resolution | Dispute open date |

**Remedy if breached:** Provider receives AED 50 compensation per delayed payout (after 2 business days beyond commitment).

### SLA-P3: Dispute Resolution (Provider Side)

| Metric | Commitment | Measurement |
|--------|------------|-------------|
| Provider dispute acknowledgment | **≤24 hours** | Ticket timestamp |
| Provider dispute resolution | **≤5 business days** | Ticket closure |
| Payout hold communication | **Immediate** on hold | Notification sent |

---

## B2B Partner SLAs

### SLA-B1: Dispatch Performance

| Metric | Commitment | Measurement |
|--------|------------|-------------|
| Time to first offer (partner job) | **≤4 minutes** (90th percentile) | Platform timestamp |
| Time to provider en route | **≤8 minutes** from acceptance (90th percentile) | Platform timestamp |
| Job completion rate | **≥97%** | Partner job records |
| Partner-reported SLA compliance | **≥95%** monthly | Partner scorecard |

**Remedy if breached:** SLA credit per partner contract (typically 5–10% of affected job value, capped monthly).

### SLA-B2: Reporting & Billing

| Metric | Commitment | Measurement |
|--------|------------|-------------|
| Monthly invoice delivery | **By 5th business day** of following month | Invoice date |
| Invoice accuracy | **≥99%** (no corrections required) | Correction tickets |
| Partner portal uptime | **99.5%** monthly | Uptime monitoring |
| Dispute response (B2B billing) | **≤4 business hours** | Ticket timestamp |

### SLA-B3: Dedicated Support

| Metric | Commitment | Measurement |
|--------|------------|-------------|
| B2B dispatch issue response | **≤30 minutes** | Ticket timestamp |
| Account manager availability | Business hours + on-call for P1 | Roster compliance |
| Quarterly business review | **Scheduled within 15 days** of quarter end | Meeting held |

---

## Support SLAs

| Channel | Active Job First Response | Post-Job First Response | Resolution |
|---------|---------------------------|-------------------------|------------|
| Phone | **≤30 seconds** | **≤60 seconds** | Per [Customer Support](./Customer-Support.md) |
| Live chat | **≤60 seconds** | **≤3 minutes** | Same interaction (70% FCR target) |
| WhatsApp | **≤3 minutes** | **≤15 minutes** | ≤24 hours |
| Email | Redirect to phone/chat for active | **≤4 business hours** | ≤72 hours |

**Support availability SLA:**
- Peak hours (6 AM – 11 PM GST): **100% channel availability**
- Off-peak (11 PM – 6 AM GST): Phone + chat within **2 minutes** of request

---

## SLA Measurement & Reporting

| Report | Audience | Frequency | Content |
|--------|----------|-----------|---------|
| Real-time SLA dashboard | Ops team | Live | Active breaches, queue depth, ETA misses |
| Daily SLA summary | Ops + Support leadership | Daily | C1–C4 performance vs. target |
| Weekly provider SLA report | Provider success team | Weekly | P1–P3 by provider |
| Monthly B2B SLA scorecard | Partnerships + Partner | Monthly | B1–B3 with credit calculations |
| Monthly executive SLA review | Leadership | Monthly | Trends, breach root causes, remedies cost |

**Measurement rules:**
- SLA clock starts at defined trigger event (request submitted, offer accepted, etc.)
- SLA clock pauses during force majeure (declared by ops manager)
- Percentile calculations use rolling 30-day window
- Jobs excluded from SLA: customer-cancelled before offer, force majeure, out-of-zone

---

## SLA Breach Remedies

### Automated Remedies (No Customer Action Required)

| Breach | Auto-Remedy | Cap |
|--------|-------------|-----|
| ETA 15–30 min late | AED 30 credit | 1 per job |
| ETA 30–45 min late | 25% partial refund | 1 per job |
| Zero offers 5–8 min (cancel) | AED 30 credit | 1 per job |
| Zero offers >8 min (cancel) | AED 50 credit | 1 per job |
| Provider no-show | Full refund + AED 50 credit | 1 per job |

### Manual Remedies (Support Discretion)

| Breach | Manual Remedy | Authority |
|--------|---------------|-----------|
| Repeated SLA misses (same customer, 3 in 30 days) | AED 100 goodwill credit | Supervisor |
| Platform outage affecting active job | AED 50 credit + re-dispatch priority | Tier 1 agent |
| B2B SLA miss | Per contract credit | Account manager |

**Remedy stacking:** Maximum one auto-remedy + one manual goodwill per job. Remedies do not stack across multiple breach types on same job (highest value applies).

---

## Force Majeure & Exclusions

**Force majeure events (SLA suspended):**
- Official government road closures or curfews
- Severe weather warnings (NCM official alert level red)
- Major public events causing gridlock (declared 24 hours in advance)
- Widespread telecommunications outage (>30% of zone)
- Security incidents (active police operations in zone)

**SLA exclusions:**
- Customer-caused delays (wrong location, unreachable, incorrect vehicle info)
- Customer-cancelled jobs before provider en route
- Jobs outside launch geography
- Requests for unavailable service categories in zone
- Provider availability during declared force majeure (best-effort only)

**Declaration process:** Ops manager declares force majeure; customer notification via app banner; SLA clocks paused; post-event report within 48 hours.

---

## SLA Improvement Targets

| SLA | Launch (Month 1–3) | Stabilization (Month 4–12) | Maturity (Year 2+) |
|-----|--------------------|-----------------------------|---------------------|
| C1: Time to first offer (≤5 min, P90) | 85% | 90% | 95% |
| C2: Arrival within ETA ±15 min | 80% | 85% | 90% |
| C3: Job completion rate | 92% | 95% | 97% |
| C3: No-show rate | <2% | <1% | <0.5% |
| C4: Platform availability | 99.0% | 99.5% | 99.9% |
| P2: Payout T+2 compliance | 95% | 98% | 99% |
| B1: Partner dispatch ≤4 min (P90) | 88% | 92% | 95% |

---

## Business Examples

**Example 1 — C1 breach:** Customer submits tow request in Business Bay at 8 PM. First offer arrives at 6 minutes 20 seconds. Within SLA (≤8 min for first offer) but ops notes zone supply gap. No auto-remedy. If customer had cancelled at 7 minutes with zero offers, AED 30 credit would apply.

**Example 2 — C2 breach with auto-remedy:** Customer accepts offer with 20-minute ETA. Provider arrives at 58 minutes (38 min late). System auto-applies 25% partial refund (AED 70 on AED 280 job). Provider SPS penalized. Customer also offered free re-dispatch option at 35-minute mark (declined; waited).

**Example 3 — B2B SLA credit:** Insurance partner job in Sharjah (Phase 1 zone). First offer at 5 minutes 10 seconds (SLA: ≤4 min P90). Partner monthly scorecard shows 91% compliance (below 95%). Contractual SLA credit of AED 15,000 applied to next invoice.

**Example 4 — Force majeure:** NCM red alert for flooding in Dubai. Ops manager declares force majeure 6 AM–2 PM. All SLA clocks paused. 47 active requests queued; customers notified. SLAs resume 2 PM; backlog cleared by 6 PM with extended ETAs communicated.

---

## Business Decisions

| Decision | Rationale |
|----------|-----------|
| ±15 minute arrival window | Accounts for UAE traffic unpredictability while setting clear expectation |
| Auto-remedies without customer request | Reduces support load; demonstrates proactive accountability |
| Stricter B2B dispatch SLA (4 min vs. 5 min) | Partners pay premium; higher expectation justified |
| T+2 payout standard (T+1 premium) | Balances provider cash flow with dispute window |
| Force majeure requires ops manager declaration | Prevents blanket SLA avoidance; documented and time-bound |
| Remedy cap: one auto + one manual per job | Prevents remedy stacking abuse |

---

## Risks

| Risk | Impact | Mitigation |
|------|--------|------------|
| SLA commitments exceed launch capability | High | Launch targets lower than mature; zone gating |
| Auto-remedy cost at scale | Medium | Monitor remedy cost as % GMV; tune thresholds |
| Provider ETA gaming (optimistic ETAs) | Medium | ETA accuracy tracked in SPS; penalties for pattern |
| B2B SLA credits erode partnership margin | Medium | Credits capped monthly; root cause reduction focus |
| Customer expectation inflation from remedies | Low | Clear SLA communication; not marketed as guarantee insurance |

---

## Assumptions

- Launch geography has sufficient provider density to meet C1 SLA 85% of the time
- Automated remedy application is technically feasible at MVP
- AED 30–50 credit remedies cost less than support-handled dispute resolution
- B2B partners accept 95% SLA compliance as industry-standard
- Force majeure events affect <2% of operating hours annually

---

## Open Questions

- Publish customer-facing SLA page in app (transparency) or internal-only?
- SLA-backed premium subscription tier (guaranteed 3-min offer) in Phase 2?
- Provider SLA penalties (financial) in addition to SPS impact?
- Independent SLA audit for B2B partners?

---

## Next Steps

1. Configure automated SLA monitoring and remedy triggers
2. Build real-time SLA dashboard for ops team
3. Include SLA summary in customer terms and B2B contract templates
4. Train support team on SLA breach remedies and force majeure protocol
5. Establish weekly SLA review meeting starting launch week
