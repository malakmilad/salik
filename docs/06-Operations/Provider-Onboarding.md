# Provider Onboarding — Salik Assist

| Field | Value |
|-------|-------|
| **Version** | 1.0 |
| **Status** | Draft |
| **Author** | Product & Strategy Team |
| **Last Updated** | July 4, 2026 |

## Purpose

Define the business process, requirements, and timeline for onboarding independent roadside assistance providers onto the Salik Assist marketplace—from initial interest through activation and first completed job.

## Scope

Covers provider types (tow, battery, tire, fuel, mobile mechanic, lockout), onboarding stages, documentation requirements, training, and go-live criteria for UAE launch. Excludes technical integration details.

## Related Documents

- [Provider Verification](./Provider-Verification.md)
- [Provider Performance](./Provider-Performance.md)
- [Provider Agreement](../07-Legal/Provider-Agreement.md)
- [Operations Workflow](./Operations-Workflow.md)
- [SLA](./SLA.md)
- [Quality Control](./Quality-Control.md)

## Table of Contents

1. [Onboarding Overview](#onboarding-overview)
2. [Eligible Provider Types](#eligible-provider-types)
3. [Onboarding Stages](#onboarding-stages)
4. [Documentation Requirements](#documentation-requirements)
5. [Training & Certification](#training--certification)
6. [Activation Criteria](#activation-criteria)
7. [Launch Incentives](#launch-incentives)
8. [Offboarding & Suspension Triggers](#offboarding--suspension-triggers)
9. [Onboarding Timeline & SLAs](#onboarding-timeline--slas)
10. [Business Examples](#business-examples)
11. [Business Decisions](#business-decisions)
12. [Risks](#risks)
13. [Assumptions](#assumptions)
14. [Open Questions](#open-questions)
15. [Next Steps](#next-steps)

---

## Onboarding Overview

Salik Assist onboarding transforms independent roadside businesses into verified marketplace participants. The process is designed to be completable in **5–10 business days** for standard applicants and **3–5 business days** for priority (field-recruited) applicants.

**Onboarding funnel targets (pre-launch):**

| Stage | Target Conversion |
|-------|-------------------|
| Lead → Application started | 70% |
| Application started → Documents submitted | 80% |
| Documents submitted → Verification passed | 85% |
| Verification passed → Training completed | 95% |
| Training completed → First job within 14 days | 75% |

---

## Eligible Provider Types

| Category | Description | Minimum Fleet |
|----------|-------------|---------------|
| **Tow / Recovery** | Flatbed, wheel-lift, heavy recovery | 1 operational tow truck |
| **Battery** | Jump-start, battery replacement | 1 service vehicle with equipment |
| **Tire** | Flat repair, spare swap, mobile tire change | 1 service vehicle |
| **Fuel Delivery** | Emergency fuel (petrol/diesel) | 1 licensed delivery vehicle |
| **Mobile Mechanic** | On-site minor repair, diagnostics | 1 equipped service van |
| **Lockout** | Vehicle lockout assistance | 1 service vehicle |

Providers may register multiple categories under one business entity if credentials and equipment support each service line.

**Ineligible at launch:** Unlicensed operators, providers without valid UAE trade license, individuals without commercial vehicle insurance.

---

## Onboarding Stages

### Stage 1: Lead Capture & Qualification (Day 0–1)

**Channels:**
- Field sales (tow yards, Al Quoz industrial area, battery retailers)
- Provider referral program (existing provider refers new provider)
- Inbound web/application form
- Industry association partnerships

**Qualification checklist:**
- [ ] Valid UAE trade license (or free zone equivalent)
- [ ] At least one operational service vehicle
- [ ] Service area overlaps with Salik launch geography
- [ ] No active legal proceedings related to consumer fraud or safety violations
- [ ] Willingness to accept platform commission structure

**Outcome:** Qualified lead receives application link and dedicated onboarding contact.

### Stage 2: Application Submission (Day 1–3)

Provider completes business profile:
- Legal business name and trade license number
- Owner/authorized signatory details
- Service categories offered
- Service radius and base location
- Fleet inventory (vehicle type, plate, capacity)
- Bank account for payouts (UAE bank)
- Base pricing by category (within platform guardrails)
- Operating hours and availability schedule

### Stage 3: Verification (Day 3–7)

See [Provider Verification](./Provider-Verification.md) for full criteria. Summary:
- Document authenticity check
- Insurance validation
- Vehicle inspection (photo-based at MVP; in-person for premium tier)
- Background check on authorized signatory

**Outcome:** Approved, conditional approval (missing minor docs), or rejected with reason.

### Stage 4: Training & Certification (Day 5–8)

Mandatory modules (estimated 2 hours total):
1. Platform basics: accepting offers, status updates, pricing rules
2. Customer experience standards and communication
3. Safety protocols (highway, night, female customers)
4. Payment, disputes, and cancellation policies
5. Quality standards by service category

**Assessment:** 80% pass rate on 20-question quiz; practical scenario review with ops team.

### Stage 5: Activation & First Job (Day 7–10)

- Profile goes live in matching pool
- Provider receives "New Provider" badge for first 30 days
- Operations monitors first 5 jobs for quality coaching
- Welcome kit: branded window sticker, QR code for customer referrals

---

## Documentation Requirements

| Document | Required | Validity |
|----------|----------|----------|
| UAE Trade License | Yes | Current; renew within 30 days of expiry |
| Emirates ID (owner/signatory) | Yes | Current |
| Commercial vehicle registration (per fleet unit) | Yes | Current |
| Commercial vehicle insurance | Yes | Min. AED 1M liability; must list roadside/recovery activity |
| RTA or relevant authority permit (tow/recovery) | Yes (tow category) | Category-specific |
| Bank account proof (IBAN letter) | Yes | Matches business name |
| VAT registration (TRN) | If applicable | Required if annual turnover > AED 375K |
| Employee visas / labor cards | If applicable | For employed drivers |

All documents submitted as clear photos or PDFs; originals verified on spot-check basis (10% random audit).

---

## Training & Certification

| Module | Duration | Format | Pass Criteria |
|--------|----------|--------|---------------|
| Platform Operations | 45 min | Video + live Q&A | 80% quiz score |
| Customer Experience | 30 min | Video + role-play | Scenario completion |
| Safety & Compliance | 30 min | Video + checklist | 100% on safety items |
| Pricing & Payments | 15 min | Document review | Acknowledgment signed |

**Recertification:** Annual refresher required; immediate retraining triggered by 2+ quality violations in 90 days.

**Languages:** Arabic and English training materials; Urdu/Hindi supplementary guides for driver staff.

---

## Activation Criteria

Provider is activated when ALL conditions are met:

1. Verification status = Approved
2. Training certification = Complete
3. [Provider Agreement](../07-Legal/Provider-Agreement.md) signed electronically
4. Base pricing configured within platform guardrails
5. At least one fleet vehicle marked "Available"
6. Payout bank account verified
7. Profile photo and business logo uploaded

**Soft launch option:** Providers may be activated in "shadow mode" (receive offers but flagged as training) for first 3 jobs upon ops manager approval.

---

## Launch Incentives

| Incentive | Details | Duration |
|-----------|---------|----------|
| Zero commission | 0% platform fee on first 20 completed jobs | First 60 days post-launch |
| Referral bonus | AED 500 per verified provider referred | Ongoing |
| Priority placement | New providers in underserved zones get matching boost | First 30 days |
| Fast-track onboarding | 3-day verification for field-recruited providers | Launch phase only |

Incentives stack unless otherwise noted; total launch subsidy budget capped per provider at AED 2,000.

---

## Offboarding & Suspension Triggers

| Trigger | Action |
|---------|--------|
| Trade license expired >30 days | Suspension until renewed |
| Insurance lapse | Immediate suspension |
| Rating drops below 3.5 (rolling 30 jobs) | Performance review; possible suspension |
| 3 no-shows in 90 days | Suspension pending investigation |
| Fraud or document falsification | Permanent removal |
| Provider request | Voluntary offboarding; 30-day notice for pending payouts |

---

## Onboarding Timeline & SLAs

| Milestone | Target SLA | Owner |
|-----------|------------|-------|
| Lead response | ≤24 hours | Field sales / Inside sales |
| Application review initiation | ≤48 hours of submission | Onboarding team |
| Verification completion | ≤5 business days | Verification team |
| Training scheduling | ≤2 business days after verification | Onboarding team |
| Activation after training | ≤24 hours | Operations |
| First job offer received | ≤7 days of activation | Platform / Ops monitoring |

---

## Business Examples

**Example 1 — Tow yard in Al Quoz:** Field sales rep visits tow yard with 4 flatbeds. Owner completes application on-site, uploads trade license photos. Verification passes in 4 days. Two drivers complete training in Arabic. Yard activated with all 4 vehicles; receives first offer within 48 hours. Zero-commission period yields 22 jobs in first month.

**Example 2 — Solo battery specialist:** Individual operator with one van applies via web. Missing RTA permit (not required for battery category). Conditional approval granted. Completes training, activates. First 5 jobs monitored by ops; customer feedback prompts coaching on ETA communication. Rating stabilizes at 4.6 after 15 jobs.

**Example 3 — Rejected applicant:** Applicant submits expired trade license and insurance certificate covering personal use only. Verification fails. Applicant notified with specific remediation steps. Re-applies 3 weeks later with valid documents; approved on second attempt.

---

## Business Decisions

| Decision | Rationale |
|----------|-----------|
| 5–10 day standard onboarding timeline | Balances verification rigor with provider acquisition velocity |
| Mandatory training before activation | Reduces early-job quality failures that damage marketplace trust |
| Zero-commission launch incentive | Overcomes provider skepticism; builds supply density quickly |
| Photo-based verification at MVP | Faster onboarding; in-person audit reserved for premium and random checks |
| Multi-category registration under one entity | Reflects how many UAE roadside businesses operate multiple service lines |
| 30-day "New Provider" badge | Signals to customers that provider is new; sets appropriate expectations |

---

## Risks

| Risk | Impact | Mitigation |
|------|--------|------------|
| Slow onboarding delays launch supply target | High | Field sales blitz; fast-track lane; dedicated onboarding team |
| Fraudulent documentation | High | Multi-step verification; random audits; insurance direct validation |
| Provider churn before first job | Medium | Zero-commission incentive; ops outreach at day 7 if no jobs |
| Training completion drop-off | Medium | In-person sessions for field-recruited; reminder sequences |
| Over-supply in one zone, under-supply in another | Medium | Geographic gating during application; zone-based incentives |

---

## Assumptions

- 150–200 providers needed for Dubai launch density
- 70% of providers will complete onboarding once application started
- Field sales will account for 60% of pre-launch provider sign-ups
- Providers accept 15–20% commission after zero-commission period ends
- Most providers operate 1–3 vehicles, not large fleets

---

## Open Questions

- Minimum provider rating threshold to remain active after first 30 jobs?
- Exclusive territory agreements for anchor providers in underserved corridors?
- Franchise or aggregator model for large multi-vehicle operators?
- Onboarding fee (AED 0 at launch) — introduce nominal fee post-scale to filter low-intent applicants?

---

## Next Steps

1. Hire and train 3 onboarding specialists for launch
2. Build field sales target list: 300 tow yards and battery shops in Dubai
3. Finalize training content in Arabic and English
4. Set up provider referral tracking and payout process
5. Achieve 150 verified, activated providers 2 weeks before consumer app launch
