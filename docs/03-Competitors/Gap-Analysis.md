# Gap Analysis — Salik Assist

| Field | Value |
|-------|-------|
| **Version** | 1.0 |
| **Status** | Draft |
| **Author** | Product & Strategy Team |
| **Last Updated** | July 4, 2026 |

## Purpose

Identify gaps between current market offerings and customer, provider, and partner expectations—and define how Salik Assist closes those gaps to establish category leadership in the GCC roadside assistance marketplace.

## Scope

Business and experience gaps only. Excludes technical debt, engineering backlog, and system integration specifications.

## Related Documents

- [Competitor Analysis](./Competitor-Analysis.md)
- [Competitive Matrix](./Competitive-Matrix.md)
- [Market Positioning](./Market-Positioning.md)
- [Value Proposition](../04-Business/Value-Proposition.md)
- [Business Requirements](../04-Business/Business-Requirements.md)
- [Personas](../02-Market-Research/Personas.md)

## Table of Contents

1. [Gap Analysis Framework](#gap-analysis-framework)
2. [Customer-Side Gaps](#customer-side-gaps)
3. [Provider-Side Gaps](#provider-side-gaps)
4. [Partner-Side Gaps (B2B)](#partner-side-gaps-b2b)
5. [Market & Category Gaps](#market--category-gaps)
6. [Salik Assist Gap Closure Plan](#salik-assist-gap-closure-plan)
7. [Gap Priority Matrix](#gap-priority-matrix)
8. [Business Examples](#business-examples)
9. [Business Decisions](#business-decisions)
10. [Risks](#risks)
11. [Assumptions](#assumptions)
12. [Open Questions](#open-questions)
13. [Next Steps](#next-steps)

---

## Gap Analysis Framework

Gaps are classified by:

| Type | Definition |
|------|------------|
| **Experience gap** | Difference between what customers expect (Uber-like) and what market delivers |
| **Supply gap** | Insufficient verified providers in zone, category, or time window |
| **Trust gap** | Lack of verification, accountability, or dispute resolution |
| **Commercial gap** | Missing B2B channels, pricing models, or partnership structures |
| **Geographic gap** | Underserved corridors, emirates, or rural/desert routes |

Each gap is rated: **Critical / High / Medium / Low** based on impact on launch success and revenue.

---

## Customer-Side Gaps

| Gap | Current Market State | Customer Expectation | Salik Assist Response | Priority |
|-----|---------------------|---------------------|----------------------|----------|
| Wait time opacity | "Someone is coming" with no ETA | Live ETA like ride-hailing | Real-time tracking from offer accept | Critical |
| Price uncertainty | Bill negotiated on-site or unknown | Upfront price band before commit | Top-3 offers with estimate ranges | Critical |
| No provider choice | Single dispatch from insurer or first tow | Compare options | Competitive top-3 offer model | Critical |
| Trust in stranger | Unverified tow drivers | Verified credentials visible | License, insurance, background badges | Critical |
| Multi-service friction | Call different numbers for tow vs. battery | One app, all breakdown types | Multi-category marketplace | High |
| Language support | Arabic/English inconsistency | Bilingual seamless experience | Arabic-first UX with English parity | High |
| Payment friction | Cash-only informal providers | Card/wallet, receipt | In-app payment + digital receipt | High |
| Post-incident support | No recourse after bad service | Dispute resolution + refund path | Platform mediation + guarantee fund | High |
| Safe waiting guidance | Customer alone on highway | Safety instructions while waiting | In-app safety checklist + share trip | Medium |
| Coverage confidence | Unknown if help available in area | Clear coverage map | Zone availability indicator pre-request | Medium |

---

## Provider-Side Gaps

| Gap | Current Market State | Provider Expectation | Salik Assist Response | Priority |
|-----|---------------------|---------------------|----------------------|----------|
| Irregular demand | Feast/famine by season and zone | Steady qualified leads | Demand aggregation marketplace | Critical |
| Payment delays | Cash disputes, bounced cheques | Guaranteed fast payout | Escrow + 48-hour payout SLA | Critical |
| No reputation portability | Word of mouth only | Digital ratings that follow business | Provider profile + rating history | High |
| Marketing cost | Yellow pages, signage, WhatsApp groups | Low-cost customer acquisition | Platform brings demand | High |
| Pricing pressure | Race to bottom with informal | Fair rates with visibility | Guardrailed pricing + surge share | Medium |
| Admin burden | Manual invoicing | Automated job records | Job history, tax-ready statements | Medium |
| Exclusivity demands | Platforms requiring exclusivity | Business independence | Non-exclusive provider terms | Medium |
| Training & standards | Inconsistent service quality | Clear service standards | Provider onboarding playbook | Medium |
| Peak capacity tools | Overwhelmed during heat waves | Surge incentives | Dynamic incentive bonuses | Low |

---

## Partner-Side Gaps (B2B)

| Gap | Current Market State | Partner Expectation | Salik Assist Response | Priority |
|-----|---------------------|--------------------|-----------------------|----------|
| Insurer SLA reporting | Manual call logs | Real-time dispatch analytics | Partner dashboard with SLA metrics | Critical |
| Fleet multi-vendor chaos | Separate tow contracts per city | Single GCC dispatch partner | Unified B2B contract + network | High |
| Rental car overflow | Dealer roadside limited hours | 24/7 overflow partner | White-label API routing | High |
| Pre-negotiated rates | Renegotiated annually offline | Dynamic rate cards by zone | Category rate cards + audit trail | High |
| Co-branded experience | Insurer brand diluted | Policyholder sees insurer + Salik | Co-branded customer journey | Medium |
| Fraud prevention | Duplicate claims | Job verification timestamps | GPS-verified job completion | Medium |
| EV roadside (emerging) | No standard offering | EV-aware dispatch | EV category tagging (Phase 2) | Low |

---

## Market & Category Gaps

| Gap | Description | Opportunity Size | Salik Assist Timing |
|-----|-------------|------------------|---------------------|
| No GCC-native marketplace leader | Fragmented local players | $180M–$240M SAM UAE | Launch window open |
| Desert / remote recovery underserved digitally | High-value, low-frequency | Premium pricing | Phase 2 category |
| Expat / tourist segment | Unfamiliar with local providers | High willingness to pay | Launch targeting |
| Women drivers safety concern | Prefer verified, tracked service | Trust premium | Verification moat |
| Corporate fleet digitization | Manual phone dispatch | Recurring B2B revenue | Month 6+ pursuit |
| Seasonal battery surge (summer) | Supply crunch June–August | Surge revenue | Pre-position supply |

---

## Salik Assist Gap Closure Plan

### Phase 1 — Launch (Months 0–6)

| Gap Closed | Initiative | Success Metric |
|------------|-----------|----------------|
| Price uncertainty | Top-3 offer model | 90%+ requests receive 3 offers in 5 min |
| Trust gap | Verification program | 100% active providers verified |
| Wait time opacity | Live tracking | Customer ETA accuracy ±5 min |
| Supply gap (Dubai) | 150+ provider sign-ups | <10% unfilled requests in launch zone |
| Payment friction | In-app payment | 85%+ card/wallet adoption |

### Phase 2 — Scale (Months 7–12)

| Gap Closed | Initiative | Success Metric |
|------------|-----------|----------------|
| Multi-service friction | Add tire, fuel, mechanic | 4+ categories live |
| Insurer SLA reporting | B2B partner portal | 2+ insurer LOIs signed |
| Geographic gap | Abu Dhabi + Sharjah | 80% highway coverage |
| Post-incident support | Dispute resolution process | <72 hr resolution SLA |

### Phase 3 — Expand (Year 2+)

| Gap Closed | Initiative | Success Metric |
|------------|-----------|----------------|
| Fleet multi-vendor | Enterprise contracts | 5+ fleet partners |
| Desert recovery | Specialist provider tier | Category live in UAE |
| KSA market gap | Riyadh/Jeddah launch | 200+ KSA providers |
| EV roadside | EV-stranded category | Pilot with charging partner |

---

## Gap Priority Matrix

```
                    HIGH IMPACT
                         │
    Insurer B2B SLA      │   Price transparency
    Provider supply      │   Top-3 offers
                         │   Verification/trust
         ────────────────┼────────────────
                         │
    Desert recovery      │   EV roadside
    Promoted listings    │   Safety checklist
                         │
                    LOW IMPACT
         LOW URGENCY ────┴──── HIGH URGENCY
```

**Focus order:** Top-right quadrant first (critical customer gaps at launch), then top-left (B2B and supply), defer bottom quadrants.

---

## Business Examples

**Example 1 — Trust gap closure:** An expat woman stranded at night rejects informal tow offers. Salik Assist shows three providers with photo, license number, 4.7+ ratings, and live tracking. She accepts within 3 minutes—gap closed vs. market norm.

**Example 2 — Insurer SLA gap:** An insurer partner receives monthly PDF reports today with 48-hour lag. Salik partner dashboard shows live dispatch metrics, average ETA, and completion rates—enabling renewal and co-marketing.

**Example 3 — Supply gap during heat wave:** July battery requests spike 300%. Gap analysis flagged seasonal supply risk. Salik pre-recruits 30 battery specialists and activates surge bonuses—fill rate stays above 92%.

---

## Business Decisions

| Decision | Rationale |
|----------|-----------|
| Close customer trust gaps before B2B gaps | B2B partners will not route volume to a consumer-untrusted brand |
| Accept geographic gap outside launch corridor at MVP | Density beats breadth; gating prevents bad early experiences |
| Build dispute resolution before scale marketing | Trust gaps explode with volume if unresolved |
| Defer EV roadside to Phase 2 | Market gap exists but volume insufficient at launch |
| Provider payment speed is non-negotiable | Supply gap widens if payout SLA slips |

---

## Risks

| Risk | Impact | Mitigation |
|------|--------|------------|
| Gap closure slower than competitor entry | High | Phase 1 scope discipline; pre-launch provider pipeline |
| Closing price gap erodes provider margins | Medium | Guardrailed minimum rates; surge share |
| B2B gap requires features partners expect Day 1 | High | LOI-driven roadmap prioritization |
| Over-promising gap closure in marketing | Medium | Zone gating; honest coverage maps |
| Seasonal supply gap repeats annually | Medium | Year-ahead recruitment calendar |

---

## Assumptions

- Customer gaps validated in 40+ discovery interviews (UAE motorists)
- Provider payment gap is top-3 reason operators would join a platform
- Insurers acknowledge SLA reporting gap internally
- No competitor closes top-3 offer gap before Salik launch
- Geographic gap acceptable to 85% of launch-zone target customers

---

## Open Questions

- Which gap matters most to first insurer LOI: SLA reporting or rate cards?
- Can we close desert recovery gap via partnership vs. owned recruitment?
- Is "safe waiting guidance" a launch requirement or Phase 2?
- What fill rate threshold defines "supply gap closed" per zone?
- Do fleet operators prioritize single-vendor or multi-vendor gap closure?

---

## Next Steps

1. Map each Phase 1 gap to owner and milestone in launch plan
2. Validate critical gaps with 10 customer usability sessions
3. Align [Business Requirements](../04-Business/Business-Requirements.md) to gap priorities
4. Present gap closure timeline in Series A investor deck
5. Review gap status monthly at leadership ops review
