# Revenue Model — Salik Assist

| Field | Value |
|-------|-------|
| **Version** | 1.0 |
| **Status** | Draft |
| **Author** | Product & Strategy Team |
| **Last Updated** | July 4, 2026 |

## Purpose

Define how Salik Assist generates revenue across customer, provider, and partner segments—and project revenue composition to support Series A financial planning and investor diligence.

## Scope

Revenue streams, monetization mechanics, and high-level projections. Excludes technical payment processing, accounting systems, and detailed financial models (see Finance folder).

## Related Documents

- [Pricing Strategy](./Pricing-Strategy.md)
- [Business Model Canvas](./Business-Model-Canvas.md)
- [Cost Structure](./Cost-Structure.md)
- [Revenue Forecast](../08-Finance/Revenue-Forecast.md)
- [Unit Economics](../08-Finance/Unit-Economics.md)
- [Business Rules](./Business-Rules.md)

## Table of Contents

1. [Revenue Model Summary](#revenue-model-summary)
2. [Primary Revenue: Commission (Take Rate)](#primary-revenue-commission-take-rate)
3. [Secondary Revenue: Provider Subscriptions](#secondary-revenue-provider-subscriptions)
4. [B2B Revenue: Dispatch & Platform Fees](#b2b-revenue-dispatch--platform-fees)
5. [Surge Revenue Share](#surge-revenue-share)
6. [Promoted Listings & Advertising](#promoted-listings--advertising)
7. [Revenue by Segment & Geography](#revenue-by-segment--geography)
8. [Revenue Projections](#revenue-projections)
9. [Revenue Recognition Principles](#revenue-recognition-principles)
10. [Business Examples](#business-examples)
11. [Business Decisions](#business-decisions)
12. [Risks](#risks)
13. [Assumptions](#assumptions)
14. [Open Questions](#open-questions)
15. [Next Steps](#next-steps)

---

## Revenue Model Summary

Salik Assist operates a **multi-stream marketplace revenue model** aligned to completed successful jobs and partner value delivered:

| Stream | Type | Year 1 Mix | Year 3 Mix |
|--------|------|------------|------------|
| Commission (take rate) | Transaction | 88% | 75% |
| B2B dispatch fees | Contract + transaction | 5% | 12% |
| Provider subscriptions | Recurring | 2% | 8% |
| Surge share | Transaction (variable) | 4% | 3% |
| Promoted listings | Recurring / CPM | 1% | 2% |

**Philosophy:** Primary revenue tied to GMV ensures platform incentives align with customer satisfaction and job completion. Secondary streams diversify without compromising marketplace neutrality.

---

## Primary Revenue: Commission (Take Rate)

| Attribute | Detail |
|-----------|--------|
| **Mechanism** | Percentage of final job value deducted at payment |
| **Standard B2C rate** | 18% |
| **B2B rate** | 12–15% (contract-dependent; lower due to volume guarantee) |
| **Launch promotion** | 0% commission for first 30 days for providers in launch zones |
| **Collection** | Automatic at customer payment; net payout to provider |

**Blended take rate target:** 17–18% across all job types by Year 2.

| Service Category | Avg. Job Value (AED) | Commission @ 18% |
|-----------------|---------------------|------------------|
| Battery jump-start | 100–150 | 18–27 |
| Flat tire change | 120–180 | 22–32 |
| Emergency fuel | 80–120 | 14–22 |
| Local tow (< 20 km) | 200–350 | 36–63 |
| Long-distance tow | 400–800 | 72–144 |
| Mobile mechanic | 150–300 | 27–54 |

---

## Secondary Revenue: Provider Subscriptions

| Tier | Monthly Fee (AED) | Benefits |
|------|-------------------|----------|
| **Standard** | Free | Basic listing, standard offer eligibility |
| **Professional** | 299 | Priority in offer ranking (+weight), monthly analytics report |
| **Premium** | 499 | Top placement bias in top-3, dedicated support, promotional badge |

**Target:** 15% of active providers on paid tier by Year 2; 25% by Year 3.

Subscription revenue is **non-commission** and improves provider LTV without increasing customer price.

---

## B2B Revenue: Dispatch & Platform Fees

| Model | Description | Typical Pricing |
|-------|-------------|-----------------|
| **Per-dispatch fee** | Flat fee per completed B2B job | AED 8–15 per dispatch |
| **Platform fee** | Monthly access to network + reporting | AED 5,000–25,000/month by volume tier |
| **Volume discount** | Reduced per-dispatch above threshold | Tiered at 1K, 5K, 10K monthly jobs |

**B2B revenue includes:** Insurer roadside programs, fleet operators, rental companies, dealer overflow programs.

**Target:** B2B contributes 25%+ of job volume and 12% of net revenue by Year 3.

---

## Surge Revenue Share

During validated peak demand (Rule 31), surge pricing activates:

| Party | Surge Increment Share |
|-------|----------------------|
| Provider | 70% |
| Salik Assist | 30% |

Surge is incremental revenue above base commission. Base commission (18%) still applies to full job value.

**Peak windows:** Summer afternoons (battery), post-rain (accidents), holiday exodus (highway tows).

---

## Promoted Listings & Advertising

| Product | Description | Pricing |
|---------|-------------|---------|
| **Zone boost** | Enhanced visibility in specific zone for 30 days | AED 750/zone/month |
| **Category sponsor** | "Featured battery provider" badge | AED 500/month |
| **Highway corridor** | Priority in highway breakdown zones | AED 1,200/corridor/month |

**Guardrail:** Promoted providers must still meet verification and rating minimums (Rule 7). Paid placement does not guarantee top-3 selection—it adds ranking weight.

---

## Revenue by Segment & Geography

### By Customer Segment (Year 3)

| Segment | % of Jobs | % of Net Revenue | Notes |
|---------|-----------|------------------|-------|
| B2C direct | 55% | 60% | Higher take rate |
| B2B2C (insurance) | 30% | 28% | Volume + lower rate |
| B2B fleet | 15% | 12% | Contract + dispatch fees |

### By Geography (Year 3)

| Market | % of Net Revenue |
|--------|------------------|
| UAE (Dubai, Abu Dhabi, Sharjah) | 70% |
| KSA (Riyadh, Jeddah) | 25% |
| Other GCC | 5% |

---

## Revenue Projections

| Metric | Year 1 | Year 2 | Year 3 |
|--------|--------|--------|--------|
| Completed jobs | 85,000 | 320,000 | 780,000 |
| GMV | $4.2M | $16.8M | $42.0M |
| Gross revenue | $840K | $3.4M | $8.8M |
| Net revenue (after provider incentives) | $756K | $3.0M | $7.6M |
| Blended take rate | 18% | 18% | 18.3% |
| Gross margin | 72% | 78% | 82% |

*Detailed model: [Revenue Forecast](../08-Finance/Revenue-Forecast.md)*

---

## Revenue Recognition Principles

1. **Commission revenue** recognized upon job completion and successful customer payment
2. **Subscription revenue** recognized monthly over subscription period
3. **B2B platform fees** recognized monthly per contract terms
4. **B2B dispatch fees** recognized upon job completion
5. **Promotional credits** treated as contra-revenue (marketing expense)
6. **Disputed jobs** revenue deferred until resolution (max 14 days per Rule 48)

---

## Business Examples

**Example 1 — Standard B2C job:** Tow completed at AED 280. Customer pays in-app. Salik collects AED 280; retains AED 50.40 commission (18%); pays provider AED 229.60 within 48 hours. Net revenue: AED 50.40.

**Example 2 — Surge job:** Battery jump during July heat wave with 1.3× surge. Base AED 100 + AED 30 surge increment. Commission: 18% × AED 130 = AED 23.40. Surge share: 30% × AED 30 = AED 9. Provider receives: AED 130 − AED 23.40 − AED 9 surge platform share + AED 21 provider surge share = AED 97.60 + AED 21 = AED 118.60.

**Example 3 — B2B insurer month:** Insurer routes 2,000 jobs. Platform fee AED 10,000 + per-dispatch AED 10 × 2,000 = AED 20,000. Commission at 13% on AED 400 avg job × 2,000 = AED 104,000. Total B2B monthly revenue: AED 134,000.

---

## Business Decisions

| Decision | Rationale |
|----------|-----------|
| Commission-primary (not subscription-primary) | Aligns with marketplace best practice; scales with GMV |
| 18% B2C take rate | Balance provider adoption and unit economics |
| Lower B2B rates for volume | Secures demand moat; reduces CAC |
| Surge share 30% platform | Incentivizes supply during peaks without customer gouging |
| Defer heavy ad revenue to Year 2 | Focus on marketplace liquidity first |

---

## Risks

| Risk | Impact | Mitigation |
|------|--------|------------|
| Provider pushback on 18% commission | High | Launch promo; demonstrate demand ROI |
| B2B pricing undercut by competitors | Medium | SLA reporting value; network density |
| Surge revenue unpredictable | Low | Base commission provides floor |
| Revenue concentration in tow category | Medium | Expand categories; B2B diversification |
| Promoted listings perceived as pay-to-win | Medium | Ranking weight limits; rating minimums |

---

## Assumptions

- Average B2C job value AED 200–250 blended across categories
- 18% take rate sustainable without mass provider churn post-promo
- B2B contracts signed by Month 8 contribute meaningfully to Year 1
- Subscription adoption follows 15% / 25% trajectory
- GMV growth of 4× Year 1 to Year 2 driven by geography + density

---

## Open Questions

- Category-specific take rates (lower for low-margin fuel delivery)?
- Should launch zero-commission extend beyond 30 days?
- B2B per-dispatch vs. platform fee optimal mix?
- Revenue share model for dealer/OEM partnerships?
- KSA pricing in SAR with different take rate?

---

## Next Steps

1. Finance team to build detailed 36-month revenue model
2. Validate 18% take rate with 20 provider interviews
3. Draft B2B pricing menu for partnerships team
4. Define subscription tier launch timing (Month 6 target)
5. Align revenue recognition with accounting advisor
