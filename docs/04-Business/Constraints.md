# Constraints — Salik Assist

| Field | Value |
|-------|-------|
| **Version** | 1.0 |
| **Status** | Draft |
| **Author** | Product & Strategy Team |
| **Last Updated** | July 4, 2026 |

## Purpose

Define the business, regulatory, financial, operational, and strategic constraints that bound Salik Assist's decisions and scope—ensuring plans remain realistic and compliant throughout Series A execution.

## Scope

Non-technical constraints on business operations, market entry, partnerships, and growth. Excludes technical system constraints, engineering limitations, and infrastructure capacity.

## Related Documents

- [Assumptions](./Assumptions.md)
- [Business Rules](./Business-Rules.md)
- [Business Requirements](./Business-Requirements.md)
- [Risk Register](./Risk-Register.md)
- [Cost Structure](./Cost-Structure.md)

## Table of Contents

1. [Constraints Overview](#constraints-overview)
2. [Regulatory & Legal Constraints](#regulatory--legal-constraints)
3. [Financial & Funding Constraints](#financial--funding-constraints)
4. [Operational Constraints](#operational-constraints)
5. [Market & Geographic Constraints](#market--geographic-constraints)
6. [Partnership Constraints](#partnership-constraints)
7. [Brand & Strategic Constraints](#brand--strategic-constraints)
8. [Provider & Supply Constraints](#provider--supply-constraints)
9. [Customer & Demand Constraints](#customer--demand-constraints)
10. [Constraint Impact Matrix](#constraint-impact-matrix)
11. [Business Examples](#business-examples)
12. [Business Decisions](#business-decisions)
13. [Risks](#risks)
14. [Assumptions](#assumptions)
15. [Open Questions](#open-questions)
16. [Next Steps](#next-steps)

---

## Constraints Overview

Constraints are **hard boundaries** that cannot be violated without explicit leadership exception and documented rationale. They differ from assumptions (beliefs about the future) and risks (uncertain events).

| Type | Count | Flexibility |
|------|-------|-------------|
| Regulatory & Legal | 8 | None without legal approval |
| Financial & Funding | 6 | Board approval required to override |
| Operational | 7 | Ops leadership may adjust within bounds |
| Market & Geographic | 5 | Leadership approval for exceptions |
| Partnership | 4 | Partnerships + Legal approval |
| Brand & Strategic | 5 | CEO approval required |
| Provider & Supply | 4 | Operations enforcement |
| Customer & Demand | 3 | Product + Marketing alignment |

---

## Regulatory & Legal Constraints

| ID | Constraint | Source | Impact |
|----|------------|--------|--------|
| RL01 | Salik Assist operates as marketplace intermediary, not transport operator or employer of providers | UAE commercial law; platform terms | Providers retain service liability; no fleet ownership |
| RL02 | All providers must hold valid UAE trade license and commercial insurance before activation | Business Rules 1–3; UAE regulations | Verification mandatory; no exceptions |
| RL03 | Customer and provider personal data handled per UAE PDPL | Federal Decree-Law No. 45 of 2021 | Consent flows; data minimization; DPO required |
| RL04 | Background checks required for all provider drivers | Business Rule 4; best practice | No driver active without completed check |
| RL05 | Platform terms must clearly disclaim Salik Assist as service provider | Legal counsel | Customer contracts with provider, facilitated by platform |
| RL06 | Surge pricing capped at 1.5× base rate | Business Rule 31; consumer protection | Cannot exceed cap even during extreme demand |
| RL07 | Cash payment not supported on-platform | Business Rule 49 | Digital payment only for audit trail and dispute resolution |
| RL08 | B2B partner contracts must comply with UAE insurance distribution regulations | Insurance authority | Legal review on all insurer agreements |

---

## Financial & Funding Constraints

| ID | Constraint | Source | Impact |
|----|------------|--------|--------|
| FC01 | Series A budget: $6M–$8M target; 24-month runway minimum | Board/investor terms | Limits hiring, marketing, and expansion pace |
| FC02 | Year 1 OpEx ceiling: ~$3.0M without board approval for overrun | Financial plan | Hiring and marketing gated to plan |
| FC03 | Promotional spend capped at 8% of Year 1 gross revenue | Marketing budget | Limits launch discount depth |
| FC04 | Dispute fund must be capitalized before consumer launch | Risk mitigation; finance policy | Minimum AED 250K reserve |
| FC05 | Provider payout SLA of 48 hours is non-negotiable | Business Rule 47; provider value prop | Finance must maintain payout liquidity |
| FC06 | KSA expansion budget not allocated until UAE contribution margin positive | Board strategy | No KSA office before Month 18–22 |

---

## Operational Constraints

| ID | Constraint | Source | Impact |
|----|------------|--------|--------|
| OC01 | No unverified provider may receive or accept job offers | Business Rules 1, 5 | Verification throughput limits supply ramp |
| OC02 | Top-3 competitive offer model mandatory for standard B2C flows | Business Rules 20–27; positioning | Cannot auto-assign without customer choice |
| OC03 | Launch limited to defined Dubai zones until 150+ verified providers signed | Launch plan | Marketing geo-gated; out-of-zone requests rejected |
| OC04 | Dispute resolution SLA: acknowledge within 4 hours; resolve within 72 hours | Business Rules 56–57 | Staffing minimum for support team |
| OC05 | Final price cannot exceed estimate upper bound by > 15% without customer approval | Business Rule 30 | Provider pricing discipline enforced |
| OC06 | Operations coverage: 16/7 at launch (06:00–22:00 GST, 7 days) | Staffing plan | No 24/7 human support at launch |
| OC07 | Maximum 2 active (uncompleted) requests per customer at any time | Business Rule 17 | Prevents system abuse |

---

## Market & Geographic Constraints

| ID | Constraint | Source | Impact |
|----|------------|--------|--------|
| MG01 | UAE launch before any KSA market entry | Expansion strategy | All Year 1 focus on UAE |
| MG02 | MVP service categories limited to: tow, battery, tire, fuel, mobile mechanic | Launch scope | Desert recovery and EV deferred |
| MG03 | Launch geography: Dubai metro + key highway corridors only | Go-to-market plan | Abu Dhabi/Sharjah Month 7+ |
| MG04 | Provider rate guardrails enforced per [Pricing Strategy](./Pricing-Strategy.md) | Marketplace fairness | Providers cannot price outside min/max |
| MG05 | Cross-emirate long-distance tows require provider opt-in | Business Rule 69 | Not all providers serve all routes |

---

## Partnership Constraints

| ID | Constraint | Source | Impact |
|----|------------|--------|--------|
| PC01 | No single B2B partner may exceed 40% of total job volume | Risk mitigation (R17) | Demand diversification enforced |
| PC02 | Provider accounts are non-exclusive; no exclusivity clauses at launch | Business Rule 10 | Cannot lock providers to Salik only |
| PC03 | B2B partner contracts require Legal review before signature | Legal policy | Partnership cycle minimum 4 weeks |
| PC04 | Co-branding must include Salik Assist verification badges | Trust policy | Partner brand cannot replace verification |

---

## Brand & Strategic Constraints

| ID | Constraint | Source | Impact |
|----|------------|--------|--------|
| BS01 | Salik Assist will not own, lease, or operate tow trucks or service vehicles | Marketplace model | Asset-light; no fleet CapEx |
| BS02 | Salik Assist will not underwrite insurance or act as insurer | Regulatory; business model | B2B2C dispatch only; no risk bearing |
| BS03 | Salik Assist will not compete on "cheapest tow" positioning | Brand strategy | Marketing guardrails |
| BS04 | Commission on completed jobs is primary revenue; no customer subscription fee at launch | Revenue model | B2C pricing structure fixed at launch |
| BS05 | Brand must not imply affiliation with Salik toll gate operator | Legal/trademark | Distinct identity required in customer-facing materials |

---

## Provider & Supply Constraints

| ID | Constraint | Source | Impact |
|----|------------|--------|--------|
| PS01 | Standard B2C commission: 18% (after 30-day zero-commission launch promo) | Business Rule 46 | Provider economics bounded |
| PS02 | Provider minimum rating: 3.5 stars (90-day rolling) to remain active | Business Rules 7–8 | Quality floor enforced |
| PS03 | Provider insurance minimum: AED 1,000,000 third-party liability | Business Rule 3 | Smaller operators must meet threshold |
| PS04 | Provider must respond to offers within 3 minutes during available hours | Business Rule 12 | Availability standards enforced |

---

## Customer & Demand Constraints

| ID | Constraint | Source | Impact |
|----|------------|--------|--------|
| CD01 | Customers must be 18+ to create account | Business Rule 15 | Age gate in registration |
| CD02 | Maximum 3 unresolved payment disputes or chargebacks in 12 months before account restriction | Business Rule 18 | Fraud/abuse prevention |
| CD03 | Customer cancellation fees apply per Business Rules 41–43 | Cancellation policy | No free cancellation after provider en route |

---

## Constraint Impact Matrix

| Constraint | Launch Impact | Scale Impact | Override Authority |
|------------|---------------|--------------|-------------------|
| RL01 (intermediary only) | Defines model | Permanent | None (structural) |
| OC03 (zone gating) | High | Decreases over time | CEO |
| FC06 (KSA gate) | None | High (delays KSA) | Board |
| OC02 (top-3 offers) | Defines UX | Permanent | CEO + Board |
| PS01 (18% commission) | Provider recruitment | Permanent | CEO (with finance review) |
| PC01 (40% partner cap) | Low initially | High at B2B scale | Board |
| BS01 (no fleet) | Enables launch | Permanent | Board (strategic pivot) |

---

## Business Examples

**Example 1 — OC03 zone gating:** Customer in Ajman requests tow. Ajman outside launch zone. App displays: "Salik Assist is coming to your area soon. Currently serving Dubai metro." Request blocked. Constraint honored; no bad experience from unfilled request.

**Example 2 — RL06 surge cap:** Extreme heat wave; demand 4× supply. Operations requests surge cap increase to 2.0×. Leadership denies—Rule 31 and RL06 are hard constraints. Surge stays at 1.5×; provider bonuses activated instead.

**Example 3 — PC01 partner cap:** Insurer A reaches 38% of volume. Partnerships team slows Insurer A marketing expansion and accelerates Insurer B pipeline to maintain diversification before Insurer A hits 40% ceiling.

---

## Business Decisions

| Decision | Rationale |
|----------|-----------|
| Constraints documented separately from rules and requirements | Rules = how; Constraints = boundaries; Requirements = what |
| Regulatory constraints have zero flexibility | Legal exposure unacceptable |
| No fleet constraint is structural, not temporary | Defines entire business model |
| Top-3 offer constraint protects core differentiation | Cannot compromise for operational convenience |
| 40% partner cap prevents demand concentration | Constraint derived from risk register |

---

## Risks

| Risk | Impact | Mitigation |
|------|--------|------------|
| Constraints too restrictive for competitive response | Medium | Quarterly constraint review with CEO |
| Team unaware of constraints; accidental violation | High | Onboarding training; ops playbook |
| Regulatory constraint changes (new license required) | High | Legal monitoring; government relations |
| Financial constraints force premature monetization | Medium | Board alignment on investment period |
| Zone gating frustrates customers; bad reviews | Medium | Clear messaging; expansion timeline published |

---

## Assumptions

- 50 documented constraints cover primary operational and strategic boundaries
- Constraints remain stable through Year 1; major review at Series A close
- Leadership will enforce constraints even under competitive pressure
- Regulatory constraints (RL01–RL08) validated by legal counsel before launch
- Constraint violations require documented exception with approval trail

---

## Open Questions

- Should OC06 (16/7 support) upgrade to 24/7 before Month 6?
- Exception process formalization: who approves constraint overrides?
- Are RL08 insurance distribution rules fully understood for B2B2C?
- Should PS01 commission constraint include category-specific tiers?
- Publish customer-facing summary of key constraints (cancellation, surge)?

---

## Next Steps

1. Legal sign-off on regulatory constraints (RL01–RL08)
2. Include constraints in provider onboarding and terms of service
3. Train operations team on non-negotiable constraints (OC01, OC02, OC05)
4. Board acknowledgment of financial constraints (FC01–FC06)
5. Quarterly constraint review scheduled in leadership calendar
6. Cross-reference constraints with [Business Rules](./Business-Rules.md) for consistency
