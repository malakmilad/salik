# Operations Workflow — Salik Assist

| Field | Value |
|-------|-------|
| **Version** | 1.0 |
| **Status** | Draft |
| **Author** | Product & Strategy Team |
| **Last Updated** | July 4, 2026 |

## Purpose

Define the end-to-end operational workflow for Salik Assist—from customer request initiation through service completion, payment settlement, and post-job quality review. This document serves as the master reference for operations, support, and launch teams.

## Scope

Covers business and operational stages, roles, handoffs, and decision points for consumer and B2B jobs in the UAE launch market. Excludes technical system design, API specifications, and database schemas.

## Related Documents

- [Provider Onboarding](./Provider-Onboarding.md)
- [Customer Onboarding](./Customer-Onboarding.md)
- [Provider Verification](./Provider-Verification.md)
- [SLA](./SLA.md)
- [Quality Control](./Quality-Control.md)
- [Escalation Policy](./Escalation-Policy.md)
- [Cancellation Policy](./Cancellation-Policy.md)
- [Refund Policy](./Refund-Policy.md)
- [Executive Summary](../01-Executive/Executive-Summary.md)

## Table of Contents

1. [Workflow Overview](#workflow-overview)
2. [Stage 1: Request Intake](#stage-1-request-intake)
3. [Stage 2: Provider Matching & Offers](#stage-2-provider-matching--offers)
4. [Stage 3: Offer Acceptance & Dispatch](#stage-3-offer-acceptance--dispatch)
5. [Stage 4: En Route & Arrival](#stage-4-en-route--arrival)
6. [Stage 5: Service Delivery](#stage-5-service-delivery)
7. [Stage 6: Payment & Settlement](#stage-6-payment--settlement)
8. [Stage 7: Post-Service Review](#stage-7-post-service-review)
9. [B2B & Insurance Workflow Variations](#b2b--insurance-workflow-variations)
10. [Operational Roles & RACI](#operational-roles--raci)
11. [Business Examples](#business-examples)
12. [Business Decisions](#business-decisions)
13. [Risks](#risks)
14. [Assumptions](#assumptions)
15. [Open Questions](#open-questions)
16. [Next Steps](#next-steps)

---

## Workflow Overview

Salik Assist operates a seven-stage operational workflow for every roadside assistance job. Each stage has defined owners, time targets, and escalation triggers aligned with the [SLA](./SLA.md).

```
Customer Request → Matching & Offers → Acceptance → En Route → Service → Payment → Review
```

| Stage | Target Duration | Primary Owner |
|-------|-----------------|---------------|
| Request Intake | 0–2 minutes | Customer (self-serve) / Support (assisted) |
| Matching & Offers | 2–5 minutes | Operations (monitoring) |
| Acceptance & Dispatch | 0–3 minutes | Customer |
| En Route & Arrival | Per offer ETA | Provider |
| Service Delivery | 15–90 minutes (category-dependent) | Provider |
| Payment & Settlement | 0–5 minutes post-completion | Platform |
| Post-Service Review | 24 hours | Quality team |

---

## Stage 1: Request Intake

**Trigger:** Customer experiences breakdown or roadside need and opens Salik Assist (app, web, or B2B partner channel).

**Required inputs:**
- GPS location (or manual pin drop)
- Service category (tow, battery, tire, fuel, mobile mechanic, lockout)
- Vehicle type (sedan, SUV, commercial, motorcycle)
- Issue description (optional but recommended)
- Contact number

**Operational actions:**
1. Validate service area coverage (Dubai metro, E11/E311 corridors at launch)
2. Confirm customer account or guest checkout eligibility
3. Display estimated price range and SLA commitment before submission
4. Flag high-risk locations (highway shoulder, desert off-road) for priority matching

**Exit criteria:** Validated request enters active matching queue.

---

## Stage 2: Provider Matching & Offers

**Process:**
1. System identifies eligible providers within service radius (default: 25 km; 40 km for tow/desert)
2. Top 3 providers by composite score (distance, rating, acceptance rate, response time) receive offer invitation
3. Providers have **90 seconds** to submit or decline
4. Customer receives up to 3 offers showing: provider name, rating, ETA, price estimate, verification badge

**Operations monitoring:**
- If zero offers within 3 minutes → expand radius and notify backup provider pool
- If still zero offers within 5 minutes → manual dispatch by operations team
- If only 1 offer within 5 minutes → customer may accept or wait for additional offers (max 8 minutes total)

**Exit criteria:** Customer has at least one valid offer, or escalation to manual dispatch.

---

## Stage 3: Offer Acceptance & Dispatch

**Customer actions:**
- Compare offers (ETA, price, rating)
- Accept one offer (binding commitment per [Cancellation Policy](./Cancellation-Policy.md))
- Receive provider contact details and live tracking link

**Provider actions:**
- Receive confirmed job assignment
- Acknowledge within **60 seconds**
- Begin route to customer location

**Operations actions:**
- Log acceptance timestamp for SLA tracking
- Send confirmation SMS/push to customer with provider photo, vehicle plate, and ETA

**Exit criteria:** Provider acknowledged and status = "En Route."

---

## Stage 4: En Route & Arrival

**Provider obligations:**
- Update status at departure, en route, and arrival
- Contact customer if ETA changes by more than **10 minutes**
- Arrive within committed ETA window (±15 minutes per [SLA](./SLA.md))

**Operations monitoring:**
- Alert if provider stationary >5 minutes during en-route phase
- Alert if ETA exceeded by >15 minutes without customer notification
- Support team available for customer anxiety calls

**Exit criteria:** Provider marks "Arrived" at customer location.

---

## Stage 5: Service Delivery

**On-site process:**
1. Provider verifies vehicle and issue matches request
2. If scope differs (e.g., tow distance longer than estimated), provider must obtain customer approval for revised price before proceeding
3. Provider performs service per category standards ([Quality Control](./Quality-Control.md))
4. Provider marks "Service Completed" with optional photo evidence

**Dispute prevention:**
- Price changes >20% from estimate require in-app customer confirmation
- Additional services (e.g., storage fee, highway surcharge) must be itemized

**Exit criteria:** Service marked complete by provider; customer acknowledges or auto-acknowledges after 15 minutes.

---

## Stage 6: Payment & Settlement

**Consumer jobs:**
- Customer charged agreed final amount via saved payment method
- Receipt issued immediately with itemized breakdown
- Provider payout initiated within **T+2 business days** (standard) or **T+1** (premium tier)

**B2B / insurance jobs:**
- Billing routed per partner agreement (direct bill, voucher, or zero customer charge)
- Platform fee invoiced to partner monthly

**Disputes:**
- Customer may flag payment issue within **48 hours**
- Funds held pending resolution per [Refund Policy](./Refund-Policy.md)

**Exit criteria:** Payment captured or B2B invoice recorded; provider payout scheduled.

---

## Stage 7: Post-Service Review

**Automated actions:**
- Rating prompt sent to customer (1–5 stars + optional comment)
- Provider performance metrics updated ([Provider Performance](./Provider-Performance.md))
- Quality flags triggered for ratings ≤2 or specific complaint keywords

**Manual review triggers:**
- Rating ≤2 stars
- Customer complaint within 48 hours
- Provider no-show or SLA breach
- Safety-related incident report

**Follow-up:**
- Quality team reviews flagged jobs within **24 hours**
- Resolution communicated to both parties within **72 hours**

---

## B2B & Insurance Workflow Variations

| Variation | Difference from Standard Flow |
|-----------|-------------------------------|
| **Insurance dispatch** | Customer authenticated via policy number; pre-negotiated rates apply; insurer billed directly |
| **Fleet dispatch** | Fleet manager creates request on behalf of driver; consolidated monthly billing |
| **Concierge / hotel** | Third party submits request; customer receives tracking link only |
| **Repeat customer** | Saved vehicle profiles; preferred provider suggestions if available |

All B2B jobs follow the same seven stages but skip consumer payment at Stage 6 where partner billing applies.

---

## Operational Roles & RACI

| Activity | Customer | Provider | Ops Team | Support | Quality | Partnerships |
|----------|----------|----------|----------|---------|---------|--------------|
| Submit request | R/A | — | I | C | — | — |
| Match providers | I | R | A | I | — | — |
| Accept offer | R/A | I | I | C | — | — |
| Deliver service | I | R/A | I | C | — | — |
| Process payment | I | I | R/A | C | — | I |
| Handle dispute | C | C | I | R/A | C | I |
| B2B job routing | I | I | C | I | — | R/A |

*R = Responsible, A = Accountable, C = Consulted, I = Informed*

---

## Business Examples

**Example 1 — Standard tow job:** Customer on Sheikh Zayed Road submits tow request at 2 PM. Three providers respond within 4 minutes. Customer accepts AED 250 offer with 22-minute ETA. Provider arrives in 20 minutes, tows to nearest garage, customer pays AED 265 (highway surcharge approved in-app). Both parties rate 5 stars.

**Example 2 — Zero-offer escalation:** Customer in desert area near Al Qudra submits battery jump-start at 9 PM. No providers respond within 5 minutes. Operations expands radius to 40 km, manually contacts two backup providers, secures one offer at AED 320. Customer accepts; job completes successfully.

**Example 3 — Insurance B2B job:** Policyholder taps "Roadside Help" in insurer app. Request routes to Salik Assist with policy pre-validation. Customer sees zero out-of-pocket. Provider completes tow; insurer billed AED 280 per contracted rate at month-end.

---

## Business Decisions

| Decision | Rationale |
|----------|-----------|
| Seven-stage linear workflow | Clear accountability at each handoff; easy to train ops and support teams |
| Top-3 offer model before acceptance | Balances speed with customer choice; avoids auto-assign backlash |
| 90-second provider response window | Creates urgency without penalizing providers mid-job |
| Manual dispatch fallback at 5 minutes | Prevents abandoned requests in low-density zones during launch |
| T+2 provider payout (standard) | Balances cash flow with dispute window; premium tier gets T+1 |
| 48-hour dispute window | Industry-standard consumer protection without indefinite holds |

---

## Risks

| Risk | Impact | Mitigation |
|------|--------|------------|
| Workflow bottleneck at matching stage | High | Pre-verified provider density; radius expansion rules; manual dispatch SOP |
| Provider status update non-compliance | Medium | Automated reminders; performance score impact; training at onboarding |
| B2B workflow divergence creates ops confusion | Medium | Unified seven-stage framework with documented variations only |
| Payment disputes delay provider payouts | Medium | Clear refund rules; partial hold only on disputed amount |
| Peak demand overwhelms ops monitoring | High | Surge staffing playbook; automated alerts; provider incentive bonuses |

---

## Assumptions

- 85% of jobs complete without human ops intervention
- Average matching time ≤4 minutes in launch zones with 150+ active providers
- Providers will update status reliably when trained and incentivized via performance scores
- B2B partners accept monthly billing cycles with net-30 terms
- Customers accept in-app price revision approval for scope changes

---

## Open Questions

- Should operations team proactively call customers waiting >3 minutes with zero offers?
- Dedicated ops shift coverage for 11 PM–6 AM peak breakdown window?
- Unified workflow for EV-specific rescue (charging truck) or separate sub-flow?
- Maximum concurrent jobs per provider before exclusion from matching?

---

## Next Steps

1. Train launch ops team on seven-stage workflow and escalation triggers
2. Create shift schedule aligned with demand peaks (evenings, weekends, summer)
3. Build provider density dashboard for matching stage monitoring
4. Pilot B2B insurance workflow with one partner before consumer launch
5. Conduct tabletop exercise simulating zero-offer and SLA breach scenarios
