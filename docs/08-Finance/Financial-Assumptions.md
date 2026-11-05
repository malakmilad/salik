# Financial Assumptions — Salik Assist

| Field | Value |
|-------|-------|
| **Version** | 1.0 |
| **Status** | Draft |
| **Author** | Product & Strategy Team |
| **Last Updated** | July 4, 2026 |

## Purpose

Document all key financial assumptions underlying Salik Assist revenue forecasts, unit economics, and CAC/LTV models—enabling auditability, scenario planning, and investor diligence.

## Scope

Business and operational assumptions for UAE launch and GCC expansion planning. Excludes technical infrastructure cost assumptions and detailed headcount plans.

## Related Documents

- [Revenue Forecast](./Revenue-Forecast.md)
- [Unit Economics](./Unit-Economics.md)
- [CAC-LTV](./CAC-LTV.md)
- [Executive Summary](../01-Executive/Executive-Summary.md)
- [MVP](../09-Roadmap/MVP.md)

## Table of Contents

1. [Assumption Categories](#assumption-categories)
2. [Market & Demand Assumptions](#market--demand-assumptions)
3. [Pricing & Revenue Assumptions](#pricing--revenue-assumptions)
4. [Cost Assumptions](#cost-assumptions)
5. [Customer Assumptions](#customer-assumptions)
6. [Provider Assumptions](#provider-assumptions)
7. [Operational Assumptions](#operational-assumptions)
8. [Expansion Assumptions](#expansion-assumptions)
9. [Macro & Regulatory Assumptions](#macro--regulatory-assumptions)
10. [Assumption Validation Plan](#assumption-validation-plan)
11. [Business Examples](#business-examples)
12. [Business Decisions](#business-decisions)
13. [Risks](#risks)
14. [Assumptions](#assumptions)
15. [Open Questions](#open-questions)
16. [Next Steps](#next-steps)

---

## Assumption Categories

| Category | # Assumptions | Confidence | Impact if Wrong |
|----------|---------------|------------|-----------------|
| Market & demand | 12 | Medium | High |
| Pricing & revenue | 10 | Medium-High | High |
| Cost | 8 | Medium | Medium |
| Customer | 9 | Medium | High |
| Provider | 11 | Medium | High |
| Operational | 7 | Medium-High | Medium |
| Expansion | 6 | Low-Medium | Medium |
| Macro & regulatory | 5 | High | Medium |

---

## Market & Demand Assumptions

| # | Assumption | Value | Source/Rationale |
|---|------------|-------|------------------|
| M1 | UAE registered vehicles (Dubai focus) | ~1.8M in Dubai; ~4.5M UAE | RTA/public data |
| M2 | Annual breakdown/incident rate per vehicle | 0.8–1.2 events/year | Industry estimate; climate factor |
| M3 | Digitally addressable share | 15% Year 1 → 30% Year 3 | Mobile adoption; competitor benchmark |
| M4 | Salik Assist market share (Dubai) | 3% Y1 → 12% Y3 | Launch density + marketing |
| M5 | Seasonal peak (summer: May–Sep) | +35% job volume vs. winter | Battery/tire failure data |
| M6 | Highway vs. urban job split | 40% highway / 60% urban | Geography and corridor launch |
| M7 | Serviceable market (SAM) UAE | AED 660M–880M ($180–240M) | Bottom-up from M1–M4 |
| M8 | KSA market multiplier vs. UAE | 3.5× | Vehicle population; geography |
| M9 | Competitor market share (combined) | 8% digital at launch | Fragmented incumbents |
| M10 | Insurance roadside market digitization | 10% Y1 → 40% Y3 | B2B partnership trend |
| M11 | Tourism/expat breakdown share | 15% of Dubai jobs | Expat population; rental cars |
| M12 | EV breakdown rate (Phase 2+) | 5% of jobs by Year 3 | EV adoption curve UAE |

---

## Pricing & Revenue Assumptions

| # | Assumption | Value | Source/Rationale |
|---|------------|-------|------------------|
| P1 | Average job value (blended UAE) | AED 181 Y1 → AED 197 Y3 | Category mix modeling |
| P2 | Tow AOV | AED 280 | Market rate survey |
| P3 | Battery AOV | AED 150 | Market rate survey |
| P4 | Standard commission rate | 18% | Competitor benchmark; provider interviews |
| P5 | B2B commission rate | 12% | Volume discount standard |
| P6 | Launch zero-commission period | 20 jobs/provider; 60 days | Provider acquisition strategy |
| P7 | Surge multiplier cap | 2.5× base | Customer protection; SLA alignment |
| P8 | Provider subscription adoption | 8% Y1 → 15% Y3 | Optional tier; home services benchmark |
| P9 | VAT rate | 5% | UAE standard |
| P10 | AED/USD exchange rate | 3.67 (fixed peg) | Currency peg |

---

## Cost Assumptions

| # | Assumption | Value | Source/Rationale |
|---|------------|-------|------------------|
| C1 | Payment processing fee | 2.9% + AED 1.00/transaction | Acquirer quote estimate |
| C2 | Support cost per contact | AED 3.50 | Agent cost ÷ contacts/job |
| C3 | SLA remedy reserve | 1.0% of GMV | Policy modeling |
| C4 | Year 1 monthly fixed costs | AED 575,000 | Headcount + office + admin plan |
| C5 | Fixed cost growth YoY | 15% | Team scaling plan |
| C6 | Gross margin target | 72% Y1 → 82% Y3 | Variable cost efficiency |
| C7 | Marketing budget Year 1 | AED 1.8M | CAC model |
| C8 | Provider verification cost | AED 350/provider (amortized) | Onboarding team cost |

---

## Customer Assumptions

| # | Assumption | Value | Source/Rationale |
|---|------------|-------|------------------|
| CU1 | Blended CAC Year 1 | AED 44–75 | Channel mix model |
| CU2 | New customer rate (% of jobs) | 47% Y1 → 30% Y3 | Repeat rate growth |
| CU3 | Customer repeat rate (D365) | 15% Y1 → 35% Y3 | Low-frequency category |
| CU4 | Lifetime jobs per customer | 1.4 Y1 → 2.5 Y3 | Repeat + subscription |
| CU5 | Guest checkout rate | 60% of first-time users | Emergency context |
| CU6 | Guest-to-registered conversion | 40% Y1 → 55% Y3 | Post-job prompts |
| CU7 | First-job NPS | ≥40 | Quality target |
| CU8 | Subscription adoption (Phase 2) | 5% Y1 end → 12% Y3 | Preparedness product |
| CU9 | Referral rate (post first job) | 8% Y1 → 12% Y3 | Referral program |

---

## Provider Assumptions

| # | Assumption | Value | Source/Rationale |
|---|------------|-------|------------------|
| PR1 | Launch provider count | 150 verified | Field sales pipeline |
| PR2 | Year 1 end provider count | 350 active | Onboarding capacity |
| PR3 | Jobs per provider per day | 1.5 Y1 → 2.4 Y3 | Utilization modeling |
| PR4 | Provider acceptance rate | 65% Y1 → 75% Y3 | Training + incentives |
| PR5 | Provider churn (annual) | 25% Y1 → 15% Y3 | Marketplace benchmark |
| PR6 | Provider commission acceptance | 70% accept 18% | Field interview (n=30) |
| PR7 | Average provider fleet size | 2.1 vehicles | Market structure |
| PR8 | Provider onboarding time | 5–10 business days | Process design |
| PR9 | Provider rating average | 4.3 platform-wide | Quality target |
| PR10 | Zero-commission promo utilization | 85% of new providers | Incentive tracking |
| PR11 | B2B pool opt-in rate | 60% of active providers | B2B rate preference |

---

## Operational Assumptions

| # | Assumption | Value | Source/Rationale |
|---|------------|-------|------------------|
| O1 | Job completion rate | 92% Y1 → 97% Y3 | SLA + quality investment |
| O2 | Time to first offer (P90) | ≤5 minutes | Matching model |
| O3 | No-show rate | <2% Y1 → <0.5% Y3 | Performance management |
| O4 | Support contact rate | 12% of jobs | Industry benchmark |
| O5 | Platform availability | 99.0% Y1 → 99.5% Y3 | Uptime target |
| O6 | Break-even month | 22–26 | Fixed cost ÷ contribution margin |
| O7 | Insurance B2B pilot live | Month 6 | Partnerships timeline |

---

## Expansion Assumptions

| # | Assumption | Value | Source/Rationale |
|---|------------|-------|------------------|
| E1 | Abu Dhabi launch | Month 10 (Phase 1) | Roadmap |
| E2 | Sharjah launch | Month 14 (Phase 1) | Roadmap |
| E3 | KSA Riyadh launch | Month 25 (Phase 3) | Post-UAE validation |
| E4 | KSA AOV premium vs. UAE | +15% | Distance/coverage |
| E5 | Expansion CAC premium | +20% vs. UAE | New market learning |
| E6 | Local entity setup time (KSA) | 4–6 months | Legal estimate |

---

## Macro & Regulatory Assumptions

| # | Assumption | Value | Source/Rationale |
|---|------------|-------|------------------|
| R1 | UAE GDP growth | 3–4% annually | IMF forecast |
| R2 | No adverse marketplace reclassification | Intermediary status maintained | Legal opinion (pending) |
| R3 | PDPL compliance achievable at launch | No material cost overrun | Privacy program |
| R4 | Fuel prices stable (±15%) | AED 3.0/liter avg | MOEI data |
| R5 | No pandemic-scale mobility disruption | Normal operations | Base case |

---

## Assumption Validation Plan

| Assumption | Validation Method | Timeline | Owner |
|------------|-------------------|----------|-------|
| P4 (18% commission acceptance) | Provider pipeline survey (n=100) | Pre-launch | Field sales |
| M4 (market share) | Launch month tracking vs. estimate | Month 1–3 | Growth |
| CU1 (CAC) | Channel tracking from Day 1 | Ongoing | Marketing |
| PR3 (jobs/provider/day) | Provider dashboard | Month 2+ | Ops |
| O1 (completion rate) | Platform metrics | Launch+ | Ops |
| P1 (AOV) | Transaction data | Month 1+ | Finance |
| CU3 (repeat rate) | Cohort analysis | Month 6+ | Growth |

**Review cadence:** Assumptions reviewed monthly for first 6 months; quarterly thereafter. Material deviations (>20%) trigger forecast revision.

---

## Business Examples

**Example 1 — AOV assumption test:** Assume tow AOV is AED 240 not AED 280 (−14%). Year 1 GMV drops from AED 15.4M to AED 13.2M. Revenue drops ~AED 400K. **Sensitivity: moderate.** Mitigation: category mix shift toward battery/tire.

**Example 2 — Provider density assumption:** Assume 100 providers at launch not 150. Jobs/provider/day must be 2.1 not 1.5 to hit volume target. Risk of SLA miss and provider burnout. **Validation critical pre-launch.**

**Example 3 — Repeat rate assumption:** If D365 repeat is 8% not 15%, LTV drops from AED 40 to AED 28. LTV:CAC at Month 12: 0.56:1 not 0.80:1. **Subscription product becomes critical earlier.**

---

## Business Decisions

| Decision | Rationale |
|----------|-----------|
| Document all assumptions centrally | Investor diligence; team alignment; forecast auditability |
| Medium confidence on demand assumptions | Pre-launch; no actual data; conservative base case |
| Validate top 5 assumptions pre-launch | Provider commission, density, AOV, CAC, completion rate |
| Monthly assumption review Month 1–6 | Fastest learning period; forecast adjustments |
| Bear case uses −20% on top 3 drivers | Jobs, AOV, take rate — covers most downside |
| KSA assumptions low confidence until UAE proof | Delay KSA if UAE assumptions fail validation |

---

## Risks

| Risk | Impact | Mitigation |
|------|--------|------------|
| Core assumptions wrong by >30% | High | Validation plan; monthly review; scenario models |
| Optimistic provider density | High | Pre-sign 150+ providers; field sales pipeline |
| Underestimated CAC | Medium | Channel caps; referral priority |
| Overestimated repeat rate | High | Subscription Phase 2 acceleration if needed |
| Regulatory assumption failure | High | Legal opinion before fundraising close |

---

## Assumptions

- This document captures assumptions as of July 4, 2026; all subject to revision
- Base case used for Series A narrative; bear case for downside planning
- Assumptions cross-referenced across Revenue Forecast, Unit Economics, and CAC-LTV
- Provider interview sample (n=30) representative of Al Quoz tow/battery segment
- Competitor data from public sources and mystery shopping (n=15)

---

## Open Questions

- Which assumptions require board/investor sign-off vs. operational adjustment?
- External market study to validate M2 (breakdown rate)?
- Sensitivity model: automated or manual quarterly?
- Assumption ownership when Product & Strategy Team and Finance diverge?

---

## Next Steps

1. Build assumption register spreadsheet linked to financial model
2. Complete provider commission acceptance survey (n=100 target)
3. Validate AOV with 20 mystery shop quotes pre-launch
4. Set Month 1 assumption review meeting (4 weeks post-launch)
5. Define assumption deviation thresholds triggering forecast revision (>10% yellow; >20% red)
