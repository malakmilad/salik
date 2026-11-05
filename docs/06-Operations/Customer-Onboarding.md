# Customer Onboarding — Salik Assist

| Field | Value |
|-------|-------|
| **Version** | 1.0 |
| **Status** | Draft |
| **Author** | Product & Strategy Team |
| **Last Updated** | July 4, 2026 |

## Purpose

Define how motorists and B2B users discover, register, and become active customers on Salik Assist—ensuring a friction-minimized first experience optimized for high-stress emergency contexts.

## Scope

Covers consumer (B2C) and business (B2B) customer acquisition, registration, verification, first-job experience, and retention onboarding. Excludes product UI specifications and payment gateway configuration.

## Related Documents

- [Operations Workflow](./Operations-Workflow.md)
- [Customer Support](./Customer-Support.md)
- [Terms Summary](../07-Legal/Terms-Summary.md)
- [Privacy Summary](../07-Legal/Privacy-Summary.md)
- [Go-To-Market](../05-Product-Strategy/Go-To-Market.md)
- [Cancellation Policy](./Cancellation-Policy.md)

## Table of Contents

1. [Onboarding Philosophy](#onboarding-philosophy)
2. [Customer Segments](#customer-segments)
3. [Acquisition Channels](#acquisition-channels)
4. [Registration Paths](#registration-paths)
5. [Account Setup & Verification](#account-setup--verification)
6. [First-Job Experience](#first-job-experience)
7. [B2B Customer Onboarding](#b2b-customer-onboarding)
8. [Retention & Habit Formation](#retention--habit-formation)
9. [Onboarding Metrics & Targets](#onboarding-metrics--targets)
10. [Business Examples](#business-examples)
11. [Business Decisions](#business-decisions)
12. [Risks](#risks)
13. [Assumptions](#assumptions)
14. [Open Questions](#open-questions)
15. [Next Steps](#next-steps)

---

## Onboarding Philosophy

Roadside assistance customers are often stressed, stranded, and time-constrained. Salik Assist onboarding follows three principles:

1. **Speed over completeness:** Allow guest checkout for first job; prompt full registration after successful service
2. **Trust before transaction:** Display verification badges, SLA commitments, and price ranges before request submission
3. **Zero surprise pricing:** Show estimated price range and cancellation terms before customer commits

**Target:** First-time customer from app open to request submitted in **≤90 seconds**.

---

## Customer Segments

| Segment | Profile | Onboarding Priority |
|---------|---------|---------------------|
| **Emergency first-timer** | Breakdown in progress; no prior app install | Guest checkout + SMS receipt |
| **Prepared motorist** | Installed app before need; saved vehicle profile | Full account; fastest path |
| **Expat / tourist** | Unfamiliar with local providers; may lack UAE payment methods | Multi-language; international card support |
| **Fleet manager** | Manages 10–500 vehicles; needs billing and reporting | B2B portal onboarding |
| **Insurance policyholder** | Accesses via insurer app or co-branded link | Policy-linked account; zero checkout |

---

## Acquisition Channels

| Channel | Onboarding Flow | CAC Target (Year 1) |
|---------|-----------------|---------------------|
| App Store / Google Play organic | Install → register → save vehicle | AED 0 (organic) |
| Performance marketing (search, social) | Landing page → install → first request | AED 45–65 |
| Referral program | Existing customer shares code → new user AED 30 credit | AED 25 (blended) |
| Roadside QR signage | Scan → mobile web → guest or install | AED 15 |
| Insurance / fleet B2B | Partner redirect → policy-linked account | AED 10 (partner subsidized) |
| Dealership / car wash partnerships | Co-branded flyer → install with promo code | AED 35 |
| SEO (emergency intent keywords) | Web → guest request or install | AED 20 |

---

## Registration Paths

### Path A: Guest Checkout (Emergency-Optimized)

**Steps:**
1. Open app or mobile web
2. Allow location access (or pin drop)
3. Select service category and vehicle type
4. Enter mobile number (OTP verification)
5. Add payment method OR select "Pay provider directly" where permitted
6. Submit request

**Post-job:** Prompt to create full account with saved vehicle, payment, and job history.

**Limits:** Maximum 2 guest jobs before full registration required; no referral credits for guest users until registered.

### Path B: Full Registration (Pre-Emergency)

**Steps:**
1. Download app
2. Register via mobile number + OTP (or Apple/Google sign-in)
3. Add profile name and preferred language (Arabic / English)
4. Add vehicle(s): make, model, year, plate (optional)
5. Add payment method
6. Optional: enable location permissions, notification preferences
7. Optional: enter referral code

**Incentive:** AED 30 credit on first completed job for registered users (launch promotion).

### Path C: B2B / Insurance Linked

**Steps:**
1. Customer taps "Roadside Help" in partner app or receives partner SMS link
2. Policy or fleet ID validated by partner
3. Salik Assist account auto-created or linked to existing account
4. Customer proceeds directly to request flow with pre-authorized billing

---

## Account Setup & Verification

| Element | Requirement | Purpose |
|---------|-------------|---------|
| Mobile number | Required (OTP verified) | Contact during job; account recovery |
| Email | Optional at registration; required for receipts | Transaction records |
| Payment method | Required before request (B2C) or partner billing (B2B) | Capture at job completion |
| Vehicle profile | Optional pre-job; required for 3rd+ job | Accurate matching and pricing |
| Emirates ID | Not required (B2C) | B2B fleet admin verification only |
| Terms acceptance | Required (implicit on first request) | Legal compliance |

**Age requirement:** Users must be 18+ or authorized vehicle operator.

---

## First-Job Experience

Salik Assist treats the first job as the highest-stakes onboarding moment. Dedicated first-job playbook:

| Touchpoint | Action |
|------------|--------|
| Pre-request | Display "First time?" tooltip explaining top-3 offer model |
| During matching | Progress indicator: "Finding nearby help..." with SLA timer |
| Offer presentation | Highlight verification badge, ETA, and price range with plain-language explanation |
| After acceptance | "Your provider is [Name], arriving in [X] min" with tracking link |
| During service | Single support contact button; no marketing |
| Post-completion | Thank-you message; rating prompt; AED 30 credit confirmation (if eligible) |
| +24 hours | Email receipt; prompt to save vehicle; referral share offer |

**First-job success criteria:**
- Request to offer: ≤5 minutes
- Customer rating: ≥4.0 average for first-time users
- Repeat usage within 90 days: ≥15% target

---

## B2B Customer Onboarding

### Fleet Operators

1. Sales contract signed ([Provider Agreement](../07-Legal/Provider-Agreement.md) equivalent for fleet clients)
2. Fleet admin account created with company TRN and billing details
3. Admin adds vehicles (bulk upload or manual)
4. Admin invites drivers (optional driver app access)
5. Pilot: 10–20 test dispatches with ops support
6. Go-live: full fleet access with monthly consolidated billing

**Timeline:** 4–8 weeks from contract to go-live.

### Insurance Partners

1. Partnership agreement with rate card and SLA
2. Policyholder authentication method agreed (policy number, plate, or partner API handoff)
3. Co-branded experience configured
4. Pilot with 500–1,000 policyholders in one emirate
5. Full rollout with call-center integration option

**Timeline:** 6–9 months from LOI to production volume.

---

## Retention & Habit Formation

| Lifecycle Stage | Trigger | Action |
|-----------------|---------|--------|
| Day 0 | First job completed | Thank-you + referral prompt |
| Day 3 | No second open | Push: "Save your vehicle for faster help next time" |
| Day 30 | No activity | Email: seasonal tip (battery check before summer) |
| Day 90 | No activity | Win-back: AED 20 credit |
| Post-breakdown | Job completed | "Add Salik Assist to your emergency contacts" prompt |
| Annual | Account anniversary | Safety checklist content (tire, battery, insurance) |

**Preparedness positioning:** Salik Assist aims to be installed before the breakdown, not discovered during it. Pre-emergency content marketing supports this habit.

---

## Onboarding Metrics & Targets

| Metric | Launch Target | Year 1 Target |
|--------|---------------|---------------|
| Guest-to-registered conversion | 40% | 55% |
| Registration completion rate | 75% | 85% |
| Time to first request (registered users) | ≤3 min median | ≤2 min |
| First-job completion rate | 88% | 92% |
| First-job NPS | ≥40 | ≥50 |
| D30 retention (registered) | 25% | 35% |
| Referral rate (post first job) | 8% | 12% |

---

## Business Examples

**Example 1 — Highway emergency guest user:** Motorist on E611 blows a tire, searches "tow truck Dubai" on phone, lands on Salik Assist mobile web. Guest checkout: location auto-detected, selects tire service, enters phone number, adds card. Three offers in 3 minutes. Accepts, tracked, pays AED 175. Post-job creates account; saves Toyota Land Cruiser profile.

**Example 2 — Prepared expat:** New UAE resident downloads Salik Assist after colleague recommendation. Registers fully, adds 2022 Nissan Altima, enables notifications. Three months later battery dies in mall parking. Opens app, one-tap request with pre-filled vehicle. Offer in 90 seconds. Rates 5 stars; shares referral code with two colleagues.

**Example 3 — Fleet onboarding:** Delivery company with 80 vans signs B2B contract. Fleet admin uploads vehicle list, trains 5 dispatchers. Pilot week: 12 test jobs across Dubai. Month 1 production: 45 roadside events, consolidated invoice AED 11,200. Driver satisfaction survey: 4.2/5.

---

## Business Decisions

| Decision | Rationale |
|----------|-----------|
| Guest checkout allowed for emergencies | Friction kills conversion when customer is stranded; register after trust is earned |
| Mobile number as primary identity | Universal in UAE; supports OTP; works for tourists with roaming |
| AED 30 first-job credit for registered users | Incentivizes pre-install behavior; lower cost than emergency acquisition |
| 2-guest-job limit before registration | Prevents abuse while allowing genuine emergency access |
| No Emirates ID required for B2C | Reduces friction; mobile + payment verification sufficient for marketplace |
| Separate B2B onboarding track | Fleet and insurance have distinct billing, compliance, and training needs |

---

## Risks

| Risk | Impact | Mitigation |
|------|--------|------------|
| Guest users never convert to registered | Medium | Post-job prompts; credit tied to registration |
| First-job failure destroys retention | High | First-job ops monitoring; priority support queue |
| Tourist payment method failures | Medium | International card support; pay-provider-direct fallback |
| B2B onboarding delays partnership revenue | High | Dedicated partnerships team; pilot-first approach |
| App not installed before emergency | High | QR signage; SEO; preparedness marketing; insurance embed |

---

## Assumptions

- 60% of first-time users will arrive via emergency context (not pre-installed)
- Mobile OTP verification achieves 95%+ deliverability in UAE
- AED 30 credit is sufficient to drive registration without excessive subsidy cost
- Fleet B2B customers require 4–8 week onboarding regardless of product simplicity
- Arabic and English cover 95%+ of target customer base at launch

---

## Open Questions

- Require account registration before request during non-emergency "schedule ahead" feature (Phase 2)?
- Family account sharing (one subscription, multiple drivers)?
- Corporate employee benefit program (employer-sponsored roadside coverage)?
- WhatsApp-based request channel for customers without app install?

---

## Next Steps

1. Finalize guest checkout flow and 2-job limit business rules
2. Launch referral program creative and tracking before consumer go-live
3. Create first-job ops monitoring dashboard
4. Develop B2B fleet onboarding kit (contract template, training deck, pilot checklist)
5. Prepare Arabic and English onboarding help content for support team
