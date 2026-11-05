# Risk Register — Salik Assist

| Field | Value |
|-------|-------|
| **Version** | 1.0 |
| **Status** | Draft |
| **Author** | Product & Strategy Team |
| **Last Updated** | July 4, 2026 |

## Purpose

Maintain a comprehensive register of business risks facing Salik Assist across marketplace operations, commercial, regulatory, competitive, and strategic dimensions—with impact assessments, mitigation plans, and ownership for Series A governance.

## Scope

Business and operational risks. Excludes technical security vulnerabilities, engineering incident response, and IT infrastructure risks (covered in Security documentation).

## Related Documents

- [Assumptions](./Assumptions.md)
- [Constraints](./Constraints.md)
- [Business Rules](./Business-Rules.md)
- [Executive Summary](../01-Executive/Executive-Summary.md)
- [Competitor Analysis](../03-Competitors/Competitor-Analysis.md)

## Table of Contents

1. [Risk Management Framework](#risk-management-framework)
2. [Risk Register Summary](#risk-register-summary)
3. [Marketplace & Operations Risks](#marketplace--operations-risks)
4. [Commercial & Financial Risks](#commercial--financial-risks)
5. [Regulatory & Legal Risks](#regulatory--legal-risks)
6. [Competitive & Strategic Risks](#competitive--strategic-risks)
7. [Partnership & B2B Risks](#partnership--b2b-risks)
8. [Reputational & Trust Risks](#reputational--trust-risks)
9. [Expansion & Growth Risks](#expansion--growth-risks)
10. [Risk Heat Map](#risk-heat-map)
11. [Business Examples](#business-examples)
12. [Business Decisions](#business-decisions)
13. [Assumptions](#assumptions)
14. [Open Questions](#open-questions)
15. [Next Steps](#next-steps)

---

## Risk Management Framework

| Element | Definition |
|---------|------------|
| **Likelihood** | Low (1) / Medium (2) / High (3) |
| **Impact** | Low (1) / Medium (2) / High (3) / Critical (4) |
| **Risk Score** | Likelihood × Impact |
| **Status** | Open / Mitigating / Accepted / Closed |
| **Review cadence** | Monthly leadership review; quarterly board update |

**Risk appetite:** Low tolerance for trust/safety risks; moderate tolerance for commercial experimentation; high tolerance for calculated growth investment.

---

## Risk Register Summary

| ID | Risk | L | I | Score | Owner | Status |
|----|------|---|---|-------|-------|--------|
| R01 | Provider supply shortage at launch | 3 | 4 | 12 | Head of Ops | Mitigating |
| R02 | Low consumer trust in new brand | 3 | 4 | 12 | Head of Marketing | Mitigating |
| R03 | Unverified provider incident | 2 | 4 | 8 | Head of Ops | Mitigating |
| R04 | Regulatory reclassification as transport operator | 2 | 3 | 6 | Legal | Open |
| R05 | Provider commission rejection / churn | 3 | 3 | 9 | Head of Ops | Open |
| R06 | Insurer partnership delays | 3 | 3 | 9 | Head of Partnerships | Open |
| R07 | Incumbent insurer builds competing platform | 2 | 4 | 8 | CEO | Open |
| R08 | CAC exceeds unit economics threshold | 3 | 3 | 9 | Head of Marketing | Open |
| R09 | Seasonal supply-demand imbalance (summer) | 3 | 2 | 6 | Head of Ops | Mitigating |
| R10 | Payment processing or payout failure | 2 | 4 | 8 | CFO | Mitigating |
| R11 | Dispute volume overwhelms operations | 2 | 3 | 6 | Head of Ops | Open |
| R12 | Brand confusion with Salik toll operator | 2 | 2 | 4 | Legal / Marketing | Open |
| R13 | Key person dependency (founding team) | 2 | 3 | 6 | CEO | Open |
| R14 | Premature KSA expansion | 2 | 3 | 6 | CEO | Open |
| R15 | Data privacy regulatory action | 1 | 4 | 4 | Legal | Mitigating |
| R16 | Fraudulent jobs or provider collusion | 2 | 3 | 6 | Head of Ops | Open |
| R17 | Single B2B partner demand concentration | 2 | 3 | 6 | Head of Partnerships | Open |
| R18 | Economic downturn reduces discretionary tow usage | 2 | 2 | 4 | CEO | Accepted |
| R19 | Negative media from surge pricing | 2 | 3 | 6 | Head of Marketing | Open |
| R20 | Provider poaching by competitor with 0% commission | 3 | 2 | 6 | Head of Ops | Open |

---

## Marketplace & Operations Risks

### R01: Provider Supply Shortage at Launch

| Attribute | Detail |
|-----------|--------|
| **Description** | Insufficient verified providers in launch zone to fulfill customer requests |
| **Impact** | Critical — unfilled requests destroy trust irreversibly in emergency category |
| **Likelihood** | High |
| **Mitigation** | Pre-sign 150+ providers; zone gating; launch incentives; zero commission period |
| **Trigger** | Fill rate < 85% for 7 consecutive days |
| **Owner** | Head of Operations |

### R03: Unverified Provider Incident

| Attribute | Detail |
|-----------|--------|
| **Description** | Safety, theft, or fraud incident involving inadequately verified provider |
| **Impact** | Critical — brand damage; legal liability; media crisis |
| **Likelihood** | Medium |
| **Mitigation** | Mandatory verification (Rules 1–6); insurance minimums; auto-suspend on expiry |
| **Trigger** | Any incident involving active provider |
| **Owner** | Head of Operations |

### R09: Seasonal Supply-Demand Imbalance

| Attribute | Detail |
|-----------|--------|
| **Description** | Summer heat causes 300%+ battery request spike; supply cannot match |
| **Impact** | Medium — long ETAs; customer dissatisfaction; surge backlash |
| **Likelihood** | High |
| **Mitigation** | Pre-recruit battery specialists; surge bonuses; demand forecasting |
| **Trigger** | Offer rate drops below 80% during June–August |
| **Owner** | Head of Operations |

### R11: Dispute Volume Overwhelms Operations

| Attribute | Detail |
|-----------|--------|
| **Description** | Dispute rate exceeds 3%; resolution SLA missed |
| **Impact** | Medium — customer trust erosion; ops cost spike |
| **Likelihood** | Medium |
| **Mitigation** | Clear pricing rules; photo evidence; dedicated dispute team |
| **Trigger** | Dispute rate > 3% or resolution > 72 hours |
| **Owner** | Head of Operations |

---

## Commercial & Financial Risks

### R05: Provider Commission Rejection / Churn

| Attribute | Detail |
|-----------|--------|
| **Description** | Providers reject 18% commission after launch promo; mass churn |
| **Impact** | High — supply collapse |
| **Likelihood** | High |
| **Mitigation** | Demonstrate ROI during zero-commission period; tiered rates; volume incentives |
| **Owner** | Head of Operations |

### R08: CAC Exceeds Unit Economics Threshold

| Attribute | Detail |
|-----------|--------|
| **Description** | Customer acquisition cost exceeds $35; payback > 4 jobs |
| **Impact** | High — unsustainable growth; runway burn |
| **Likelihood** | High |
| **Mitigation** | B2B demand channel; referral programs; geo-focused marketing |
| **Owner** | Head of Marketing |

### R10: Payment Processing or Payout Failure

| Attribute | Detail |
|-----------|--------|
| **Description** | Payment provider outage or payout delay beyond 48-hour SLA |
| **Impact** | Critical — provider trust destroyed; supply exodus |
| **Likelihood** | Medium |
| **Mitigation** | Backup payment provider; finance buffer; manual payout contingency |
| **Owner** | CFO |

---

## Regulatory & Legal Risks

### R04: Regulatory Reclassification as Transport Operator

| Attribute | Detail |
|-----------|--------|
| **Description** | UAE authorities classify Salik Assist as transport operator, not marketplace intermediary |
| **Impact** | High — licensing requirements; operational restrictions; cost |
| **Likelihood** | Medium |
| **Mitigation** | Legal review; marketplace terms (Rule 9); providers retain service liability |
| **Owner** | Legal Counsel |

### R15: Data Privacy Regulatory Action

| Attribute | Detail |
|-----------|--------|
| **Description** | Non-compliance with UAE PDPL regarding customer location and personal data |
| **Impact** | Critical — fines; operational suspension |
| **Likelihood** | Low |
| **Mitigation** | Privacy policy; consent flows; DPO appointment; data minimization |
| **Owner** | Legal Counsel |

---

## Competitive & Strategic Risks

### R07: Incumbent Insurer Builds Competing Platform

| Attribute | Detail |
|-----------|--------|
| **Description** | Major insurer develops in-house digital dispatch rather than partner |
| **Impact** | Critical — loss of primary B2B channel |
| **Likelihood** | Medium |
| **Mitigation** | Speed to LOI; demonstrate SLA superiority; multi-insurer strategy |
| **Owner** | CEO |

### R20: Provider Poaching by Competitor

| Attribute | Detail |
|-----------|--------|
| **Description** | Competitor offers 0% commission indefinitely to Salik-signed providers |
| **Impact** | Medium — supply erosion in key zones |
| **Likelihood** | High |
| **Mitigation** | Non-exclusive terms; payment guarantee; reputation tools; volume proof |
| **Owner** | Head of Operations |

---

## Partnership & B2B Risks

### R06: Insurer Partnership Delays

| Attribute | Detail |
|-----------|--------|
| **Description** | B2B sales cycle extends beyond 12 months; no live partner in Year 1 |
| **Impact** | High — CAC remains elevated; B2B revenue delayed |
| **Likelihood** | High |
| **Mitigation** | Parallel B2C launch; multiple insurer pipeline; pilot proposal |
| **Owner** | Head of Partnerships |

### R17: Single B2B Partner Demand Concentration

| Attribute | Detail |
|-----------|--------|
| **Description** | One insurer represents > 40% of job volume; partner churn is existential |
| **Impact** | Medium — revenue cliff |
| **Likelihood** | Medium |
| **Mitigation** | Policy: no partner > 40% of volume; B2C brand building parallel |
| **Owner** | Head of Partnerships |

---

## Reputational & Trust Risks

### R02: Low Consumer Trust in New Brand

| Attribute | Detail |
|-----------|--------|
| **Description** | Motorists default to insurer hotline or informal tow despite Salik marketing |
| **Impact** | Critical — demand side fails to materialize |
| **Likelihood** | High |
| **Mitigation** | Verification badges; insurer co-marketing; money-back guarantee; PR |
| **Owner** | Head of Marketing |

### R12: Brand Confusion with Salik Toll Operator

| Attribute | Detail |
|-----------|--------|
| **Description** | Customers confuse Salik Assist with Salik toll gates; legal challenge from toll operator |
| **Impact** | Medium — brand dilution; legal cost |
| **Likelihood** | Medium |
| **Mitigation** | Trademark review; distinct visual identity; clarifying tagline |
| **Owner** | Legal / Marketing |

### R19: Negative Media from Surge Pricing

| Attribute | Detail |
|-----------|--------|
| **Description** | Customer complaint about surge pricing during heat wave goes viral |
| **Impact** | Medium — brand damage; regulatory scrutiny |
| **Likelihood** | Medium |
| **Mitigation** | Surge cap at 1.5×; pre-accept disclosure; PR preparedness |
| **Owner** | Head of Marketing |

---

## Expansion & Growth Risks

### R13: Key Person Dependency

| Attribute | Detail |
|-----------|--------|
| **Description** | Critical knowledge concentrated in founding team without succession |
| **Impact** | Medium — execution stall if key departure |
| **Likelihood** | Medium |
| **Mitigation** | Document SOPs; hire functional heads; equity retention |
| **Owner** | CEO |

### R14: Premature KSA Expansion

| Attribute | Detail |
|-----------|--------|
| **Description** | KSA launch before UAE profitability; capital drain |
| **Impact** | Medium — runway reduction; divided focus |
| **Likelihood** | Medium |
| **Mitigation** | Milestone gates: UAE contribution breakeven before KSA office |
| **Owner** | CEO |

---

## Risk Heat Map

```
IMPACT →     Low (1)      Medium (2)     High (3)      Critical (4)
LIKELIHOOD ↓
High (3)                  R09,R20        R05,R08       R01,R02
Medium (2)   R12          R11,R16,R19    R04,R06,R07   R03,R10
                           R13,R14,R17
Low (1)                   R18            R15
```

**Top 5 risks by score:** R01, R02, R05, R08, R06 — all require active mitigation before and through launch.

---

## Business Examples

**Example 1 — R01 materialization:** Launch week: 200 requests, 72% fill rate. Ops triggers contingency: expand offer radius, activate 10 standby providers, pause marketing in underserved zone. Fill rate recovers to 88% within 5 days.

**Example 2 — R03 near-miss:** Provider insurance expires; system auto-suspends before next job. Provider renews within 48 hours. Zero customer exposure. Verification monitoring validated.

**Example 3 — R19 management:** Customer tweets about AED 130 battery jump during surge. Marketing responds within 2 hours with surge policy explanation, offers credit. Story does not escalate. Surge cap and disclosure rules reaffirmed.

---

## Business Decisions

| Decision | Rationale |
|----------|-----------|
| Zero tolerance for trust risks (R02, R03) | Emergency category; one incident is fatal |
| Accept economic downturn risk (R18) | Roadside is necessity; low mitigation ROI |
| Milestone-gate KSA expansion (R14) | Capital preservation |
| No single partner > 40% volume (R17) | Demand concentration risk |
| Monthly risk review mandatory | Marketplace dynamics shift rapidly |

---

## Assumptions

- 20 identified risks cover primary Series A diligence concerns
- Risk of Operations can monitor R01 and R09 with weekly fill rate dashboard
- Legal counsel engaged for R04 and R15 before launch
- Dispute fund capitalized for R11 mitigation
- Risk scores valid for UAE launch context; KSA re-assessment required

---

## Open Questions

- Insurance policy for platform liability (R03)—covered?
- Risk appetite for exclusive insurer deal vs. R17 concentration?
- Board-level risk committee at Series A close?
- Crisis communication plan owner for R19?
- Threshold for pausing launch if R01 trigger hit?

---

## Next Steps

1. Assign risk owners and confirm accountability
2. Legal review for R04, R12, R15 before launch
3. Establish weekly fill rate and dispute rate monitoring (R01, R11)
4. Capitalize dispute fund and payment contingency (R10, R11)
5. Present top 10 risks in Series A data room
6. Schedule monthly risk review starting launch month
