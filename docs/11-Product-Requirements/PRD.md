# Product Requirements Document (PRD) — Salik Assist MVP

| Field | Value |
|-------|-------|
| **Version** | 1.0 |
| **Status** | Draft — Ready for engineering kickoff |
| **Author** | Product & Engineering |
| **Last Updated** | November 5, 2026 |
| **Launch target** | Dubai MVP (W0 TBD) |

## Purpose

Define build-ready product requirements for the Salik Assist MVP: a two-sided roadside assistance marketplace where a stranded motorist receives up to three verified provider offers, tracks arrival, pays on completion, and rates the job.

## Scope

**In scope:** Customer iOS/Android app, Provider iOS/Android app, Ops web dashboard, Tow + Battery categories, Dubai launch zones, guest checkout, card/Apple Pay, bilingual AR/EN.

**Out of scope (Phase 1+):** Tire/fuel/mechanic/lockout, B2B/insurance, Abu Dhabi/Sharjah, subscriptions, WhatsApp, desktop web, tipping, scheduled jobs, automated surge.

## Related Documents

- [MVP](../09-Roadmap/MVP.md)
- [BRD](./BRD.md)
- [Business Rules](../04-Business/Business-Rules.md)
- [Operations Workflow](../06-Operations/Operations-Workflow.md)
- [Job State Machine](../12-Engineering/Job-State-Machine.md)
- [SRS](../12-Engineering/SRS.md)
- [Cancellation Policy](../06-Operations/Cancellation-Policy.md)
- [SLA](../06-Operations/SLA.md)

## Table of Contents

