# KPIs — Salik Assist

| Field | Value |
|-------|-------|
| **Version** | 1.0 |
| **Status** | Draft |
| **Author** | Product & Strategy Team |
| **Last Updated** | July 4, 2026 |

## Purpose

Define the Key Performance Indicators (KPIs) that operationalize Salik Assist's [North Star Metric](./North-Star-Metric.md) and [Product Strategy](./Product-Strategy.md). This document provides definitions, formulas, targets, owners, and reporting standards for ongoing business measurement.

## Scope

Business and product KPIs across demand, supply, marketplace health, financial performance, quality, and partnerships. Excludes technical monitoring, system uptime metrics, and engineering velocity measures.

## Related Documents

- [North Star Metric](./North-Star-Metric.md)
- [OKRs](./OKRs.md)
- [Success Metrics](../01-Executive/Success-Metrics.md)
- [Product Strategy](./Product-Strategy.md)
- [Unit Economics](../08-Finance/Unit-Economics.md)
- [CAC-LTV](../08-Finance/CAC-LTV.md)
- [Revenue Forecast](../08-Finance/Revenue-Forecast.md)
- [SLA](../06-Operations/SLA.md)
- [Pricing Strategy](../04-Business/Pricing-Strategy.md)

## Table of Contents

1. [KPI Hierarchy](#kpi-hierarchy)
2. [North Star KPI](#north-star-kpi)
3. [Growth KPIs](#growth-kpis)
4. [Marketplace Liquidity KPIs](#marketplace-liquidity-kpis)
5. [Fulfillment KPIs](#fulfillment-kpis)
6. [Supply-Side KPIs](#supply-side-kpis)
7. [Demand-Side KPIs](#demand-side-kpis)
8. [Financial KPIs](#financial-kpis)
9. [Quality and Trust KPIs](#quality-and-trust-kpis)
10. [B2B Partnership KPIs](#b2b-partnership-kpis)
11. [KPI Dashboards and Ownership](#kpi-dashboards-and-ownership)
12. [Business Examples](#business-examples)
13. [Business Decisions](#business-decisions)
14. [Risks](#risks)
15. [Assumptions](#assumptions)
16. [Open Questions](#open-questions)
17. [Next Steps](#next-steps)

---

## KPI Hierarchy

| Tier | KPIs | Audience | Cadence |
|------|------|----------|---------|
| **L1 — North Star** | SCAJ | CEO, board, all teams | Daily / weekly |
| **L2 — Strategic** | GMV, liquidity, NPS, active providers | Executives | Weekly / monthly |
| **L3 — Operational** | TTFO, fill rate, CAC, SLA breach | Functional leads | Daily |
| **L4 — Diagnostic** | Funnel conversion, zone heatmaps | Product, analytics | Ad hoc |

---

## North Star KPI

### Successfully Completed Assisted Jobs (SCAJ)

| Attribute | Value |
|-----------|-------|
| **Definition** | Jobs meeting full completion criteria per [North Star Metric](./North-Star-Metric.md) |
| **Formula** | `COUNT(completed_jobs WHERE all_conditions_met)` |
| **Y1 Target** | 85,000 annual; 10,500/month by M12 |
| **Owner** | GM |
| **Cadence** | Daily pulse; weekly exec review |

---

## Growth KPIs

| KPI | Definition | Formula | Y1 Target | Owner |
|-----|------------|---------|-----------|-------|
| **Monthly SCAJ Growth Rate** | WoW or MoM SCAJ change | `(SCAJ_t - SCAJ_t-1) / SCAJ_t-1` | ≥8% MoM (post-launch) | GM |
| **Registered Customers** | Verified customer accounts | `COUNT(customers WHERE verified)` | 95,000 | Growth |
| **Monthly Active Requesters (MAR)** | Unique customers requesting/month | `COUNT(DISTINCT customer_id REQUEST in month)` | 18,000 by M12 | Growth |
| **New Requester Acquisition** | First-time requesters/month | `COUNT(customers FIRST_REQUEST in month)` | Track vs plan | Growth |
| **Referral Rate** | Referral-attributed requests / total | `referral_requests / total_requests` | ≥15% by M9 | Growth |
| **Organic Share** | Non-paid requests / total | `organic_requests / total_requests` | ≥40% by M12 | Marketing |

---

## Marketplace Liquidity KPIs

| KPI | Definition | Formula | Y1 Target | Owner |
|-----|------------|---------|-----------|-------|
| **Liquidity Index** | Requests with ≥3 offers within 5 min | `eligible_3offer_5min / total_requests` | ≥65% | Operations |
| **Top-3 Delivery Rate** | Jobs where customer saw 3 offers before accept | `jobs_3offers / total_accepted` | ≥60% | Product |
| **Time to First Offer (TTFO)** | Median request → first offer | `MEDIAN(offer_time - request_time)` | ≤3 min | Product |
| **Time to Three Offers (TT3O)** | Median request → third offer | `MEDIAN(third_offer_time - request_time)` | ≤5 min | Operations |
| **Offer Response Rate** | Eligible providers responding in window | `responses / eligible_pings` | ≥60% | Operations |
| **Zone Coverage Score** | Land area with 3+ providers within 15 km | GIS analysis per zone | ≥90% launch zones | Operations |
| **Supply Stress Index** | Requests with only 0–1 offers | `low_offer_requests / total` | ≤15% | Operations |

---

## Fulfillment KPIs

| KPI | Definition | Formula | Y1 Target | Owner |
|-----|------------|---------|-----------|-------|
| **Match Rate** | Requests receiving ≥1 accepted offer | `accepted_requests / total_requests` | ≥78% | Product |
| **Acceptance Rate** | Requests with offers → customer accepts | `acceptances / offers_shown` | ≥65% | Product |
| **Fill Rate** | Accepted offers → completed | `completions / acceptances` | ≥92% | Operations |
| **Time to Accept (TTA)** | Median request → acceptance | `MEDIAN(accept_time - request_time)` | ≤8 min | Product |
| **Time to Arrive (TTAar)** | Median acceptance → on-site | `MEDIAN(arrival_time - accept_time)` | Category SLA | Operations |
| **Customer Cancellation Rate** | Pre-arrival customer cancels | `cust_cancel / acceptances` | ≤12% | Support |
| **Provider Cancellation Rate** | Post-accept provider cancels | `prov_cancel / acceptances` | ≤5% | Operations |

---

## Supply-Side KPIs

| KPI | Definition | Formula | Y1 Target | Owner |
|-----|------------|---------|-----------|-------|
| **Verified Providers (total)** | Passed verification, active status | `COUNT(providers WHERE verified)` | 150 launch; 200 M6 | Operations |
| **Active Providers (30-day)** | ≥1 SCAJ in last 30 days | `COUNT(providers SCAJ in 30d)` | 120 | Operations |
| **Provider Activation Rate** | Registered → first SCAJ within 14 days | `first_job_14d / new_registrations` | ≥55% | Operations |
| **Provider Retention (90-day)** | Month-1 actives still active month 4 | Cohort retention | ≥70% | Operations |
| **Provider Utilization** | SCAJ per active provider per month | `SCAJ / active_providers / month` | 12–25 | Operations |
| **Provider Earnings (median)** | Monthly net payout per active provider | `MEDIAN(provider_payout)` | AED 3,500+ | Finance |
| **Provider NPS** | Quarterly survey | Standard NPS | ≥35 | Operations |

---

## Demand-Side KPIs

| KPI | Definition | Formula | Y1 Target | Owner |
|-----|------------|---------|-----------|-------|
| **Customer CAC** | Blended acquisition cost | `sales_marketing_spend / new_customers` | ≤$18 | Growth |
| **Customer LTV (24-mo)** | Projected net contribution/customer | Model-based | ≥$45 | Finance |
| **LTV:CAC Ratio** | LTV / CAC | `LTV / CAC` | ≥3:1 by M12 | Finance |
| **Repeat Rate (90-day)** | Customers with 2+ SCAJ in 90 days | Cohort analysis | ≥12% | Product |
| **CSAT (post-job)** | 1–5 satisfaction survey | `AVG(csat_score)` | ≥4.4 | Support |
| **Customer NPS** | Promoters − detractors | Standard NPS | ≥35 | Product |
| **App Store Rating** | Weighted iOS/Android | Platform aggregate | ≥4.5 | Marketing |

---

## Financial KPIs

| KPI | Definition | Formula | Y1 Target | Owner |
|-----|------------|---------|-----------|-------|
| **GMV** | Total customer-paid job value | `SUM(job_value)` | $4.2M | Finance |
| **Net Revenue** | Commissions + subscriptions + B2B fees | `SUM(platform_revenue)` | $756K | Finance |
| **Take Rate (net)** | Net revenue / GMV | `net_revenue / GMV` | 16–18% | Finance |
| **Average Order Value (AOV)** | GMV / SCAJ | `GMV / SCAJ` | AED 200–280 | Finance |
| **Contribution Margin** | (Net revenue − variable costs) / net revenue | Per job and aggregate | Positive by M9 | Finance |
| **CAC Payback** | Months to recover CAC | Model-based | ≤8 months | Finance |
| **Refund Rate** | Refunded GMV / total GMV | `refunds / GMV` | ≤2.5% | Finance |
| **Gross Margin** | Platform gross margin | Per finance model | 72% | Finance |

---

## Quality and Trust KPIs

| KPI | Definition | Formula | Y1 Target | Owner |
|-----|------------|---------|-----------|-------|
| **Average Provider Rating** | Post-job star average | `AVG(rating)` | ≥4.6 | Product |
| **Dispute Rate** | Disputes / SCAJ | `disputes / SCAJ` | ≤4% | Support |
| **Dispute Resolution Time** | Median hours to resolve | `MEDIAN(resolve_time)` | ≤48h | Support |
| **SLA Breach Rate** | Jobs missing arrival SLA | `breaches / SCAJ` | ≤8% | Operations |
| **Safety Incident Rate** | Verified complaints per 10K jobs | `safety_cases / (SCAJ/10000)` | ≤2 | Compliance |
| **Verification Compliance** | Active providers with valid docs | `valid_docs / active_providers` | 100% | Compliance |
| **No-Show Rate** | Provider no-shows / acceptances | `noshows / acceptances` | ≤3% | Operations |

---

## B2B Partnership KPIs

| KPI | Definition | Formula | Y1 Target | Owner |
|-----|------------|---------|-----------|-------|
| **B2B Job Share** | B2B SCAJ / total SCAJ | `b2b_scaj / total_scaj` | ≥8% M6; ≥15% M12 | Partnerships |
| **B2B Contracts (active)** | Signed enterprise agreements | `COUNT(active_contracts)` | 1 M6; 2 M12 | Partnerships |
| **B2B SLA Adherence** | Partner jobs meeting SLA | `sla_met / b2b_jobs` | ≥95% | Operations |
| **B2B Revenue Share** | B2B fees / net revenue | `b2b_revenue / net_revenue` | ≥12% M12 | Finance |
| **Partner Churn** | Lost contracts / total | Annualized | ≤10% | Partnerships |
| **B2B Pipeline** | Qualified partner opportunities | CRM stage-weighted | 5+ in pipeline | Partnerships |

---

## KPI Dashboards and Ownership

| Dashboard | Primary KPIs | Audience | Update |
|-----------|--------------|----------|--------|
| **Daily Pulse** | SCAJ, TTFO, fill rate, cancellations | Ops + GM | Real-time |
| **Weekly Growth** | MAR, CAC, referral, SCAJ WoW | Exec + Growth | Weekly Mon |
| **Monthly Board** | L1–L2 full suite, financials | Board | Monthly |
| **Zone Heatmap** | Liquidity, SCAJ, supply stress by zone | City manager | Daily |
| **Provider Scorecard** | Utilization, rating, cancellation | Provider ops | Weekly |
| **B2B Partner View** | B2B SCAJ, SLA, revenue | Partnerships | Weekly |

**Data stewardship:** Finance owns revenue KPIs; Product Ops owns marketplace definitions; Operations owns supply KPIs. Definition changes require cross-functional sign-off.

---

## Business Examples

**Example 1 — Liquidity KPI triggers action:** Dubai Marina Liquidity Index drops to 58% for 2 weeks. Supply Stress Index rises to 22%. Operations KPI review triggers recruitment of 10 battery providers; Marketing pauses Marina geo-targeted ads until Index recovers to 65%.

**Example 2 — Fill rate diagnostic:** Match Rate healthy at 80% but Fill Rate 85% (below 92% target). Diagnostic KPIs show Provider Cancellation Rate at 8%. Root cause: payout delays. Finance KPI owner targets 48-hour payout; Fill Rate recovers to 91% in 3 weeks.

**Example 3 — Unit economics KPI:** Customer CAC $24 exceeds $18 target via paid social. LTV:CAC for paid social cohort 1.8:1. Growth shifts budget to referral (CAC $9, LTV:CAC 4.2:1). Blended CAC returns to $17.

**Example 4 — Top-3 delivery tracking:** Top-3 Delivery Rate only 48% despite 65% Liquidity Index—investigation shows customers accepting before third offer arrives. Product adjusts UX to encourage comparison without blocking fast acceptance; rate rises to 62%.

---

## Business Decisions

| Decision | Rationale |
|----------|-----------|
| Liquidity Index as co-primary executive KPI | Without offers, SCAJ cannot scale |
| Zone-level reporting mandatory | City averages mask deserts |
| Separate B2B KPI suite | Different sales cycle and SLA |
| Fill rate over match rate for ops bonuses | Acceptance without completion wastes trust |
| Provider retention weighted over raw sign-ups | Quality supply beats vanity registration |
| Contribution margin tracked from M6 | Growth must trend toward sustainability |

---

## Risks

| Risk | KPI Impact |
|------|------------|
| Definition drift across teams | Incomparable reports; decision paralysis |
| KPI gaming (fake SCAJ) | Inflated North Star |
| Over-dashboarding | Analysis paralysis; slow decisions |
| Lagging financial KPIs | Monthly GMV miss discovered too late |
| Vanity MAR inflation | Registrations without requests |

---

## Assumptions

- KPI targets calibrated to Dubai-only Year 1 scope
- Baseline benchmarks from mobility marketplace comparables
- Weekly exec review discipline maintained post-launch
- Zone geography stable for 6 months post-launch

---

## Open Questions

- Real-time investor/partner KPI sharing portal?
- Weight KPIs differently by quarter (pre-launch vs scale)?
- Provider-facing KPI dashboard (their own stats only)?
- Include carbon/EV KPIs in Year 1 or defer?

---

## Next Steps

1. Publish KPI dictionary with formulas to all team leads
2. Assign dashboard owners and data stewards
3. Configure Daily Pulse and Weekly Growth templates
4. Align [OKRs](./OKRs.md) KRs to specific KPIs in this document
5. Baseline mystery shopper metrics pre-launch for TTFO/TTA benchmarks
