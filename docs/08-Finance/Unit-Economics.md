# Unit Economics — Salik Assist

| Field | Value |
|-------|-------|
| **Version** | 1.0 |
| **Status** | Draft |
| **Author** | Product & Strategy Team |
| **Last Updated** | July 4, 2026 |

## Purpose

Define and analyze the unit economics of a single Salik Assist marketplace job—establishing contribution margin, cost structure, and path to profitability per transaction and at scale.

## Scope

Per-job and per-customer economic analysis for UAE B2C operations at launch and maturity. Excludes corporate overhead allocation detail and technical cost modeling.

## Related Documents

- [Revenue Forecast](./Revenue-Forecast.md)
- [CAC-LTV](./CAC-LTV.md)
- [Financial Assumptions](./Financial-Assumptions.md)
- [Provider Agreement](../07-Legal/Provider-Agreement.md)
- [Executive Summary](../01-Executive/Executive-Summary.md)

## Table of Contents

1. [Unit Economics Overview](#unit-economics-overview)
2. [Per-Job Economics (B2C)](#per-job-economics-b2c)
3. [Per-Job Economics (B2B)](#per-job-economics-b2b)
4. [Cost Structure Breakdown](#cost-structure-breakdown)
5. [Contribution Margin Analysis](#contribution-margin-analysis)
6. [Unit Economics by Service Category](#unit-economics-by-service-category)
7. [Scale Effects](#scale-effects)
8. [Break-Even Analysis](#break-even-analysis)
9. [Benchmark Comparison](#benchmark-comparison)
10. [Business Examples](#business-examples)
11. [Business Decisions](#business-decisions)
12. [Risks](#risks)
13. [Assumptions](#assumptions)
14. [Open Questions](#open-questions)
15. [Next Steps](#next-steps)

---

## Unit Economics Overview

Salik Assist unit economics measured at three levels:

| Level | Primary Metric | Target |
|-------|----------------|--------|
| **Per job** | Contribution margin per completed job | ≥AED 22 at maturity |
| **Per customer** | LTV:CAC ratio | ≥3:1 by Month 12 |
| **Per provider** | Revenue per active provider per month | ≥AED 1,800 |

**North star unit metric:** Contribution margin per job ≥ 12% of GMV at Year 1 maturity.

---

## Per-Job Economics (B2C)

### Standard Tow Job (Base Case)

| Line Item | AED | % of GMV |
|-----------|-----|----------|
| **GMV (customer payment)** | 280.00 | 100% |
| Provider payout (82%) | (229.60) | 82% |
| **Platform revenue (commission 18%)** | **50.40** | **18%** |
| Payment processing (2.9% + AED 1) | (9.12) | 3.3% |
| Support cost (allocated) | (3.50) | 1.3% |
| Verification/quality (allocated) | (1.20) | 0.4% |
| SLA remedy reserve | (2.80) | 1.0% |
| **Contribution margin** | **33.78** | **12.1%** |

### Blended Average Job (All Categories)

| Line Item | AED | % of GMV |
|-----------|-----|----------|
| **GMV** | 181.00 | 100% |
| Provider payout | (148.42) | 82% |
| **Platform revenue** | **32.58** | **18%** |
| Variable costs | (10.86) | 6.0% |
| **Contribution margin** | **21.72** | **12.0%** |

---

## Per-Job Economics (B2B)

### Insurance Dispatch Job

| Line Item | AED | % of GMV |
|-----------|-----|----------|
| **GMV (insurer billed)** | 250.00 | 100% |
| Provider payout (88%) | (220.00) | 88% |
| **Platform revenue (12% + AED 5 fee)** | **35.00** | **14%** |
| Variable costs | (8.50) | 3.4% |
| **Contribution margin** | **26.50** | **10.6%** |

B2B lower commission offset by lower CAC (partner-sourced demand) and higher job volume per customer.

---

## Cost Structure Breakdown

### Variable Costs Per Job

| Cost Category | Launch (AED) | Mature (AED) | Driver |
|---------------|--------------|--------------|--------|
| Payment processing | 6.25 | 5.50 | Negotiated rates at volume |
| Customer support | 4.20 | 3.50 | Self-service + automation |
| Provider support | 1.80 | 1.20 | Scale efficiencies |
| Quality/remedy reserve | 3.50 | 2.80 | SLA improvement |
| Verification (amortized) | 2.10 | 0.80 | Provider density |
| **Total variable cost** | **17.85** | **13.80** | |

### Fixed Costs (Monthly, Year 1)

| Category | AED/Month | Per Job (at 7,000 jobs/mo) |
|----------|-----------|----------------------------|
| Team (ops, support, sales) | 420,000 | 60.00 |
| Marketing (non-CAC brand) | 85,000 | 12.14 |
| Office & admin | 45,000 | 6.43 |
| Legal & compliance | 25,000 | 3.57 |
| **Total fixed** | **575,000** | **82.14** |

**Fully loaded cost per job (Year 1 avg):** AED 17.85 variable + AED 82.14 fixed = AED 99.99 → **Not profitable per job until ~Month 22** when fixed cost spread over ~12,000+ jobs/month.

---

## Contribution Margin Analysis

| Period | Avg GMV | Platform Revenue | Variable Cost | Contribution Margin | CM % |
|--------|---------|------------------|---------------|---------------------|------|
| Launch (M1–3) | 175 | 24.50* | 17.85 | 6.65 | 3.8% |
| Growth (M4–9) | 181 | 32.58 | 15.20 | 17.38 | 9.6% |
| Mature (M10–12) | 188 | 33.84 | 13.80 | 20.04 | 10.7% |
| Year 2 avg | 193 | 34.35 | 12.50 | 21.85 | 11.3% |
| Year 3 avg | 197 | 35.66 | 11.20 | 24.46 | 12.4% |

*Lower revenue due to 0% commission launch promo in early months.*

---

## Unit Economics by Service Category

| Category | Avg GMV (AED) | Commission (AED) | Variable Cost (AED) | Contribution (AED) | CM % |
|----------|---------------|------------------|---------------------|--------------------|----- |
| **Tow** | 280 | 50.40 | 18.50 | 31.90 | 11.4% |
| **Battery** | 150 | 27.00 | 14.20 | 12.80 | 8.5% |
| **Tire** | 120 | 21.60 | 13.80 | 7.80 | 6.5% |
| **Fuel** | 95 | 17.10 | 13.50 | 3.60 | 3.8% |
| **Mobile mechanic** | 220 | 39.60 | 16.80 | 22.80 | 10.4% |
| **Lockout** | 130 | 23.40 | 14.00 | 9.40 | 7.2% |

**Insight:** Tow and mobile mechanic drive margin; fuel and tire are volume/entry categories with lower margin but high acquisition value.

---

## Scale Effects

| Jobs/Month | Fixed Cost/Job (AED) | Contribution/Job (AED) | Net Margin/Job (AED) |
|------------|----------------------|------------------------|----------------------|
| 2,000 | 287.50 | 17.38 | (270.12) |
| 5,000 | 115.00 | 19.00 | (96.00) |
| 7,000 | 82.14 | 20.04 | (62.10) |
| 10,000 | 57.50 | 21.00 | (36.50) |
| 15,000 | 38.33 | 22.50 | (15.83) |
| 20,000 | 28.75 | 23.00 | (5.75) |
| 27,000 | 21.30 | 24.00 | 2.70 |
| 35,000 | 16.43 | 24.50 | 8.07 |

**Break-even volume:** ~27,000 jobs/month (Year 2 Q3 trajectory with UAE expansion).

---

## Break-Even Analysis

| Metric | Value |
|--------|-------|
| Monthly fixed costs (Year 1 avg) | AED 575,000 |
| Contribution margin per job (mature) | AED 24.00 |
| Break-even jobs/month | 23,958 |
| Break-even jobs/day | 799 |
| Expected break-even month | Month 22–26 |
| Break-even active providers needed | ~400 at 2 jobs/provider/day |

---

## Benchmark Comparison

| Marketplace | Reported Take Rate | Est. Contribution Margin | Notes |
|-------------|-------------------|--------------------------|-------|
| **Salik Assist (target)** | 18% | 12% of GMV | Roadside assistance |
| Ride-hail (UAE) | 20–25% | 15–18% | Higher frequency; lower AOV |
| Food delivery | 25–35% | 8–12% | Higher marketing intensity |
| Home services marketplace | 15–20% | 10–15% | Similar job-based model |
| Insurance roadside (traditional) | N/A (owned) | Unknown | Salik B2B competes here |

Salik Assist targets margin profile similar to home services marketplaces with lower frequency but higher AOV.

---

## Business Examples

**Example 1 — Profitable mature job:** Year 2 tow job, AED 300 GMV. Commission AED 54. Variable cost AED 14. Contribution AED 40. Fixed cost allocation at 20K jobs/month: AED 29. Net margin AED 11. **Profitable.**

**Example 2 — Launch promo job (Month 2):** Battery jump, AED 140 GMV. Commission AED 0 (promo). Variable cost AED 16. Contribution AED −16. **Loss leader** for provider acquisition and customer habit.

**Example 3 — B2B fleet job at scale:** Fleet tow, AED 230 contracted. Platform revenue AED 32.60 (12% + fee). Variable cost AED 8. CAC effectively zero (fleet-sourced). Contribution AED 24.60. **Highly profitable** unit despite lower commission.

**Example 4 — SLA remedy impact:** Tow job contribution AED 35 before remedy. ETA breach triggers 25% customer refund (AED 70). Remedy cost AED 70; platform absorbs (provider fault). Net contribution: AED −35. Remedy reserve (AED 2.80/job avg) covers ~4% of jobs at this severity.

---

## Business Decisions

| Decision | Rationale |
|----------|-----------|
| Target 12% contribution margin | Sustainable for marketplace with emergency support costs |
| Accept negative margin during launch promo | Customer and provider acquisition investment |
| Prioritize tow/battery categories | Highest contribution margin categories |
| B2B lower commission but zero CAC | Net unit economics favorable at scale |
| SLA remedy reserve at 1% of GMV | Predictable cost vs. surprise refund hits |
| Break-even at ~24K jobs/month | Achievable Month 22–26 with expansion plan |

---

## Risks

| Risk | Impact | Mitigation |
|------|--------|------------|
| Variable costs higher than modeled | Medium | Payment processor negotiation; support automation |
| AOV lower than AED 181 | High | Category mix management; surge pricing |
| Remedy costs exceed 1% reserve | Medium | SLA improvement; provider accountability |
| Fixed cost creep | Medium | Hiring gates tied to volume milestones |
| Fuel/tire categories dilute margin | Low | Cross-subsidize with tow; limit marketing on low-margin categories |

---

## Assumptions

- 18% blended commission (excluding launch promo period)
- Payment processing at 2.9% + AED 1.00 per transaction
- 12% of jobs generate support contact at AED 3.50 avg cost
- SLA remedies affect 4% of jobs at AED 35 avg cost
- Fixed costs grow 15% YoY (team scaling) while jobs grow 275% YoY
- Provider payout is 82% of GMV (18% commission)

---

## Open Questions

- Include provider subscription revenue in per-job economics or separate?
- Allocate marketing CAC to per-job or per-customer only?
- Minimum AOV floor by category to maintain margin?
- Dynamic commission by category (tow 18%, fuel 22%)?

---

## Next Steps

1. Build unit economics calculator (spreadsheet) with scenario toggles
2. Validate payment processing rates with acquirer quotes
3. Track actual contribution margin per job from Month 1 launch
4. Monthly unit economics review in finance/ops meeting
5. Set category-specific marketing spend caps based on margin profile