1. [Goals](#goals)
2. [Personas & Surfaces](#personas--surfaces)
3. [Success Metrics](#success-metrics)
4. [Feature Epics](#feature-epics)
5. [User Stories & Acceptance Criteria](#user-stories--acceptance-criteria)
6. [Non-Functional Requirements](#non-functional-requirements)
7. [Business Rules Mapping](#business-rules-mapping)
8. [Dependencies & Assumptions](#dependencies--assumptions)
9. [Risks](#risks)
10. [Open Questions](#open-questions)
11. [Release Plan](#release-plan)

---

## Goals

| Goal | Measure |
|------|---------|
| Validate top-3 offer marketplace in Dubai | ≥70% offer acceptance when ≥2 offers shown |
| Deliver help under emergency friction | Request submit &lt; 60s for 95% of sessions |
| Meet offer SLA | P90 time-to-first-offer ≤ 5 minutes |
| Complete paid jobs reliably | Job completion rate ≥ 88% at Day 90 |
| Convert guests to accounts | ≥40% guest → registered within 2 jobs |

**North Star (platform):** Successfully Completed Assisted Jobs (SCAJ).

---

## Personas & Surfaces

| Persona | Surface | Primary jobs-to-be-done |
|---------|---------|-------------------------|
| Stranded motorist (guest or registered) | Customer app | Get help fast, compare offers, track, pay, rate |
| Tow / battery provider | Provider app | Receive offers, navigate, update status, earn |
| Ops agent / supervisor | Ops dashboard | Monitor SLAs, manual dispatch, escalate, verify providers |

---

## Success Metrics

Aligned with [MVP Success Metrics](../09-Roadmap/MVP.md#mvp-success-metrics):

| Metric | Target (90 days) |
|--------|------------------|
| Completed jobs | 8,500 |
| Completion rate | ≥88% |
| Time to first offer (P90) | ≤5 min |
| Avg customer rating | ≥4.2 |
| Provider retention (M3) | ≥65% of launch cohort |
| Support contact rate | ≤15% |
| No-show rate | &lt;2% |

---

## Feature Epics

| Epic ID | Name | Priority | Surfaces |
|---------|------|----------|----------|
| E1 | Identity & Access | P0 | Customer, Provider, Ops |
| E2 | Customer Request | P0 | Customer |
| E3 | Matching & Offers | P0 | Customer, Provider, Platform |
| E4 | Job Lifecycle & Tracking | P0 | Customer, Provider |
| E5 | Payments & Settlement | P0 | Customer, Provider, Platform |
| E6 | Ratings & Support | P0 | Customer, Provider, Ops |
| E7 | Provider Onboarding & Verification | P0 | Provider, Ops |
| E8 | Ops Monitoring & Manual Dispatch | P0 | Ops |
| E9 | Localization & Coverage Gates | P0 | All |
| E10 | Notifications | P0 | Customer, Provider |

---

## User Stories & Acceptance Criteria

### E1 — Identity & Access

#### US-C01 — Guest checkout with OTP
**As a** stranded motorist, **I want** to request help with only my mobile number, **so that** I am not blocked by registration during an emergency.

**Acceptance criteria:**
- [ ] User enters UAE mobile number and verifies via OTP
- [ ] Guest may complete up to **2 jobs** without full registration
- [ ] On 3rd job attempt, registration (name + optional email) is required before submit
- [ ] Session persists across app restarts until logout
- [ ] Age attestation: user confirms 18+ (Rule 15)

#### US-C02 — Registered customer account
**As a** returning customer, **I want** to save a payment method and vehicle, **so that** re-requests are faster.

**Acceptance criteria:**
- [ ] Account stores: name, mobile, preferred language (AR/EN), 1 vehicle profile
- [ ] Saved card tokenization via payment provider (no raw PAN stored)
- [ ] User can switch language AR ↔ EN with full UI parity

#### US-P01 — Provider login
**As a** verified provider, **I want** to sign in and set availability, **so that** I only receive offers when ready.

**Acceptance criteria:**
- [ ] Login via mobile OTP or email+password (choose one primary; document in SRS)
- [ ] Toggle Available / Unavailable
- [ ] Unverified or suspended accounts cannot receive offers (Rules 1, 5)

#### US-O01 — Ops authentication
**As an** ops agent, **I want** role-based access to the dashboard, **so that** sensitive actions are controlled.

**Acceptance criteria:**
- [ ] Roles: Agent, Supervisor, Verifier, Admin
- [ ] Audit log for manual dispatch, refunds, suspensions

---

### E2 — Customer Request

#### US-C03 — Create roadside request
**As a** customer, **I want** to submit location, service type, and vehicle info in under 60 seconds, **so that** help starts immediately.

**Acceptance criteria:**
- [ ] Auto-capture GPS; allow pin-drop override
- [ ] Service types MVP: **Tow**, **Battery** (jump-start or replacement)
- [ ] Vehicle type: sedan / SUV / commercial (motorcycle deferred)
- [ ] Optional plate number and issue notes
- [ ] Show estimated price **range** before submit
- [ ] Block submit if outside launch coverage with “Coming soon” + waitlist (Rule 19, BR-M08)
- [ ] Max **2** active uncompleted requests per customer (Rule 17)
- [ ] Highway/high-risk pin flagged for priority matching (ops signal)

#### US-C04 — Tow-specific inputs
**As a** customer requesting tow, **I want** to set drop-off preference, **so that** providers price correctly.

**Acceptance criteria:**
- [ ] Drop-off: nearest safe location OR customer-specified garage pin
- [ ] Distance bands: ≤30 km, ≤80 km reflected in estimate band
- [ ] Photo evidence required post-job for tow (Rule 39) — provider side

#### US-C05 — Battery-specific inputs
**As a** customer requesting battery help, **I want** to choose jump-start vs replacement, **so that** I get the right provider.

**Acceptance criteria:**
- [ ] Subtypes: Jump-start, Battery replacement
- [ ] Replacement shows note: 30-day warranty is provider responsibility (display only at MVP)

---

### E3 — Matching & Offers

#### US-SYS01 — Invite eligible providers
**As the** platform, **I want** to invite the best eligible providers, **so that** customers get competitive offers fast.

**Acceptance criteria:**
- [ ] Eligible = verified + available + category match + within radius + not suspended
- [ ] Default radius 25 km; tow may use up to 40 km
- [ ] Rank by composite: distance, rating, acceptance rate, response time
- [ ] Invite top N candidates (config; default enough to yield ≤3 customer offers)
- [ ] Provider has **90 seconds** to submit ETA + price or decline
- [ ] No auto-assign in B2C (Rule 27)

#### US-C06 — View and compare offers
**As a** customer, **I want** up to 3 offers with ETA, price, rating, and verified badge, **so that** I can choose confidently.

**Acceptance criteria:**
- [ ] Offer window **5 minutes** from request (Rule 22)
- [ ] Each offer shows: name, rating, ETA, price estimate, category, verified badge (Rule 24)
- [ ] If &lt;3 responses, show all valid offers received
- [ ] At 3 min with 0 offers → system expands radius + notifies backup pool
- [ ] At 5 min with 0 offers → escalate to Ops manual dispatch queue
- [ ] Customer may wait up to 8 minutes total if only 1 offer (ops policy)

#### US-C07 — Accept an offer
**As a** customer, **I want** to accept one offer, **so that** a provider is dispatched.

**Acceptance criteria:**
- [ ] Accept binds customer per cancellation policy
- [ ] Other offers auto-withdrawn (Rule 25)
- [ ] Provider must acknowledge assignment within **60 seconds**
- [ ] **3-minute free grace cancel** after acceptance (Cancellation Policy S1)
- [ ] Pre-auth / payment method validation before or at accept (fail closed if no valid method for registered; guest must add method before accept)

#### US-P02 — Submit offer
**As a** provider, **I want** to propose ETA and price within guardrails, **so that** I compete for the job.

**Acceptance criteria:**
- [ ] Price must be within platform min/max guardrails for category/zone (Rule 28)
- [ ] ETA in minutes; must be realistic (ops may audit outliers)
- [ ] Decline does not penalize; repeated non-response (≥5 in 7 days) lowers priority (Rule 12)

---

### E4 — Job Lifecycle & Tracking

#### US-C08 — Live tracking
**As a** customer, **I want** to see provider progress on a map, **so that** I know help is coming.

**Acceptance criteria:**
- [ ] Tracking from accept → arrival
- [ ] States visible: Accepted, En Route, Arrived, In Progress, Completed
- [ ] Provider contact method available after accept (masked number preferred)

#### US-P03 — Update job status
**As a** provider, **I want** to mark En Route / Arrived / In Progress / Complete, **so that** the customer and ops stay informed.

**Acceptance criteria:**
- [ ] En Route starts navigation deep-link (Google/Apple Maps)
- [ ] Arrived only valid within **200 m** of customer pin (Rule 36)
- [ ] Complete requires customer confirm **or** 15 min after provider completion request with no objection (Rule 37)
- [ ] Tow jobs require photo evidence upload before/at complete (Rule 39)
- [ ] Jobs stuck &gt;24h in non-terminal state auto-escalate (Rule 40)

#### US-C09 — Cancel job
**As a** customer or provider, **I want** clear cancellation fees by stage, **so that** cancellations are fair.

**Acceptance criteria:**
- [ ] Enforce [Cancellation Policy](../06-Operations/Cancellation-Policy.md) fee schedule in product
- [ ] S0 (no accept): AED 0
- [ ] S1 &lt;3 min: AED 0; S1 ≥3 min: AED 25
- [ ] En route fees per policy (AED 40 / 60)
- [ ] Provider no-show / unjustified cancel → customer credit AED 25 (Rule 44) + reliability penalty
- [ ] Fees disclosed before offer accept

**Policy note:** Prefer Cancellation Policy fee table over older Rule 41–43 numeric variants until Legal reconciles documents.

---

### E5 — Payments & Settlement

#### US-C10 — Pay on completion
**As a** customer, **I want** to pay digitally when the job completes, **so that** I do not handle cash roadside.

**Acceptance criteria:**
- [ ] Methods: card + Apple Pay (Rule 49 — no cash)
- [ ] Charge only after Completed per Rule 37–38
- [ ] Final price ≤ estimate upper bound +15% without in-app approval (Rule 30)
- [ ] Currency: AED
- [ ] Digital receipt available in app

#### US-P04 — Earnings & payout
**As a** provider, **I want** to see earnings and receive payout within 48 hours, **so that** cash flow is predictable.

**Acceptance criteria:**
- [ ] Platform take rate **18%** of final job value (Rule 46)
- [ ] Payout initiated within **48 hours** of successful collection (Rule 47) — T+2
- [ ] Disputed jobs hold payout ≤14 days (Rule 48)
- [ ] Daily/weekly earnings views; monthly statement

#### US-SYS02 — Commission capture
**As the** platform, **I want** commission deducted automatically, **so that** revenue is consistent.

**Acceptance criteria:**
- [ ] 100% of completed paid jobs record commission
- [ ] Promo discounts funded by platform, not provider (Rule 34)
- [ ] Zero-commission promo window configurable per provider cohort (MVP ops tool)

---

### E6 — Ratings & Support

#### US-C11 — Rate provider
**As a** customer, **I want** to rate 1–5 stars with optional comment within 7 days, **so that** quality stays visible.

**Acceptance criteria:**
- [ ] Prompt after completion; skipable but countable in rating rate KPI
- [ ] Public on provider profile (Rule 51)
- [ ] Moderation for abuse (Rule 53)

#### US-P05 — Rate customer (internal)
**As a** provider, **I want** to rate customer cooperation internally, **so that** ops can manage abuse.

**Acceptance criteria:**
- [ ] Internal only — not shown publicly (Rule 52)

#### US-C12 — Contact support
**As a** customer, **I want** in-app chat and phone support, **so that** disputes and emergencies are handled.

**Acceptance criteria:**
- [ ] In-app chat + phone hotline entry points
- [ ] Dispute filing within 48h of completion (Rule 56)
- [ ] Ticket acknowledge target &lt;4 business hours (Rule 57)

---

### E7 — Provider Onboarding & Verification

#### US-P06 — Submit verification package
**As a** provider applicant, **I want** to upload required documents, **so that** I can be activated.

**Acceptance criteria:**
- [ ] Required: trade license, insurance (≥AED 1M TPL + roadside activity), vehicle registration(s), owner/driver IDs (Rules 2–3)
- [ ] Background check status required before driver activation (Rule 4)
- [ ] Up to **5** vehicles on account (MVP)
- [ ] Training module completion required before activation (MVP ops readiness)

#### US-O02 — Verify / suspend providers
**As a** verifier, **I want** to approve, reject, or suspend providers, **so that** only trusted supply is live.

**Acceptance criteria:**
- [ ] Approve → eligible for offers
- [ ] Auto-suspend on document expiry (Rule 5)
- [ ] Rating &lt;3.5 rolling 90d → improvement period; &lt;3.0 → may deactivate (Rules 7–8)

---

### E8 — Ops Monitoring & Manual Dispatch

#### US-O03 — Live job board
**As an** ops agent, **I want** a real-time view of open jobs and SLA clocks, **so that** I intervene before breach.

**Acceptance criteria:**
- [ ] Filters: awaiting offers, zero-offer risk, en route late, disputed, stuck &gt;24h
- [ ] SLA-C1 timers visible (first offer ≤5 min)

#### US-O04 — Manual dispatch
**As an** ops agent, **I want** to assign or invite a backup provider, **so that** zero-offer jobs still complete.

**Acceptance criteria:**
- [ ] Manual invite/assign logged with agent ID and reason
- [ ] Customer still confirms offer unless emergency override by Supervisor (document policy)
- [ ] Post-incident: optional service credit issuance (SLA remedies AED 30/50)

---

### E9 — Localization & Coverage

#### US-SYS03 — Bilingual product
**As a** user, **I want** full Arabic and English, **so that** I can operate under stress in my language.

**Acceptance criteria:**
- [ ] 100% MVP strings localized AR + EN
- [ ] RTL layout correct for Arabic
- [ ] Provider-facing and customer-facing parity

#### US-SYS04 — Geo fence
**As the** platform, **I want** to enforce Dubai MVP zones, **so that** SLAs are only promised where supply exists.

**Acceptance criteria:**
- [ ] Zones: Dubai Metro districts listed in MVP + E11/E311/E611 Dubai segments + DXB 5 km
- [ ] Out of zone → waitlist capture, no SLA

---

### E10 — Notifications

#### US-SYS05 — Push & SMS
**As a** user, **I want** timely alerts for offers, assignment, arrival, payment, and cancellations.

**Acceptance criteria:**
- [ ] Customer: offers ready, provider en route, arrived, payment receipt, cancel/fee
- [ ] Provider: offer invite (with 90s countdown), job assigned, cancel, payout
- [ ] SMS fallback for critical OTP and assignment if push unavailable

---

## Non-Functional Requirements

| ID | Requirement | Target |
|----|-------------|--------|
| NFR-1 | Request submit latency | p95 &lt; 2s API |
| NFR-2 | Offer fan-out | Providers notified &lt; 3s after match |
| NFR-3 | Location update frequency (en route) | ≤10s |
| NFR-4 | Availability | 99.5% monthly for core APIs (MVP) |
| NFR-5 | Payment success | ≥98% authorized charges on valid methods |
| NFR-6 | Data residency / privacy | UAE PDPL-aligned; consent flows live |
| NFR-7 | Auditability | Full job state timestamps immutable |
| NFR-8 | App support | iOS and Android versions per store policy (last 2 major) |
| NFR-9 | Security | TLS everywhere; secrets in vault; no PAN at rest |
| NFR-10 | Observability | Metrics for offer SLA, completion, payment failures |

---

## Business Rules Mapping

| Product area | Primary rules |
|--------------|---------------|
| Verification | 1–8 |
| Matching & offers | 20–27 |
| Pricing | 28–30, 34 (surge automation deferred) |
| Lifecycle | 35–40 |
| Cancellation | 41–44 + Cancellation Policy table |
| Payment | 46–49 |
| Ratings | 51–55 |
| Disputes | 56–60 |
| Geo | 19, geographic rules section |

P0 business requirements covered: BR-C01–C08, BR-P01–P08, BR-M01–M05, BR-M08–M09, BR-F01–F03, BR-T01–T04, BR-T06. See [BRD](./BRD.md).

---

## Dependencies & Assumptions

| Dependency | Owner |
|------------|-------|
| Payment provider (card + Apple Pay) | Eng + Finance |
| Maps / geocoding / distance matrix | Eng |
| SMS OTP gateway | Eng |
| Push notifications (FCM/APNs) | Eng |
| Provider pipeline ≥150 verified | Ops / Field sales |
| Legal ToS / Privacy / Provider Agreement templates | Legal |
| App Store / Play Console accounts | Product |

**Assumptions:** Soft launch invite-only preferred (Open Q P1); brand “Salik Assist” provisional until S1 closed; native apps for both stores.

---

## Risks

| Risk | Mitigation |
|------|------------|
| Scope creep into Phase 1 categories | Change control; this PRD is source of truth |
| Supply &lt;150 at W0 | Soft launch gated on Launch Checklist |
| Cancellation policy vs Business Rules mismatch | Legal reconcile; product uses Cancellation Policy |
| App store delay | Submit by W-2; alpha builds via TestFlight/Internal track |
| Zero-offer nights | Manual dispatch + on-call ops (O2/O3 decisions) |

---

## Open Questions

Carried from MVP / Open Questions (do not block engineering scaffolding):

1. Soft launch invite-only vs public? (**P1**)
2. Final brand co-branding with Salik toll? (**S1/S2** — Block Launch)
3. Provider app: confirm native vs cross-platform (Flutter/RN) — Eng decision by sprint 0
4. Masked calling provider vs direct number at MVP?

---

## Release Plan

| Build | Contents | Gate |
|-------|----------|------|
| Alpha | Internal E2E jobs (≥50) | Ops + Product |
| Soft launch | Invite ~500 users | Launch checklist ≥90% |
| Public W0 | Open download in UAE | All launch criteria green |

Engineering backlog should be sliced by epic E1→E10 with Job State Machine as shared contract.
