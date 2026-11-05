# CAC & LTV — Salik Assist

| Field | Value |
|-------|-------|
| **Version** | 1.0 |
| **Status** | Draft |
| **Author** | Product & Strategy Team |
| **Last Updated** | July 4, 2026 |

## Purpose

Define customer acquisition cost (CAC), lifetime value (LTV), and the LTV:CAC ratio framework for Salik Assist—guiding marketing spend efficiency, channel investment, and growth sustainability.

## Scope

B2C customer acquisition and retention economics for UAE operations. B2B partner acquisition treated separately. Excludes provider acquisition costs (covered in go-to-market budget).

## Related Documents

- [Unit Economics](./Unit-Economics.md)
- [Revenue Forecast](./Revenue-Forecast.md)
- [Financial Assumptions](./Financial-Assumptions.md)
- [Customer Onboarding](../06-Operations/Customer-Onboarding.md)
- [Go-To-Market](../05-Product-Strategy/Go-To-Market.md)

## Table of Contents

1. [Framework Overview](#framework-overview)
2. [Customer Acquisition Cost (CAC)](#customer-acquisition-cost-cac)
3. [Lifetime Value (LTV)](#lifetime-value-ltv)
4. [LTV:CAC Ratio Targets](#ltvcac-ratio-targets)
5. [CAC by Channel](#cac-by-channel)
6. [Cohort Retention & LTV Build](#cohort-retention--ltv-build)
7. [Payback Period](#payback-period)
8. [B2B Customer Economics](#b2b-customer-economics)
9. [Marketing Budget Allocation](#marketing-budget-allocation)
10. [Business Examples](#business-examples)
11. [Business Decisions](#business-decisions)
12. [Risks](#risks)
13. [Assumptions](#assumptions)
14. [Open Questions](#open-questions)
15. [Next Steps](#next-steps)

---

## Framework Overview

| Metric | Definition | Formula |
|--------|------------|---------|
| **CAC** | Cost to acquire one new customer who completes ≥1 job | Total acquisition spend ÷ new customers |
| **LTV** | Total contribution margin from a customer over relationship | Avg jobs × contribution/job × retention periods |
| **LTV:CAC** | Return on acquisition investment | LTV ÷ CAC |
| **Payback period** | Months to recover CAC from customer contribution | CAC ÷ (monthly contribution per customer) |

**Target LTV:CAC:** ≥3:1 by Month 12; ≥4:1 at maturity.

---

## Customer Acquisition Cost (CAC)

### Blended CAC Targets

| Period | Blended CAC (AED) | Blended CAC (USD) | New Customers/Month |
|--------|-------------------|-------------------|---------------------|
| Launch (M1–3) | 75 | $20 | 1,200 |
| Growth (M4–9) | 55 | $15 | 4,500 |
| Mature (M10–12) | 45 | $12 | 7,000 |
| Year 2 avg | 40 | $11 | 12,000 |
| Year 3 avg | 35 | $10 | 22,000 |

### CAC Cost Components

| Component | % of CAC | Launch (AED) |
|-----------|----------|--------------|
| Performance marketing (paid search, social) | 45% | 33.75 |
| Referral incentives (both sides) | 20% | 15.00 |
| Partnerships (dealership, car wash) | 15% | 11.25 |
| App store optimization & content | 10% | 7.50 |
| Launch promotions (AED 30 first-job credit) | 10% | 7.50 |
| **Total blended CAC** | **100%** | **75.00** |

**Note:** First-job credit (AED 30) amortized as acquisition cost, not COGS.

---

## Lifetime Value (LTV)

### LTV Calculation

```
LTV = Average jobs per customer (lifetime) × Contribution margin per job
```

| Input | Launch | Year 1 Mature | Year 3 |
|-------|--------|---------------|--------|
| Avg jobs/customer (24 months) | 1.4 | 1.8 | 2.5 |
| Contribution margin/job (AED) | 18 | 22 | 25 |
| **LTV (AED)** | **25** | **40** | **63** |
| **LTV (USD)** | **$7** | **$11** | **$17** |

### LTV Sensitivity

| Variable | −20% LTV Impact | +20% LTV Impact |
|----------|-----------------|-----------------|
| Jobs/customer (1.8 base) | LTV = AED 32 | LTV = AED 48 |
| Contribution/job (AED 22) | LTV = AED 32 | LTV = AED 48 |
| Retention period | LTV = AED 32 | LTV = AED 48 |

**Key insight:** LTV is low in Year 1 because roadside assistance is inherently low-frequency (1–2 jobs/year). Retention and repeat rate are the primary LTV levers.

---

## LTV:CAC Ratio Targets

| Period | LTV (AED) | CAC (AED) | LTV:CAC | Status |
|--------|-----------|-----------|---------|--------|
| Launch (M1–3) | 25 | 75 | 0.33:1 | Expected (investment phase) |
| Month 6 | 32 | 60 | 0.53:1 | Building |
| Month 12 | 40 | 50 | 0.80:1 | Approaching |
| Month 18 | 48 | 42 | 1.14:1 | Improving |
| Month 24 | 55 | 38 | 1.45:1 | Growth efficient |
| Month 30 | 60 | 35 | 1.71:1 | Near target |
| Month 36 | 63 | 35 | 1.80:1 | **Approaching 3:1 with subscription** |

### LTV with Subscription (Phase 2)

| Element | Addition to LTV |
|---------|---------------|
| Roadside subscription (AED 99/year, 30% margin) | +AED 30/year × 2 years = AED 60 |
| **Adjusted LTV (Year 3 with subscription)** | **AED 123** |
| **Adjusted LTV:CAC** | **3.5:1** |

Subscription product (Phase 2) is critical to reaching 3:1 LTV:CAC in a low-frequency category.

---

## CAC by Channel

| Channel | CAC (AED) | Volume Potential | LTV Quality | Priority |
|---------|-----------|------------------|-------------|----------|
| **Referral** | 25 | Medium | High (trust-based) | High |
| **Roadside QR signage** | 15 | Medium | High (emergency context) | High |
| **Insurance B2B2C** | 10 | High (at maturity) | High | High (Year 2) |
| **SEO (organic)** | 20 | Medium | Medium | Medium |
| **App Store organic** | 0 | Low-Medium | Medium | Medium |
| **Performance marketing** | 55 | High | Medium | Medium (controlled) |
| **Dealership partnerships** | 35 | Medium | Medium-High | Medium |
| **Social media paid** | 65 | High | Low-Medium | Low (test only) |

**Channel strategy:** Prioritize low-CAC, high-LTV channels (referral, QR, B2B2C) over paid performance marketing.

---

## Cohort Retention & LTV Build

### Customer Repeat Rate

| Cohort | D30 Repeat | D90 Repeat | D365 Repeat | Lifetime Jobs |
|--------|------------|------------|-------------|---------------|
| Launch (M1) | 5% | 8% | 15% | 1.2 |
| M6 cohort | 8% | 12% | 20% | 1.4 |
| M12 cohort | 12% | 18% | 25% | 1.8 |
| Year 2 target | 15% | 22% | 30% | 2.2 |
| Year 3 target | 18% | 28% | 35% | 2.5 |

*Repeat = customer completes second job.*

### Retention Drivers

| Driver | Impact on Repeat Rate |
|--------|----------------------|
| First job NPS ≥50 | +8% D365 repeat |
| Saved vehicle profile | +5% D365 repeat |
| Referral program participation | +3% D365 repeat |
| Subscription (Phase 2) | +15% annual retention |
| Seasonal (summer battery failures) | Natural +10% for summer cohorts |

---

## Payback Period

| Period | CAC (AED) | Monthly Contribution/Customer | Payback (Months) |
|--------|-----------|-------------------------------|------------------|
| Launch | 75 | 2.50 (1 job/30 days × AED 18 margin / 12 mo) | 30 months |
| Year 1 mature | 50 | 3.30 | 15 months |
| Year 2 | 40 | 4.50 | 9 months |
| Year 3 (with subscription) | 35 | 6.50 | 5 months |

**Target payback:** ≤12 months by Year 2.

Low-frequency category means payback is inherently longer than ride-hail (payback <6 months) unless subscription or B2B2C channels dominate.

---

## B2B Customer Economics

B2B customers (insurers, fleets) have different economics:

| Metric | B2B Partner | B2B End User (Policyholder/Driver) |
|--------|-------------|-------------------------------------|
| Acquisition cost | AED 50K–200K (sales cycle) | AED 10 (partner-subsidized) |
| Jobs per year | 5,000–50,000 per partner | 0.5–1.0 |
| Revenue per job | AED 30–35 (lower commission) | — |
| LTV (partner, 3-year contract) | AED 450K–2.7M | AED 15–25 |
| LTV:CAC (partner) | 9:1–13:1 | 1.5:1–2.5:1 |

**Strategy:** Anchor B2B partnerships for volume and low effective CAC; B2C for brand and direct relationship.

---

## Marketing Budget Allocation

### Year 1 Marketing Budget: AED 1.8M (~$490K)

| Category | Budget (AED) | % | Expected Customers | CAC |
|----------|--------------|---|-------------------|-----|
| Performance marketing | 720,000 | 40% | 13,000 | 55 |
| Referral program | 360,000 | 20% | 14,400 | 25 |
| Partnerships & B2B2C setup | 270,000 | 15% | 5,000 | 54 |
| Launch promotions (credits) | 270,000 | 15% | 9,000 | 30 |
| Brand & content | 180,000 | 10% | — | — |
| **Total** | **1,800,000** | **100%** | **~41,400 new** | **~44 blended** |

*Note: Not all customers are unique (some channels overlap); 41K new customers from 85K jobs implies ~47% new customer rate.*

---

## Business Examples

**Example 1 — Referral acquisition:** Customer A refers Customer B. Customer B completes first job. Cost: AED 30 credit to A + AED 30 credit to B = AED 60. Customer B LTV (projected): AED 40. LTV:CAC = 0.67:1 initially; if B refers Customer C, effective CAC drops to AED 30 (AED 60/2 referrals). **Referral loop improves economics.**

**Example 2 — QR highway signage:** AED 5,000 per highway sign installation. Sign generates 40 new customers/month. Monthly cost: AED 5,000/12 (amortized) = AED 417 + maintenance AED 100 = AED 517. CAC: AED 517/40 = AED 13. LTV: AED 40. LTV:CAC = 3.1:1. **Highly efficient channel.**

**Example 3 — Paid search emergency keyword:** "Tow truck Dubai" CPC AED 8. Conversion to completed job: 12%. CAC: AED 8/0.12 = AED 67. Plus AED 30 first-job credit = AED 97 total. LTV: AED 35 (emergency first-timers repeat less). LTV:CAC = 0.36:1. **Unprofitable alone; acceptable for brand presence and app install.**

**Example 4 — Insurance B2B2C:** Insurer partnership costs AED 100K to establish (sales, integration, co-marketing). Insurer routes 3,000 jobs/year. Effective CAC per end user: AED 100K/3,000 = AED 33. Platform revenue per job: AED 35. Single job exceeds CAC. **Highly efficient at volume.**

---

## Business Decisions

| Decision | Rationale |
|----------|-----------|
| Accept LTV:CAC <1 in Year 1 | Low-frequency category requires patience; focus on channel efficiency trend |
| Prioritize referral and QR over paid | Better LTV:CAC; emergency intent captured at moment of need |
| Invest in B2B2C from Month 6 | Lowest effective CAC at scale despite long sales cycle |
| Phase 2 subscription to boost LTV | Required to reach 3:1 LTV:CAC in standalone B2C |
| Cap performance marketing at 40% of budget | Prevent CAC inflation from competitive bidding |
| AED 30 first-job credit as CAC not COGS | Correct accounting; reflects acquisition investment |

---

## Risks

| Risk | Impact | Mitigation |
|------|--------|------------|
| LTV lower than projected (no repeat) | High | Subscription; preparedness marketing; referral loops |
| CAC inflation in paid channels | Medium | Channel diversification; organic investment |
| B2B partnership delays | High | B2C channel efficiency; extend timeline |
| Referral fraud | Low | Job completion requirement; account verification |
| Competitor customer subsidies | Medium | Differentiate on quality/trust, not price alone |

---

## Assumptions

- 47% of Year 1 jobs from first-time customers (rest repeat)
- Average customer completes 1.8 jobs over 24 months (Year 1 mature)
- Referral program achieves 12% of new customers by Month 12
- Insurance B2B2C live Month 6 with 400 jobs/month growing to 2,500
- Subscription product launches Month 15 with 5% adoption Year 1
- Marketing spend efficiency improves 10% per quarter (learning curve)

---

## Open Questions

- Include brand marketing in CAC or separate?
- Provider-as-acquisition-channel (provider refers customer)?
- CAC target for KSA launch — higher or lower than UAE?
- Lifetime defined as 24 or 36 months for LTV calculation?

---

## Next Steps

1. Implement channel-level CAC tracking from launch day
2. Build cohort retention dashboard (D30, D90, D365)
3. Set monthly marketing spend caps by channel based on LTV:CAC
4. Launch referral program before consumer go-live
5. Begin insurance B2B partnership sales for Month 6 CAC reduction
