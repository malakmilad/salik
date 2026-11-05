# Pain Points — Salik Assist

| Field | Value |
|-------|-------|
| **Version** | 1.0 |
| **Status** | Draft |
| **Author** | Product & Strategy Team |
| **Last Updated** | July 4, 2026 |

## Purpose

Catalog and prioritize the pain points experienced by motorists, institutional buyers, and service providers in the current GCC roadside assistance ecosystem. This analysis validates Salik Assist's value proposition and informs product, operations, and go-to-market priorities.

## Scope

Covers demand-side (B2C and B2B) and supply-side pain points in the UAE and GCC context. Maps each pain point to Salik Assist's solution approach. Excludes technical debt, system limitations, or engineering constraints.

## Related Documents

- [Customer Journey](./Customer-Journey.md)
- [Personas](./Personas.md)
- [Customer Segments](./Customer-Segments.md)
- [Market Research](./Market-Research.md)
- [SWOT](./SWOT.md)
- [Executive Summary](../01-Executive/Executive-Summary.md)
- [Business Model Canvas](../04-Business/Business-Model-Canvas.md)

## Table of Contents

1. [Pain Point Framework](#pain-point-framework)
2. [Motorist Pain Points (B2C)](#motorist-pain-points-b2c)
3. [Institutional Buyer Pain Points (B2B)](#institutional-buyer-pain-points-b2b)
4. [Provider Pain Points (Supply)](#provider-pain-points-supply)
5. [Pain Point Severity Matrix](#pain-point-severity-matrix)
6. [Current Workarounds](#current-workarounds)
7. [Salik Assist Solution Mapping](#salik-assist-solution-mapping)
8. [Unaddressed Pain Points](#unaddressed-pain-points)
9. [Business Examples](#business-examples)
10. [Business Decisions](#business-decisions)
11. [Risks](#risks)
12. [Assumptions](#assumptions)
13. [Open Questions](#open-questions)
14. [Next Steps](#next-steps)

---

## Pain Point Framework

Pain points are categorized by type and measured by **severity** (impact on user) and **frequency** (how often experienced in roadside context).

| Type | Definition |
|------|------------|
| **Access** | Cannot find or reach appropriate help |
| **Transparency** | Unknown price, ETA, or provider credentials |
| **Trust** | Fear of fraud, damage, or overcharging |
| **Speed** | Excessive wait for dispatch or arrival |
| **Convenience** | Friction in request, payment, or communication |
| **Economics** | Cost too high; payment disputes; provider underpayment |
| **Quality** | Poor service execution; unprofessional providers |
| **Coverage** | Service or geography not available |

---

## Motorist Pain Points (B2C)

### PP-C1: Unknown Price Before Service

| Attribute | Detail |
|-----------|--------|
| Type | Transparency |
| Severity | Critical |
| Frequency | 65% of out-of-pocket events |
| Current state | Motorists receive price only after service; tow drivers quote on arrival |
| Emotional impact | Anxiety, anger, feeling exploited |
| Segments most affected | Raj (expat), budget motorists |

**Evidence:** Mystery shopping shows 70% of informal tows quote 40–80% above market rate when motorist appears distressed.

---

### PP-C2: Long Wait for Help Assignment

| Attribute | Detail |
|-----------|--------|
| Type | Speed |
| Severity | Critical |
| Frequency | 50% of insurer-dispatched events |
| Current state | Insurer hotlines average 25–45 minutes to assign provider |
| Emotional impact | Fear (highway), frustration, helplessness |
| Segments most affected | Fatima (highway), Sarah (urgent) |

---

### PP-C3: No Real-Time Tracking

| Attribute | Detail |
|-----------|--------|
| Type | Convenience / Transparency |
| Severity | High |
| Frequency | 80%+ of non-app dispatches |
| Current state | Motorist has no visibility into provider location or updated ETA |
| Emotional impact | Anxiety during wait; cannot plan or share status |
| Segments most affected | All B2C; especially women alone, highway |

---

### PP-C4: Unverified or Unprofessional Providers

| Attribute | Detail |
|-----------|--------|
| Type | Trust / Quality |
| Severity | Critical |
| Frequency | 30% report negative provider experience |
| Current state | Informal operators dominate cash-pay segment; no credential check |
| Emotional impact | Fear of damage, theft, harassment |
| Segments most affected | Fatima (luxury), Raj (expat), female motorists |

---

### PP-C5: No Provider Choice

| Attribute | Detail |
|-----------|--------|
| Type | Access / Transparency |
| Severity | High |
| Frequency | 90% of insurer dispatch |
| Current state | Single provider assigned; no comparison of ETA or price |
| Emotional impact | Resignation; perceived unfairness |
| Segments most affected | Sarah, Raj |

---

### PP-C6: Language and Communication Barriers

| Attribute | Detail |
|-----------|--------|
| Type | Convenience |
| Severity | Medium |
| Frequency | 35% of expat motorists |
| Current state | Provider may not speak English/Arabic; location description fails |
| Emotional impact | Frustration; delayed service |
| Segments most affected | Expat residents, tourists |

---

### PP-C7: Cash-Only Payment and No Receipt

| Attribute | Detail |
|-----------|--------|
| Type | Convenience / Economics |
| Severity | Medium |
| Frequency | 55% of informal transactions |
| Current state | Cash demanded; no receipt for insurance reimbursement |
| Emotional impact | Inconvenience; reimbursement delays |
| Segments most affected | Raj, business travelers |

---

### PP-C8: Fragmented Service Categories

| Attribute | Detail |
|-----------|--------|
| Type | Access |
| Severity | Medium |
| Frequency | 25% need non-tow service |
| Current state | Tow app can't help with battery; battery shop doesn't tow |
| Emotional impact | Multiple calls; wasted time |
| Segments most affected | All; especially multi-issue breakdowns |

---

### PP-C9: Unsafe Waiting Conditions

| Attribute | Detail |
|-----------|--------|
| Type | Speed / Trust |
| Severity | Critical (highway) |
| Frequency | 35% of events are highway/safety-critical |
| Current state | Motorists stand outside vehicle in heat, traffic, or darkness |
| Emotional impact | Fear, physical discomfort |
| Segments most affected | Fatima, highway travelers, summer events |

---

### PP-C10: Insurance Claim Complexity

| Attribute | Detail |
|-----------|--------|
| Type | Convenience |
| Severity | Medium |
| Frequency | 45% of insured events |
| Current state | Pay out-of-pocket; submit claim later; slow reimbursement |
| Emotional impact | Financial stress; bureaucracy |
| Segments most affected | Insured motorists without direct billing |

---

## Institutional Buyer Pain Points (B2B)

### PP-B1: High Cost Per Dispatch Event

| Attribute | Detail |
|-----------|--------|
| Type | Economics |
| Severity | High |
| Frequency | Continuous (insurer/fleet) |
| Current state | Legacy assistance contracts rising 6–10% annually |
| Stakeholder | Noura (insurer), Khalid (fleet) |

---

### PP-B2: Poor Policyholder / Driver Satisfaction

| Attribute | Detail |
|-----------|--------|
| Type | Quality |
| Severity | High |
| Frequency | Top-3 complaint in motor insurance CSAT |
| Current state | 45-min dispatch; no tracking; opaque process |
| Stakeholder | Insurers |

---

### PP-B3: No Real-Time Visibility for Operations

| Attribute | Detail |
|-----------|--------|
| Type | Transparency |
| Severity | Medium |
| Frequency | Fleet managers daily |
| Current state | Drivers self-dispatch; manager learns after the fact |
| Stakeholder | Fleet managers |

---

### PP-B4: Fraudulent or Inflated Tow Claims

| Attribute | Detail |
|-----------|--------|
| Type | Economics / Trust |
| Severity | High |
| Frequency | 8–12% of claims flagged |
| Current state | Collusion between providers and claimants; inflated distances |
| Stakeholder | Insurers |

---

### PP-B5: Inconsistent Provider Quality Across Geography

| Attribute | Detail |
|-----------|--------|
| Type | Quality / Coverage |
| Severity | Medium |
| Frequency | Multi-emirate operations |
| Current state | Strong Dubai network; weak Sharjah/rural coverage |
| Stakeholder | Insurers, fleets |

---

### PP-B6: Long B2B Sales and Integration Cycles

| Attribute | Detail |
|-----------|--------|
| Type | Access |
| Severity | Medium |
| Frequency | Per partnership |
| Current state | 6–9 months from pitch to live integration |
| Stakeholder | Salik Assist (internal) |

---

## Provider Pain Points (Supply)

### PP-S1: Idle Capacity and Unpredictable Demand

| Attribute | Detail |
|-----------|--------|
| Type | Economics |
| Severity | Critical |
| Frequency | Daily (55% utilization) |
| Current state | Trucks sit idle 3–5 hours/day; revenue unpredictable |
| Segments affected | Tow operators (Ahmed) |

---

### PP-S2: Payment Collection Risk

| Attribute | Detail |
|-----------|--------|
| Type | Economics |
| Severity | Critical |
| Frequency | 15–20% of informal jobs |
| Current state | Customer refuses to pay; cash disputes; no recourse |
| Segments affected | All providers |

---

### PP-S3: No Digital Demand Channel

| Attribute | Detail |
|-----------|--------|
| Type | Access |
| Severity | High |
| Frequency | Continuous |
| Current state | Depend on phone, garage referrals, roadside visibility |
| Segments affected | All providers |

---

### PP-S4: Insurance Payment Delays

| Attribute | Detail |
|-----------|--------|
| Type | Economics |
| Severity | High |
| Frequency | 60–90 day payment cycles |
| Current state | Cash flow strain; providers avoid insurer jobs |
| Segments affected | Tow operators, battery specialists |

---

### PP-S5: Price Undercutting by Informal Operators

| Attribute | Detail |
|-----------|--------|
| Type | Economics |
| Severity | High |
| Frequency | Continuous |
| Current state | Unlicensed operators accept 30% less; no overhead |
| Segments affected | Licensed providers |

---

### PP-S6: Customer No-Shows and Cancellations

| Attribute | Detail |
|-----------|--------|
| Type | Economics |
| Severity | Medium |
| Frequency | 10–15% of dispatched jobs |
| Current state | Provider en route; customer found another solution |
| Segments affected | All providers |

---

### PP-S7: No Reputation Portability

| Attribute | Detail |
|-----------|--------|
| Type | Access |
| Severity | Medium |
| Frequency | Continuous |
| Current state | Good service on phone dispatch builds no digital reputation |
| Segments affected | Mobile mechanics (Hassan), quality-focused operators |

---

### PP-S8: Commission and Platform Fee Concerns

| Attribute | Detail |
|-----------|--------|
| Type | Economics |
| Severity | Medium |
| Frequency | Per platform evaluation |
| Current state | Providers resist 15–20% commission without proven demand lift |
| Segments affected | All considering marketplace join |

---

## Pain Point Severity Matrix

| Pain Point | Severity | Frequency | Salik Assist Addresses? | Priority |
|------------|----------|-----------|---------------------------|----------|
| PP-C1 Unknown price | Critical | High | ✓ Top-3 offers | P1 |
| PP-C2 Long wait | Critical | High | ✓ Fast matching | P1 |
| PP-C3 No tracking | High | Very High | ✓ Live ETA | P1 |
| PP-C4 Unverified providers | Critical | Medium | ✓ Verification | P1 |
| PP-C5 No choice | High | High | ✓ Top-3 model | P1 |
| PP-C9 Unsafe waiting | Critical | Medium | ✓ Speed + tracking | P1 |
| PP-S1 Idle capacity | Critical | High | ✓ Demand routing | P1 |
| PP-S2 Payment risk | Critical | Medium | ✓ Platform payment | P1 |
| PP-B1 High dispatch cost | High | Continuous | ✓ Marketplace efficiency | P1 |
| PP-B2 Poor CSAT | High | Continuous | ✓ UX + speed | P1 |
| PP-C6 Language barriers | Medium | Medium | Partial (multilingual) | P2 |
| PP-C8 Fragmented categories | Medium | Medium | ✓ Multi-category | P2 |
| PP-S4 Insurance delays | High | Medium | ✓ 48-hour payout | P2 |
| PP-B4 Fraud | High | Medium | Partial (GPS, photos) | P2 |
| PP-C10 Insurance claim complexity | Medium | Medium | ✓ B2B2C billing | P2 |

---

## Current Workarounds

| Pain Point | Motorist Workaround | Why It Fails |
|------------|---------------------|--------------|
| PP-C1 Price unknown | Ask friend for "fair price" | Friend may be wrong; stress affects judgment |
| PP-C2 Long wait | Call multiple tow numbers | Wastes time; no better outcome |
| PP-C3 No tracking | Call provider repeatedly | Provider may not answer while driving |
| PP-C4 Trust | Use insurer only | Slow; no choice; still unverified at arrival |
| PP-C5 No choice | Accept assigned provider | Resignation; no recourse |
| PP-S1 Idle time | Wait by phone | Unpredictable; can't plan day |
| PP-S2 Payment risk | Demand cash upfront | Customer hostility; lost jobs |

---

## Salik Assist Solution Mapping

| Pain Point | Salik Assist Solution | Business Mechanism |
|------------|----------------------|-------------------|
| PP-C1 | Upfront price estimate in each offer | Provider submits estimate before acceptance |
| PP-C2 | Top-3 offers within 5 minutes | Marketplace matching; provider app alerts |
| PP-C3 | Live provider tracking | GPS sharing during active job |
| PP-C4 | Verification badge (license, insurance) | Onboarding checks before activation |
| PP-C5 | Top-3 competitive offers | Customer selects preferred option |
| PP-C6 | Arabic, English, Hindi support | Localized app and support team |
| PP-C7 | In-app card payment + digital receipt | Payment facilitation |
| PP-C8 | Multi-category marketplace | Tow, battery, tire, fuel, mechanic in one app |
| PP-C9 | Fastest-ETA highlighting | Highway-priority matching algorithm (business rules) |
| PP-C10 | Insurer direct billing (B2B2C) | Partnership integration |
| PP-S1 | Qualified demand to idle providers | Marketplace routing |
| PP-S2 | Platform-guaranteed payment | Escrow-style payment on completion |
| PP-S3 | Provider app with job alerts | Digital demand channel |
| PP-S4 | 48-hour provider payout | Platform float and payment processing |
| PP-S5 | Verified quality premium | Customers choose verified over cheapest |
| PP-S6 | Commitment on acceptance | Cancellation penalties |
| PP-S7 | Star ratings and job history | Reputation system |
| PP-B1 | Lower cost per dispatch | Competitive provider offers reduce average |
| PP-B2 | Tracking + speed | Measurable CSAT improvement |
| PP-B3 | Fleet dashboard | B2B reporting (Phase 2) |
| PP-B4 | GPS-verified pickup/dropoff | Distance validation; photo evidence |

---

## Unaddressed Pain Points

Pain points Salik Assist does not fully solve in MVP (acknowledged gaps):

| Pain Point | Gap | Planned Resolution |
|------------|-----|-------------------|
| PP-C9 Unsafe waiting | Cannot shorten physical distance | Fastest matching; safety guidance content |
| PP-B4 Fraud | Sophisticated collusion | Phase 2: ML fraud detection |
| PP-B6 Long B2B cycles | Sales process inherent | Dedicated partnerships team |
| EV-specific recovery | New category | Phase 3: EV charging assistance |
| Desert/off-road recovery | Low provider density | Geographic gating; specialist partnerships |

---

## Business Examples

**Example 1 — PP-C1 resolution:** Raj's car won't start in JLT. Opens Salik Assist. Three offers: AED 140 (22 min), AED 165 (15 min), AED 195 (10 min). Selects AED 165. Final bill AED 170 (within estimate). No haggling. Pain point eliminated.

**Example 2 — PP-S1 resolution:** Ahmed's tow truck idle at 2 PM Tuesday. Salik Assist alert: battery job 4 km away, AED 120. Accepts. 40 minutes of idle time converted to revenue. Monthly idle reduction: 12 hours → 3 hours.

**Example 3 — PP-B2 resolution:** Insurer pilot: dispatch time drops from 42 minutes to 14 minutes. Policyholder CSAT on assistance rises from 3.2 to 4.1 (out of 5). Noura approves annual contract.

---

## Business Decisions

| Decision | Pain Points Addressed |
|----------|----------------------|
| Top-3 offer model | PP-C1, PP-C5 |
| Verification before activation | PP-C4 |
| 48-hour provider payout | PP-S2, PP-S4 |
| Multi-category from positioning day one | PP-C8 |
| 0% commission launch period | PP-S8 |
| Insurer B2B2C direct billing | PP-C10, PP-B1 |
| Highway corridor supply density | PP-C2, PP-C9 |

---

## Risks

| Risk | Related Pain Point | If Unresolved |
|------|-------------------|---------------|
| Supply shortage | PP-C2, PP-C5 | Pain points persist; customer abandonment |
| Verification lapses | PP-C4 | Trust pain point worsens; brand damage |
| Price estimate inaccuracy | PP-C1 | New pain point: "app lied about price" |
| Provider payout delays | PP-S2, PP-S4 | Supply churn; pain point transfers to platform |
| B2B partnership delay | PP-B1, PP-B2 | Insurer channel pain points unaddressed |

---

## Assumptions

- Pain point severity rankings reflect UAE market; KSA may differ (higher PP-C6 in some regions)
- 65% price opacity figure holds for out-of-pocket; insured events have pre-negotiated rates
- Provider willingness to join marketplace correlates directly with PP-S1 and PP-S2 severity
- Customers will trade 5–10% higher price for PP-C1 and PP-C3 resolution
- Insurer pain points (PP-B1, PP-B2) are sufficient to drive partnership conversations

---

## Open Questions

- What percentage of female motorists cite PP-C4 (trust) as primary concern vs. price?
- Do tourists (PP-C6, PP-C7) have distinct pain points requiring rental-specific flows?
- Can PP-B4 (fraud) be addressed sufficiently without insurer data sharing?
- What is the minimum price transparency (range vs. fixed) that resolves PP-C1?
- Do providers perceive PP-S8 (commission) as worse than PP-S5 (informal undercutting)?

---

## Next Steps

1. Validate pain point rankings via customer survey (n=400, Q3 2026)
2. Map P1 pain points to MVP feature priorities in [MVP](../09-Roadmap/MVP.md)
3. Develop marketing messaging around top 3 motorist pain points (price, wait, trust)
4. Design provider pitch around PP-S1 and PP-S2 resolution
5. Build insurer ROI model centered on PP-B1 and PP-B2
