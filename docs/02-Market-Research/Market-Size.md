# Market Size — Salik Assist

| Field | Value |
|-------|-------|
| **Version** | 1.0 |
| **Status** | Draft |
| **Author** | Product & Strategy Team |
| **Last Updated** | July 4, 2026 |

## Purpose

Quantify the addressable market opportunity for Salik Assist across the UAE and GCC, providing TAM, SAM, and SOM estimates with clear methodology, assumptions, and scenario analysis to support Series A fundraising and strategic planning.

## Scope

Covers market sizing for digital marketplace-facilitated roadside assistance transactions. Includes vehicle parc data, breakdown incidence, average transaction values, and penetration scenarios. Excludes technical infrastructure costs and product development estimates.

## Related Documents

- [Market Research](./Market-Research.md)
- [Industry Analysis](./Industry-Analysis.md)
- [Customer Segments](./Customer-Segments.md)
- [Executive Summary](../01-Executive/Executive-Summary.md)
- [Revenue Forecast](../08-Finance/Revenue-Forecast.md)
- [Unit Economics](../08-Finance/Unit-Economics.md)
- [Go-To-Market](../05-Product-Strategy/Go-To-Market.md)

## Table of Contents

1. [Sizing Summary](#sizing-summary)
2. [Methodology](#methodology)
3. [Total Addressable Market (TAM)](#total-addressable-market-tam)
4. [Serviceable Addressable Market (SAM)](#serviceable-addressable-market-sam)
5. [Serviceable Obtainable Market (SOM)](#serviceable-obtainable-market-som)
6. [UAE Deep Dive](#uae-deep-dive)
7. [GCC Country Breakdown](#gcc-country-breakdown)
8. [Category-Level Sizing](#category-level-sizing)
9. [Scenario Analysis](#scenario-analysis)
10. [Penetration Curve](#penetration-curve)
11. [Business Examples](#business-examples)
12. [Business Decisions](#business-decisions)
13. [Risks](#risks)
14. [Assumptions](#assumptions)
15. [Open Questions](#open-questions)
16. [Next Steps](#next-steps)

---

## Sizing Summary

| Market Layer | UAE (Year 3) | GCC (Year 5) |
|--------------|--------------|--------------|
| **TAM** | $620M | $2.6B |
| **SAM** | $180M–$240M | $720M–$960M |
| **SOM (Salik Assist)** | $18M–$29M GMV | $85M–$120M GMV |
| **Net Revenue (at ~18% take rate)** | $3.2M–$5.2M | $15M–$22M |

*All figures in USD. Year 3 = 36 months post-UAE launch. Year 5 includes KSA and secondary GCC markets.*

---

## Methodology

Market size is derived using a **bottom-up transaction model** triangulated with a **top-down industry revenue** approach.

### Bottom-Up Formula

```
Market Size = Vehicle Parc × Breakdown Incidence Rate × Digital-Eligible Share × Average Transaction Value
```

### Data Sources

| Input | Source | Confidence |
|-------|--------|------------|
| UAE vehicle parc | RTA Dubai, DoT Abu Dhabi, industry reports | High |
| Breakdown incidence | Insurer claims data (benchmarked), automotive associations | Medium |
| Average transaction value | Provider interviews, competitor pricing, mystery shopping | Medium |
| Digital eligibility | Smartphone penetration, corridor coverage analysis | Medium |
| Penetration rates | Mobility marketplace benchmarks (ride-hail, food delivery) | Medium |

### Calibration

Bottom-up estimates are calibrated against top-down industry revenue figures from [Industry Analysis](./Industry-Analysis.md). Variance beyond 15% triggers assumption review.

---

## Total Addressable Market (TAM)

TAM represents all paid roadside assistance and vehicle recovery services in the target geography, regardless of channel.

### UAE TAM

| Input | Value |
|-------|-------|
| Licensed vehicles | 3.5M |
| Annual breakdown events (all types) | 2.8M–4.2M |
| Average transaction value | $95–$165 |
| **UAE TAM (annual)** | **$520M–$680M** |

### GCC TAM

| Country | Licensed Vehicles | Est. TAM |
|---------|-------------------|----------|
| UAE | 3.5M | $520M–$680M |
| KSA | 12M+ | $1.1B–$1.4B |
| Qatar | 1.1M | $95M–$125M |
| Kuwait | 1.5M | $110M–$145M |
| Bahrain | 0.5M | $40M–$55M |
| Oman | 1.2M | $85M–$110M |
| **GCC Total** | **~20M** | **$2.1B–$2.8B** |

---

## Serviceable Addressable Market (SAM)

SAM narrows TAM to transactions that can realistically be facilitated through a digital marketplace—smartphone-enabled customers in corridors with sufficient provider density.

### SAM Filters

| Filter | Exclusion Rate | Rationale |
|--------|----------------|-----------|
| Non-smartphone users | 5% | GCC penetration >90% among motorists |
| Remote/rural (no provider density) | 15% | Marketplace requires supply liquidity |
| OEM warranty captive (non-choice) | 10% | Locked to manufacturer programs |
| Insurer captive dispatch (contracted) | 20% | Some volume requires B2B integration |
| Self-resolved / family assistance | 10% | Non-paid events |

**Net digital-addressable share:** ~40% of TAM

### UAE SAM

| Metric | Conservative | Base | Optimistic |
|--------|--------------|------|------------|
| TAM | $520M | $600M | $680M |
| Digital-addressable % | 35% | 40% | 45% |
| **SAM** | **$182M** | **$240M** | **$306M** |

**Series A planning figure:** $180M–$240M SAM (UAE, Year 3)

### GCC SAM (Year 5)

| Metric | Value |
|--------|-------|
| GCC TAM | $2.1B–$2.8B |
| Digital-addressable % | 35–40% |
| **GCC SAM** | **$720M–$960M** |

---

## Serviceable Obtainable Market (SOM)

SOM represents Salik Assist's realistic revenue capture given competition, execution capability, and partnership pipeline.

### Market Share Targets

| Period | UAE Marketplace Share of SAM | Rationale |
|--------|------------------------------|-----------|
| Year 1 | 2–3% | Launch liquidity; limited geography |
| Year 2 | 5–7% | Category expansion; insurer pilot |
| Year 3 | 8–12% | Density + B2B2C maturity |
| Year 5 (GCC) | 10–14% (blended) | KSA entry; multi-country ops |

### UAE SOM (Year 3)

| Scenario | SAM | Market Share | GMV | Net Revenue (~18%) |
|----------|-----|--------------|-----|-------------------|
| Conservative | $180M | 8% | $14.4M | $2.6M |
| Base | $210M | 10% | $21.0M | $3.8M |
| Optimistic | $240M | 12% | $28.8M | $5.2M |

*Note: Executive Summary Year 3 GMV target of $42M implies broader category mix and B2B volume; reconcile in [Revenue Forecast](../08-Finance/Revenue-Forecast.md) with job volume assumptions (780,000 completed jobs).*

### Job Volume Translation

| Metric | Year 1 | Year 2 | Year 3 |
|--------|--------|--------|--------|
| Completed jobs | 85,000 | 320,000 | 780,000 |
| Avg. transaction value | $49 | $53 | $54 |
| Implied GMV | $4.2M | $16.8M | $42.0M |
| Implied SAM capture (on $210M base) | 2.0% | 8.0% | 20.0% |

Year 3 job-based GMV exceeds pure SAM-share model due to: (a) category mix shift toward higher-value tows, (b) B2B fleet volume, (c) SAM expansion as digital share grows. Both models are maintained; job forecast is operational planning primary.

---

## UAE Deep Dive

### Vehicle Parc by Emirate

| Emirate | Licensed Vehicles | % of UAE | Launch Priority |
|---------|-------------------|----------|-----------------|
| Dubai | 1.6M | 46% | P1 — MVP |
| Abu Dhabi | 1.0M | 29% | P2 — Month 6 |
| Sharjah | 0.5M | 14% | P2 — Month 9 |
| Other | 0.4M | 11% | P3 — Month 12+ |

### Annual Events by Emirate (Base Case)

| Emirate | Events (000s) | Digital-Eligible (000s) |
|---------|---------------|-------------------------|
| Dubai | 1,300–1,800 | 520–720 |
| Abu Dhabi | 800–1,100 | 280–385 |
| Sharjah | 400–550 | 120–165 |

### Launch Corridor SAM (Dubai MVP)

Dubai MVP corridors represent ~35% of Dubai digital-eligible events:

| Corridor | Est. Annual Events | Avg. Transaction |
|----------|-------------------|------------------|
| Sheikh Zayed Road / E11 | 45,000 | $75 |
| Al Khail / E44 | 28,000 | $70 |
| Emirates Road / E611 | 32,000 | $85 |
| Industrial zones (Al Quoz, DIP) | 22,000 | $90 |
| **MVP Corridor Total** | **~127,000** | **$78 avg** |
| **MVP Corridor SAM** | **~$9.9M** | |

Pre-launch provider target of 150–200 verified providers serves this corridor SAM.

---

## GCC Country Breakdown

### Saudi Arabia

| Metric | Value |
|--------|-------|
| Licensed vehicles | 12M+ |
| TAM | $1.1B–$1.4B |
| SAM (digital) | $380M–$480M |
| SOM potential (Year 5) | $45M–$65M GMV |
| Entry timing | Months 12–18 (Riyadh, Jeddah) |
| Sizing vs. UAE | 3–4× UAE potential |

KSA represents the largest GCC expansion prize but requires localized operations, Saudization compliance, and domestic insurer partnerships.

### Secondary GCC Markets

| Country | SAM | Entry Approach |
|---------|-----|----------------|
| Qatar | $35M–$45M | Partner-led; premium positioning |
| Bahrain | $15M–$20M | Cross-border UAE providers |
| Kuwait | $40M–$50M | Local entity required |
| Oman | $30M–$38M | Phased; Muscat first |

---

## Category-Level Sizing

### UAE SAM by Service Category

| Category | % of Events | Avg. Value | SAM Contribution |
|----------|-------------|------------|------------------|
| Towing | 38% | $120 | $34M–$45M |
| Battery | 28% | $65 | $13M–$17M |
| Tire | 18% | $55 | $5M–$7M |
| Mobile mechanic | 9% | $85 | $4M–$5M |
| Fuel delivery | 5% | $45 | $1M–$1.5M |
| Other | 2% | $100 | $0.5M–$1M |
| **Total** | **100%** | **~$77 blended** | **$180M–$240M** |

### Revenue Implications

Tow and battery categories drive 75%+ of GMV; tire and mobile mechanic add frequency. Fuel delivery is low value but high urgency—useful for customer acquisition and retention.

---

## Scenario Analysis

### Bull Case

- Digital adoption accelerates post-launch (insurer partnerships convert 3+ major carriers)
- KSA entry 6 months ahead of plan
- Average transaction value rises 15% due to premium tier adoption
- **Year 3 GMV:** $55M+ | **Year 5 GCC GMV:** $150M+

### Base Case

- UAE launch on plan; KSA entry Month 15
- 2 insurer partnerships live by Year 2
- Steady category mix
- **Year 3 GMV:** $42M | **Year 5 GCC GMV:** $100M

### Bear Case

- Provider supply shortage delays launch 3 months
- Single insurer partnership; slow B2B conversion
- Aggressive competitor undercuts take rate
- **Year 3 GMV:** $22M | **Year 5 GCC GMV:** $50M

---

## Penetration Curve

| Metric | UAE Year 1 | UAE Year 3 | GCC Year 5 |
|--------|------------|------------|------------|
| Motorists aware of Salik Assist | 15% | 55% | 40% (blended) |
| Motorists who have used (ever) | 3% | 18% | 12% |
| Active annual users (1+ request) | 1.5% | 10% | 7% |
| B2B-covered events via platform | 5% | 30% | 25% |

Penetration benchmarks: Careem/Uber reached ~20% urban adoption in 4 years; food delivery apps reached 30%+ in 3 years. Roadside is lower frequency (1 event/year) but higher urgency—awareness matters more than daily active use.

---

## Business Examples

**Example 1 — Bottom-up validation:** Dubai has 1.6M vehicles × 0.9 events/year × 40% digital-eligible × $78 avg = $44.9M Dubai digital SAM. UAE-wide extrapolation yields ~$210M—consistent with base SAM estimate.

**Example 2 — B2B uplift:** A single insurer with 500,000 policyholders generating 40,000 roadside events annually at $90 average adds $3.6M GMV—representing 8.5% of Year 1 base GMV from one partnership.

**Example 3 — KSA multiplier:** Riyadh alone has 4M+ vehicles. At UAE-equivalent incidence and 35% digital eligibility, Riyadh SAM approximates $120M—justifying KSA as Phase 2 priority.

---

## Business Decisions

| Decision | Rationale |
|----------|-----------|
| Plan against base case; fundraise against bull case sensitivity | Investor confidence requires upside; operations require realism |
| Use job-volume model for operational targets | SAM share is strategic; jobs are measurable |
| Prioritize Dubai corridor depth over UAE-wide coverage | MVP SAM of ~$10M is capturable with 150–200 providers |
| Target KSA entry at Month 12–18 | 3–4× UAE SOM justifies expansion investment |
| Anchor tow + battery for 66% of SAM value | Category sequencing aligned to market size |

---

## Risks

| Risk | Impact on Sizing |
|------|------------------|
| Vehicle parc overcount (unregistered vehicles) | TAM inflated 10–15% |
| Breakdown incidence lower in newer vehicle fleet | Event volume -20% |
| Digital eligibility slower in older demographics | SAM -10% |
| Insurance captive volume inaccessible | SAM -15–20% |
| Competitor captures B2B partnerships first | SOM -25% |

---

## Assumptions

- UAE vehicle parc: 3.5M licensed (2025), growing 2.5% annually
- Breakdown incidence: 0.8–1.2 events/vehicle/year (blended)
- Average transaction value: AED 180–320 ($49–$87) metro; higher for highway tows
- Digital-addressable share grows from 35% to 45% by Year 3
- Salik Assist take rate: 18% blended (commission + B2B fees)
- KSA entry adds 2.5–3× UAE job volume by Year 5

---

## Open Questions

- Can insurer claims data under NDA validate breakdown incidence by emirate?
- What is the true average transaction value for informal (cash) transactions?
- How much SAM is locked in multi-year insurer contracts vs. open to marketplace?
- Does "Salik" brand recognition in UAE translate to higher adoption (upside) or category confusion (downside)?
- What is the EV vehicle share impact on battery service SAM by 2028?

---

## Next Steps

1. Validate vehicle parc and incidence with RTA/insurer data requests
2. Reconcile job-volume GMV model with SAM share model in [Revenue Forecast](../08-Finance/Revenue-Forecast.md)
3. Build emirate-level SAM maps for provider recruitment prioritization
4. Develop KSA-specific sizing with local market research partner
5. Establish quarterly SAM/SOM refresh cadence with actual transaction data post-launch
