# Business Requirements — Salik Assist

| Field | Value |
|-------|-------|
| **Version** | 1.0 |
| **Status** | Draft |
| **Author** | Product & Strategy Team |
| **Last Updated** | July 4, 2026 |

## Purpose

Define the high-level business requirements Salik Assist must satisfy to launch and scale as a roadside assistance marketplace in the GCC, serving as the authoritative reference for stakeholders evaluating scope, investment, and operational readiness.

## Scope

Business capabilities, outcomes, and constraints. Excludes functional specifications, user stories, acceptance criteria, and technical design.

## Related Documents

- [Business Rules](./Business-Rules.md)
- [Business Model Canvas](./Business-Model-Canvas.md)
- [Value Proposition](./Value-Proposition.md)
- [Constraints](./Constraints.md)
- [Assumptions](./Assumptions.md)
- [MVP](../09-Roadmap/MVP.md)

## Table of Contents

1. [Requirements Overview](#requirements-overview)
2. [Customer (Demand) Requirements](#customer-demand-requirements)
3. [Provider (Supply) Requirements](#provider-supply-requirements)
4. [Marketplace Operations Requirements](#marketplace-operations-requirements)
5. [B2B Partner Requirements](#b2b-partner-requirements)
6. [Financial & Commercial Requirements](#financial--commercial-requirements)
7. [Compliance & Trust Requirements](#compliance--trust-requirements)
8. [Growth & Expansion Requirements](#growth--expansion-requirements)
9. [Requirements Traceability Matrix](#requirements-traceability-matrix)
10. [Business Examples](#business-examples)
11. [Business Decisions](#business-decisions)
12. [Risks](#risks)
13. [Assumptions](#assumptions)
14. [Open Questions](#open-questions)
15. [Next Steps](#next-steps)

---

## Requirements Overview

Business requirements are categorized by stakeholder and prioritized:

| Priority | Definition |
|----------|------------|
| **P0 — Launch critical** | Must be satisfied before public consumer launch |
| **P1 — Scale critical** | Required within 6 months of launch |
| **P2 — Growth** | Required for Year 2 expansion |

---

## Customer (Demand) Requirements

| ID | Requirement | Priority | Success Measure |
|----|-------------|----------|-----------------|
| BR-C01 | Customer can request roadside help in under 60 seconds with location, vehicle, and issue type | P0 | 95% requests submitted < 60 sec |
| BR-C02 | Customer receives up to 3 provider offers within 5 minutes of request | P0 | 90% requests get ≥1 offer in 5 min |
| BR-C03 | Customer can compare offers by ETA, price estimate, rating, and credentials | P0 | Offer comparison available on 100% of multi-offer requests |
| BR-C04 | Customer can track provider en route after accepting an offer | P0 | Tracking active from accept to arrival |
| BR-C05 | Customer can pay digitally upon service completion | P0 | 85%+ jobs paid in-app |
| BR-C06 | Customer can rate and review provider after job completion | P0 | 70%+ completion rate on ratings |
| BR-C07 | Customer can access support for disputes within 24 hours | P0 | Support ticket response < 4 hours |
| BR-C08 | Customer experience available in Arabic and English | P0 | Full parity in both languages |
| BR-C09 | Customer can request multiple service categories (tow, battery, tire, fuel, mechanic) | P1 | 4+ categories live |
| BR-C10 | Customer can share live trip status with a contact for safety | P1 | Share link available on active jobs |
| BR-C11 | Customer receives upfront coverage indication before submitting request | P1 | Zone map visible pre-request |
| BR-C12 | Customer can access service history and digital receipts | P2 | 12-month history retained |

---

## Provider (Supply) Requirements

| ID | Requirement | Priority | Success Measure |
|----|-------------|----------|-----------------|
| BR-P01 | Provider must complete verification before receiving job offers | P0 | 0 unverified providers active |
| BR-P02 | Provider can accept or decline incoming job offers | P0 | 100% offers require explicit accept |
| BR-P03 | Provider receives guaranteed payout within 48 hours of job completion | P0 | 98%+ payouts within SLA |
| BR-P04 | Provider can set availability and service zone | P0 | Availability controls functional |
| BR-P05 | Provider can view job history and earnings statements | P0 | Monthly statements available |
| BR-P06 | Provider can build and maintain a public rating profile | P0 | Ratings visible on offers |
| BR-P07 | Provider retains business independence (non-exclusive) | P0 | No exclusivity clause enforced |
| BR-P08 | Provider can access bilingual support for operational issues | P0 | Arabic/English support available |
| BR-P09 | Provider can receive surge incentive bonuses during peak demand | P1 | Surge bonuses active in peak windows |
| BR-P10 | Provider can subscribe to premium tier for enhanced visibility | P2 | Subscription tier available |
| BR-P11 | Provider can manage multiple vehicles/drivers under one account | P2 | Multi-vehicle accounts supported |

---

## Marketplace Operations Requirements

| ID | Requirement | Priority | Success Measure |
|----|-------------|----------|-----------------|
| BR-M01 | Platform matches requests to nearest qualified available providers | P0 | Median match time < 90 sec |
| BR-M02 | Platform enforces top-3 offer presentation before auto-expiry | P0 | 100% eligible requests get offer round |
| BR-M03 | Platform records full job lifecycle audit trail | P0 | 100% jobs have timestamped states |
| BR-M04 | Platform mediates customer-provider disputes | P0 | Dispute resolution process documented |
| BR-M05 | Platform maintains minimum provider density per launch zone | P0 | ≥150 providers in launch zone |
| BR-M06 | Platform supports surge pricing during validated peak demand | P1 | Surge rules active with caps |
| BR-M07 | Platform provides operations dashboard for fill rate and SLA monitoring | P1 | Real-time ops metrics available |
| BR-M08 | Platform gates service availability by geographic zone | P0 | Out-of-zone requests blocked with message |
| BR-M09 | Platform supports cancellation policies with defined fee rules | P0 | Cancellation rules enforced per [Business Rules](./Business-Rules.md) |
| BR-M10 | Platform generates monthly marketplace health reports for leadership | P1 | Monthly report automated |

---

## B2B Partner Requirements

| ID | Requirement | Priority | Success Measure |
|----|-------------|----------|-----------------|
| BR-B01 | Insurer can route policyholder requests through Salik network | P1 | ≥1 insurer LOI operational |
| BR-B02 | Partner receives SLA reporting dashboard (ETA, completion, CSAT) | P1 | Dashboard live for signed partners |
| BR-B03 | Partner can apply pre-negotiated rate cards by zone and category | P1 | Rate cards configurable per contract |
| BR-B04 | Fleet operator can dispatch via dedicated account with multi-vehicle support | P2 | Fleet account type available |
| BR-B05 | Partner co-branding visible in policyholder customer journey | P1 | Co-brand option per contract |
| BR-B06 | Partner billing supports monthly invoicing with job-level detail | P1 | Invoice format agreed with first partner |

---

## Financial & Commercial Requirements

| ID | Requirement | Priority | Success Measure |
|----|-------------|----------|-----------------|
| BR-F01 | Platform collects commission on completed jobs automatically | P0 | 100% completed jobs commission captured |
| BR-F02 | Platform supports AED and major GCC currencies | P0 | AED primary; SAR readiness for KSA |
| BR-F03 | Platform maintains dispute resolution fund for customer guarantees | P0 | Fund capitalized per finance plan |
| BR-F04 | Platform provides provider tax-ready earnings documentation | P1 | Annual statements available |
| BR-F05 | Platform supports promotional credits and referral incentives | P1 | Promo engine operational |
| BR-F06 | Platform achieves target unit economics by Month 22–26 | P1 | Contribution margin positive UAE |

---

## Compliance & Trust Requirements

| ID | Requirement | Priority | Success Measure |
|----|-------------|----------|-----------------|
| BR-T01 | All active providers verified for trade license, insurance, and identity | P0 | 100% verification compliance |
| BR-T02 | Platform terms classify Salik as intermediary, not service provider | P0 | Legal sign-off on terms |
| BR-T03 | Customer data handled per UAE PDPL requirements | P0 | Privacy policy and consent flows live |
| BR-T04 | Platform maintains insurance certificate expiry monitoring for providers | P0 | Auto-suspend on expired insurance |
| BR-T05 | Platform supports regulatory audit requests with job records | P1 | Audit export capability |
| BR-T06 | Background checks completed for all provider drivers | P0 | 100% driver checks before activation |

---

## Growth & Expansion Requirements

| ID | Requirement | Priority | Success Measure |
|----|-------------|----------|-----------------|
| BR-G01 | Launch in Dubai metro and key highway corridors | P0 | Launch zone live |
| BR-G02 | Expand to Abu Dhabi and Sharjah within 12 months | P1 | 3 emirates operational |
| BR-G03 | Achieve 85,000 completed jobs in Year 1 | P0 | Year 1 job target |
| BR-G04 | KSA market entry readiness assessment by Month 12 | P2 | KSA expansion plan approved |
| BR-G05 | Provider network scales to 500+ verified across UAE by Year 2 | P1 | Provider count target |

---

## Requirements Traceability Matrix

| Business Requirement | Business Rule(s) | Success Metric |
|---------------------|------------------|----------------|
| BR-C02 (top-3 offers) | Rule 12, 13, 14 | Offer rate in 5 min |
| BR-P01 (verification) | Rule 1, 2, 3, 4 | Zero unverified active |
| BR-P03 (payout SLA) | Rule 28, 29 | 48-hour payout compliance |
| BR-M09 (cancellation) | Rule 20, 21, 22 | Cancellation fee accuracy |
| BR-T01 (verification) | Rule 1–6 | Verification audit pass |
| BR-F01 (commission) | Rule 25, 26 | Commission capture rate |

---

## Business Examples

**Example 1 — BR-C02 in practice:** Customer submits flat tire request at Dubai Marina. Within 4 minutes, three tire service providers submit offers with ETAs of 15, 22, and 28 minutes and price bands of AED 120–150, AED 140–170, and AED 100–130. Requirement satisfied.

**Example 2 — BR-P01 gate:** New tow operator uploads documents but insurance certificate expires in 3 days. System flags expiry; operator cannot go live until renewal uploaded and verified. Requirement satisfied.

**Example 3 — BR-B02 partner value:** Insurer partner logs into portal, sees 94% jobs completed within 45 minutes, average CSAT 4.6, and 2% dispute rate for the month. Renews annual dispatch contract.

---

## Business Decisions

| Decision | Rationale |
|----------|-----------|
| P0 requirements are non-negotiable for launch | Investor and customer trust depend on core marketplace loop |
| B2B requirements at P1, not P0 | Consumer marketplace must work before partner volume scales |
| Verification requirements cannot be deferred | One unverified incident destroys brand in emergency category |
| Top-3 offer requirement is P0 | Core differentiation vs. all alternatives |
| Multi-category at P1 allows tow+battery anchor at launch | Focus supply recruitment; expand categories Month 4–6 |

---

## Risks

| Risk | Impact | Mitigation |
|------|--------|------------|
| P0 scope too large for launch date | High | MVP zone gating; phased category rollout |
| Requirements conflict between B2B and B2C | Medium | Partner requirements as configurable overlays |
| Provider payout SLA unachievable at scale | High | Payment partner SLA; finance buffer |
| Verification throughput bottleneck | Medium | Dedicated verification team; batch processing |

---

## Assumptions

- 42 business requirements sufficient for Series A diligence scope
- P0 set can be satisfied within 6-month pre-launch window
- Business rules (separate document) enforce operational requirements
- Stakeholders accept P1 deferral for non-critical B2B features
- Year 1 job target of 85,000 requires 150+ active providers

---

## Open Questions

- Should BR-C10 (share trip) be elevated to P0 for women-driver segment?
- Minimum provider count per zone—fixed at 150 total or density-based?
- Which B2B requirement is the gating item for first insurer LOI?
- Are desert recovery requirements in scope for Year 1 or deferred?
- Who owns requirements traceability updates as rules change?

---

## Next Steps

1. Review P0 requirements with Operations and Legal for feasibility sign-off
2. Map each P0 requirement to MVP milestone in roadmap
3. Establish monthly requirements compliance review at leadership level
4. Link requirements to [Success Metrics](../01-Executive/Success-Metrics.md)
5. Validate B2B P1 set with top 3 insurer prospects
