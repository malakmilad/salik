# Software Requirements Specification (SRS) — Salik Assist MVP

| Field | Value |
|-------|-------|
| **Version** | 1.0 |
| **Status** | Draft |
| **Author** | Engineering |
| **Last Updated** | November 5, 2026 |

## Purpose

Specify software behavior for MVP systems implementing the [PRD](../11-Product-Requirements/PRD.md). This SRS is the contract between product acceptance and engineering implementation.

## Scope

Backend platform, Customer mobile apps, Provider mobile apps, Ops web dashboard. Excludes Phase 1 B2B APIs and multi-country config beyond AED/UAE.

## Related Documents

- [PRD](../11-Product-Requirements/PRD.md)
- [Job State Machine](./Job-State-Machine.md)
- [System Architecture](./System-Architecture.md)
- [API Overview](./API-Overview.md)
- [Database Design](./Database-Design.md)
- [Security](./Security.md)

---

## 1. System Overview

Salik Assist MVP is a marketplace platform that:

1. Accepts roadside assistance requests (tow, battery) in Dubai zones
2. Matches verified available providers and collects competitive offers
3. Lets customers accept one offer and track fulfillment
4. Settles payment on completion and pays providers minus commission
5. Gives ops visibility and manual dispatch fallback

---

## 2. External Interfaces

| Interface | Description |
|-----------|-------------|
| Customer App | iOS + Android |
| Provider App | iOS + Android |
| Ops Dashboard | Web (desktop-first) |
| Payment PSP | Card + Apple Pay tokenization/capture |
| Maps | Geocoding, distance, deep-link navigation |
| SMS | OTP + critical fallbacks |
| Push | FCM + APNs |

---

## 3. Functional Requirements (Software)

### 3.1 Identity Service

| ID | Requirement |
|----|-------------|
| SRS-I01 | Issue OTP for UAE mobiles; rate-limit attempts |
| SRS-I02 | Create guest session with job quota (max 2 completed as guest) |
| SRS-I03 | Upgrade guest → registered preserving job history |
| SRS-I04 | Provider accounts distinct from customer accounts |
| SRS-I05 | Ops users via SSO or email+password with MFA (MVP: MFA required for Admin/Supervisor) |
| SRS-I06 | JWT/session tokens with refresh; revoke on suspend |

### 3.2 Catalog & Coverage

| ID | Requirement |
|----|-------------|
| SRS-G01 | Maintain geofence polygons for MVP zones |
| SRS-G02 | `coverage.check(lat,lng)` returns in/out + waitlist option |
| SRS-G03 | Service catalog: `TOW`, `BATTERY_JUMP`, `BATTERY_REPLACE` |

### 3.3 Request Service

| ID | Requirement |
|----|-------------|
| SRS-R01 | Create request with location, category, vehicle, optional notes/plate |
| SRS-R02 | Reject if &gt;2 active jobs for customer |
| SRS-R03 | Persist price estimate band snapshot on create |
| SRS-R04 | Emit `REQUESTED` → start matching |

### 3.4 Matching & Offers

| ID | Requirement |
|----|-------------|
| SRS-M01 | Query eligible providers by radius, category, availability, verification |
| SRS-M02 | Score and invite candidates; 90s response window |
| SRS-M03 | Accept provider offer payload `{eta_minutes, price_aed}` within guardrails |
| SRS-M04 | Present ≤3 offers to customer; withdraw others on accept |
| SRS-M05 | At t=3m zero offers: expand radius + backup cohort |
| SRS-M06 | At t=5m zero offers: enqueue `manual_dispatch` |
| SRS-M07 | Never auto-assign in B2C without customer accept |

### 3.5 Job Lifecycle

| ID | Requirement |
|----|-------------|
| SRS-J01 | Enforce [Job State Machine](./Job-State-Machine.md) transitions server-side |
| SRS-J02 | Reject illegal transitions with `409` |
| SRS-J03 | Validate Arrived geofence ≤200 m |
| SRS-J04 | Completion confirm / 15-min auto-complete |
| SRS-J05 | Append-only state event log |
| SRS-J06 | Calculate cancellation fees by stage at cancel time |

### 3.6 Tracking

| ID | Requirement |
|----|-------------|
| SRS-T01 | Provider location updates while EN_ROUTE/ARRIVED/IN_PROGRESS |
| SRS-T02 | Customer subscribes to location + state via realtime channel |
| SRS-T03 | Stop sharing location after COMPLETED/CANCELLED |

### 3.7 Payments

| ID | Requirement |
|----|-------------|
| SRS-PAY01 | Save payment method via PSP tokenization |
| SRS-PAY02 | Charge on COMPLETED; block charge earlier |
| SRS-PAY03 | Enforce +15% price cap without customer approval |
| SRS-PAY04 | Record commission 18% (or promo 0%) |
| SRS-PAY05 | Initiate provider payout T+2; hold if DISPUTED |
| SRS-PAY06 | Issue receipts (PDF or in-app detail) |

### 3.8 Ratings & Disputes

| ID | Requirement |
|----|-------------|
| SRS-Q01 | Customer rating 1–5 + comment within 7 days |
| SRS-Q02 | Provider internal customer rating |
| SRS-Q03 | Dispute entity with reasons; notify ops |
| SRS-Q04 | Hold payout on open dispute |

### 3.9 Provider Verification

| ID | Requirement |
|----|-------------|
| SRS-V01 | Document upload + status workflow: submitted → approved/rejected |
| SRS-V02 | Cron/job to suspend on document expiry |
| SRS-V03 | Training completion flag required for activation |
| SRS-V04 | Max 5 vehicles per provider account |

### 3.10 Ops Dashboard

| ID | Requirement |
|----|-------------|
| SRS-O01 | Live job list with SLA countdown |
| SRS-O02 | Manual invite/assign with audit |
| SRS-O03 | Issue service credits |
| SRS-O04 | Provider verify/suspend actions |
| SRS-O05 | Role-based permissions |

### 3.11 Notifications

| ID | Requirement |
|----|-------------|
| SRS-N01 | Push templates for offer, assign, en route, arrived, pay, cancel |
| SRS-N02 | SMS OTP + fallback for assignment critical path |
| SRS-N03 | Localize notification copy AR/EN |

### 3.12 Localization

| ID | Requirement |
|----|-------------|
| SRS-L01 | All user-facing strings via i18n keys |
| SRS-L02 | RTL support in customer and provider apps |

---

## 4. Non-Functional Requirements

Inherited from PRD NFR-1…NFR-10. Additional:

| ID | Requirement |
|----|-------------|
| SRS-NFR11 | Idempotent payment and state-transition APIs |
| SRS-NFR12 | PII encrypted at rest where stored; minimize retention |
| SRS-NFR13 | Backups daily; RPO ≤24h MVP; RTO ≤4h target |
| SRS-NFR14 | Feature flags for soft-launch invite gate |

---

## 5. Data Requirements

See [Database Design](./Database-Design.md). Core entities: User, Provider, Vehicle, Document, Request/Job, Offer, Payment, Payout, Rating, Dispute, CoverageZone, AuditEvent.

---

## 6. Constraints

- No cash collection flows
- No owned-fleet dispatch modules
- AED only at MVP
- Server is source of truth for fees, commission, and state

---

## 7. Acceptance

A requirement is done when:

1. Automated tests cover happy path + key guards
2. Product signs acceptance criteria in linked PRD stories
3. Ops runbook updated for manual paths (dispatch, dispute)
