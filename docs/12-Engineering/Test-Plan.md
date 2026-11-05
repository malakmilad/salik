# Test Plan — Salik Assist MVP

| Field | Value |
|-------|-------|
| **Version** | 1.0 |
| **Status** | Draft |
| **Author** | Engineering & QA |
| **Last Updated** | November 5, 2026 |

## Purpose

Define how we prove the MVP is safe to soft-launch and publicly launch.

## Test Layers

| Layer | Ownership | Focus |
|-------|-----------|-------|
| Unit | Eng | State machine guards, fee calc, commission, eligibility |
| API integration | Eng | Auth, jobs, offers, payments (sandbox) |
| Mobile E2E | QA + Eng | Customer + Provider happy paths |
| Ops E2E | QA + Ops | Manual dispatch, suspend, credits |
| Mystery shop | Ops | ≥10 pre-launch real-world jobs |
| Load (light) | Eng | Matching fan-out + tracking updates |

## Must-Pass Scenarios (Launch Gate)

1. Guest OTP → request tow in-zone → 3 offers → accept → track → complete → pay → rate
2. Battery jump happy path
3. Out-of-zone → waitlist, no job
4. Zero offers → expand → ops manual invite → accept
5. Cancel within 3-min grace → AED 0
6. Cancel after en route → correct fee
7. Provider Arrived rejected if &gt;200 m
8. Price &gt;15% over estimate blocked without approval
9. Unverified provider never receives invites
10. Expired insurance auto-suspend (simulated)
11. Dispute holds payout
12. AR/EN language switch on critical screens
13. Apple Pay / card sandbox capture on complete
14. Provider payout scheduled T+2 in ledger (sandbox)

## Exit Criteria

| Gate | Criteria |
|------|----------|
| Alpha | 50 internal E2E jobs; P0 bugs = 0 open |
| Soft launch | Must-pass 1–14 green on staging; invite flag on |
| Public | App store live; payment production verified; launch checklist complete |

## Bug Severity

- **P0:** Payment wrong, state cheat, security, crash on request path
- **P1:** SLA tooling broken, tracking missing, localization broken on core flow
- **P2:** Polish, non-blocking UX

No open P0 at soft launch; no open P0/P1 at public launch.
