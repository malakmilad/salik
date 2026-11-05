# Success Metrics — Salik Assist

| Field | Value |
|-------|-------|
| **Version** | 1.0 |
| **Status** | Draft |
| **Author** | Product & Strategy Team |
| **Last Updated** | July 4, 2026 |

## Purpose

Define the canonical success metrics framework—how Salik Assist measures progress toward strategic objectives at executive, product, and operational levels.

## Scope

Metric definitions, formulas, targets, and reporting cadence. Technical instrumentation specifications are out of scope.

## Related Documents

- [Objectives](./Objectives.md)
- [North Star Metric](../05-Product-Strategy/North-Star-Metric.md)
- [KPIs](../05-Product-Strategy/KPIs.md)
- [OKRs](../05-Product-Strategy/OKRs.md)
- [SLA](../06-Operations/SLA.md)
- [Unit Economics](../08-Finance/Unit-Economics.md)

## Table of Contents

1. [Metrics Hierarchy](#metrics-hierarchy)
2. [North Star Metric](#north-star-metric)
3. [Primary Success Metrics](#primary-success-metrics)
4. [Supply-Side Metrics](#supply-side-metrics)
5. [Demand-Side Metrics](#demand-side-metrics)
6. [Marketplace Health Metrics](#marketplace-health-metrics)
7. [Financial Success Metrics](#financial-success-metrics)
8. [Quality & Trust Metrics](#quality--trust-metrics)
9. [B2B Success Metrics](#b2b-success-metrics)
10. [Reporting Cadence](#reporting-cadence)
11. [Business Examples](#business-examples)
12. [Business Decisions](#business-decisions)
13. [Risks](#risks)
14. [Assumptions](#assumptions)
15. [Open Questions](#open-questions)
16. [Next Steps](#next-steps)

---

## Metrics Hierarchy

| Level | Audience | Horizon | Example |
|-------|----------|---------|---------|
| **L1 — North Star** | Company | Real-time / weekly | Successfully completed assisted jobs |
| **L2 — Strategic KPIs** | Executives, board | Monthly | GMV, NPS, liquidity index |
| **L3 — Operational KPIs** | Ops, support, city teams | Daily | ETA adherence, offer response rate |
| **L4 — Diagnostic metrics** | Product, analytics | Ad hoc | Funnel drop-off by step |

---

## North Star Metric

**Successfully Completed Assisted Jobs (SCAJ)**

A job counts when:
1. Customer created a valid request
2. Customer accepted a provider offer
3. Provider marked service completed
4. Payment captured or B2B invoice recorded
5. No unresolved fraud flag

**Why:** Captures both sides of marketplace value—demand fulfilled and supply paid—unlike raw downloads or requests alone.

Detail: [North Star Metric](../05-Product-Strategy/North-Star-Metric.md)

---

## Primary Success Metrics

| Metric | Definition | Y1 Target | Y3 Target |
|--------|------------|-----------|-----------|
| SCAJ | See above | 85,000 / year | 780,000 / year |
| GMV | Total customer-paid job value | $4.2M | $42M |
| Net Revenue | Commissions + subscriptions + B2B fees | $756K | $7.6M |
| Liquidity Index | % requests receiving ≥3 offers within 5 min | 65% | 85% |
| Match Rate | % requests with ≥1 accepted offer | 78% | 88% |

---

## Supply-Side Metrics

| Metric | Definition | Target |
|--------|------------|--------|
| Active Providers | ≥1 completed job in last 30 days | Y1: 120; Y3: 2,000 |
| Provider Activation Rate | Registered → first completed job within 14 days | ≥55% |
| Provider Retention (90-day) | Providers active in month 1 still active in month 4 | ≥70% |
| Offer Response Rate | Eligible providers responding within SLA window | ≥60% |
| Provider Utilization | Completed jobs / active provider / month | 12–25 (zone dependent) |
| Provider NPS | Quarterly survey | ≥35 Y1; ≥40 Y3 |
| Document Compliance Rate | Providers with valid credentials | 100% active |

---

## Demand-Side Metrics

| Metric | Definition | Target |
|--------|------------|--------|
| Registered Customers | Verified accounts | Y1: 95K; Y3: 680K |
| Monthly Active Requesters (MAR) | Unique customers requesting/month | Y1 M12: 18K |
| Repeat Rate (90-day) | Customers with 2+ jobs in 90 days | ≥12% Y1; ≥22% Y3 |
| Customer CAC | Blended acquisition cost | ≤$18 Y1 |
| Customer LTV (24-mo) | Projected net contribution | ≥$45 |
| App Store Rating | Weighted iOS/Android | ≥4.5 |
| CSAT (post-job) | 1–5 survey | ≥4.4 |

---

## Marketplace Health Metrics

| Metric | Definition | Target |
|--------|------------|--------|
| Time to First Offer (TTFO) | Request created → first provider offer | Median ≤3 min |
| Time to Accept (TTA) | Request → customer acceptance | Median ≤8 min |
| Time to Arrive (TTAar) | Acceptance → provider on-site | Per category SLA |
| Cancellation Rate (customer) | Pre-arrival customer cancels | ≤12% |
| Cancellation Rate (provider) | Provider cancels post-accept | ≤5% |
| Fill Rate | Completed / accepted offers | ≥92% |
| Zone Coverage Score | % land area with 3+ providers within 15 km | Launch zones: 90% |

---

## Financial Success Metrics

| Metric | Definition | Target |
|--------|------------|--------|
| Take Rate (net) | Net revenue / GMV | 16–20% |
| Contribution Margin | (Net revenue − variable costs) / net revenue | 45% Y2; 55% Y3 |
| CAC Payback | Months to recover customer CAC | ≤8 months |
| LTV:CAC Ratio | 24-month LTV / CAC | ≥3:1 |
| EBITDA Margin | EBITDA / net revenue | Break-even Y3 |
| Cash Runway | Months at current burn | Maintain ≥12 post-Series A |

See [Unit Economics](../08-Finance/Unit-Economics.md), [CAC-LTV](../08-Finance/CAC-LTV.md).

---

## Quality & Trust Metrics

| Metric | Definition | Target |
|--------|------------|--------|
| Customer NPS | Promoters − detractors | ≥40 Y2 |
| Average Provider Rating | Post-job stars | ≥4.6 |
| Dispute Rate | Disputes / completed jobs | ≤4% |
| Dispute Resolution Time | Median hours to resolve | ≤48h |
| SLA Breach Rate | Jobs missing arrival SLA | ≤8% |
| Safety Incident Rate | Verified safety complaints / 10K jobs | ≤2 |
| Refund Rate | Refunded GMV / total GMV | ≤2.5% |

---

## B2B Success Metrics

| Metric | Definition | Target |
|--------|------------|--------|
| B2B Job Share | B2B jobs / total SCAJ | 20% Y2; 35% Y3 |
| B2B Contract Count | Active enterprise agreements | 1 Y1; 8 Y3 |
| B2B SLA Adherence | Partner-specific arrival/resolution | ≥95% |
| B2B Revenue Share | B2B fees / net revenue | 25% Y3 |
| Partner Churn | Lost B2B contracts / year | ≤10% |

---

## Reporting Cadence

| Report | Metrics | Audience | Frequency |
|--------|---------|----------|-----------|
| Daily Pulse | SCAJ, TTFO, cancellations, active jobs | Ops leadership | Daily |
| Weekly Growth | MAR, provider activation, liquidity | Exec team | Weekly |
| Monthly Board Pack | L1–L2 full suite + financials | Board | Monthly |
| Quarterly Business Review | Strategic KPIs vs objectives | All-hands | Quarterly |
| Provider Scorecards | Individual provider performance | Provider ops | Monthly |

---

## Business Examples

**Liquidity Index calculation:** In Dubai Marina zone, 100 requests in a week; 68 received 3+ offers within 5 minutes → Liquidity Index = 68%. Below 65% target triggers supply recruitment.

**SCAJ exclusion:** Customer accepts offer but provider never arrives; job auto-cancelled after 2 hours with full refund → does **not** count as SCAJ but counts toward cancellation and SLA breach metrics.

**LTV:CAC:** Customer acquired via referral ($8 CAC) completes 2 tow jobs ($70 net revenue to platform over 24 months) → healthy unit; paid social user at $25 CAC with 1 small job → flagged for channel review.

---

## Business Decisions

| Decision | Rationale |
|----------|-----------|
| SCAJ as North Star vs GMV | GMV inflates with price; SCAJ measures real marketplace output |
| Liquidity Index as co-primary metric | Without offers, nothing else matters in marketplace |
| Separate B2B metric suite | Partner SLAs and sales cycles differ materially from B2C |
| Public refund/dispute targets | Accountability metric visible to support and legal teams |

---

## Risks

| Risk | Metric Impact |
|------|---------------|
| Gaming (fake completions) | Inflated SCAJ; mitigated by payment + GPS audit sampling |
| Over-indexing on speed | SLA breaches hidden if providers rush unsafely |
| Vanity registration counts | MAR and SCAJ preferred over total sign-ups |
| Zone averaging masking deserts | Require zone-level liquidity reporting |

---

## Assumptions

- Metric definitions remain stable for 12 months post-launch for comparability
- Baseline benchmarks derived from mobility marketplace comparables (ride-hailing, food delivery)
- All metrics have single definitional owner in Finance + Product Ops

---

## Open Questions

- Include "prevented secondary incidents" as qualitative safety metric?
- Real-time public transparency dashboard for investors?
- Weight NPS vs CSAT as primary voice-of-customer metric?

---

## Next Steps

1. Publish metric dictionary to all department heads
2. Align [KPIs](../05-Product-Strategy/KPIs.md) dashboard spec with this document
3. Set up weekly exec review template using L1/L2 metrics
4. Define zone-level reporting geography with operations
