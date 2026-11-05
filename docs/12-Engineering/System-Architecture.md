# System Architecture — Salik Assist MVP

| Field | Value |
|-------|-------|
| **Version** | 1.0 |
| **Status** | Draft |
| **Author** | Engineering |
| **Last Updated** | November 5, 2026 |

## Purpose

Describe the high-level MVP architecture so mobile, backend, and ops clients can be built against a shared design.

## Related Documents

- [SRS](./SRS.md)
- [API Overview](./API-Overview.md)
- [Database Design](./Database-Design.md)
- [Security](./Security.md)
- [Deployment](./Deployment.md)

---

## Architecture Style

**Modular monolith (recommended for MVP)** with clear domain modules, plus managed third-party services. Split to microservices only when a module’s scale or release cadence demands it post–Product-Market Fit.

```text
┌─────────────┐  ┌─────────────┐  ┌──────────────┐
│ Customer App│  │ Provider App│  │ Ops Web App  │
└──────┬──────┘  └──────┬──────┘  └──────┬───────┘
       │ HTTPS/JSON      │                │
       └────────────┬────┴────────────────┘
                    ▼
            ┌───────────────┐
            │  API Gateway  │  (auth, rate limit, WAF)
            └───────┬───────┘
                    ▼
            ┌───────────────┐
            │  App Server   │  modular monolith
            │  (domain APIs)│
            └───┬───┬───┬───┘
                │   │   │
       ┌────────┘   │   └────────┐
       ▼            ▼            ▼
   PostgreSQL    Redis       Object Store
   (primary)   (cache/locks/ (docs, photos)
                realtime bus)
       │
       ▼
   Workers (matching timers, payouts, expiry suspend)
```

---

## Domain Modules

| Module | Responsibility |
|--------|----------------|
| Identity | OTP, sessions, roles, guest quota |
| Coverage | Geofences, waitlist |
| Requests | Create/validate requests |
| Matching | Eligibility, scoring, invitations, offer window |
| Jobs | State machine, tracking, cancellations |
| Payments | PSP integration, commission, receipts |
| Payouts | Provider settlements, holds |
| Providers | Onboarding, vehicles, documents, availability |
| Ratings | Stars, moderation flags |
| Disputes | Cases, holds, ops workflow |
| Notifications | Push/SMS templates |
| Ops | Manual dispatch, credits, audits |
| Pricing | Guardrails, estimate bands |

---

## Realtime

- Provider location + job state → Redis pub/sub or managed websocket/SSE
- Customer and Ops subscribe by `job_id`
- Fallback: client polling every 5–10s if socket drops

---

## Third-Party Integrations

| System | Use |
|--------|-----|
| Payment PSP | Tokenize, authorize/capture, refunds |
| Maps SDK | Customer/provider maps, ETA assist |
| Distance Matrix / Routing | Matching radius & ETA sanity (optional MVP: haversine + traffic buffer) |
| SMS gateway | OTP |
| FCM / APNs | Push |
| Object storage | KYC docs, job photos |
| Error monitoring | Crash/API errors |
| Analytics | Funnel + SCAJ metrics |

---

## Key Design Decisions

| Decision | Rationale |
|----------|-----------|
| Modular monolith first | Faster MVP, simpler transactions for job+payment |
| Server-authoritative state machine | Prevents client cheating on Arrived/Complete/fees |
| Async workers for timers | 90s/3m/5m/15m/24h reliably |
| Feature flag soft-launch | Invite-only without rebuild |
| Separate provider vs customer identity | Clearer permissions and suspension |

---

## Environment Topology

| Env | Purpose |
|-----|---------|
| `dev` | Local / shared dev |
| `staging` | QA + mystery shop |
| `production` | Live UAE |

See [Deployment](./Deployment.md).

---

## Scalability Notes (Post-MVP)

- Extract Matching + Notifications if fan-out latency grows
- Read replicas for ops reporting
- Multi-region only when expanding beyond UAE
