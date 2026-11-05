# North Star Metric — Salik Assist

| Field | Value |
|-------|-------|
| **Version** | 1.0 |
| **Status** | Draft |
| **Author** | Product & Strategy Team |
| **Last Updated** | July 4, 2026 |

## Purpose

Define the single North Star Metric (NSM) that aligns Salik Assist teams—product, operations, growth, partnerships, and finance—on what ultimate success looks like. This document specifies definition, counting rules, exclusions, drivers, and governance.

## Scope

North Star definition, formula, counting criteria, input metrics, targets, and reporting. Excludes instrumentation implementation, data pipeline design, and dashboard engineering.

## Related Documents

- [Success Metrics](../01-Executive/Success-Metrics.md)
- [Objectives](../01-Executive/Objectives.md)
- [KPIs](./KPIs.md)
- [OKRs](./OKRs.md)
- [Product Strategy](./Product-Strategy.md)
- [Product Principles](./Product-Principles.md)
- [Unit Economics](../08-Finance/Unit-Economics.md)
- [SLA](../06-Operations/SLA.md)

## Table of Contents

1. [North Star Metric Statement](#north-star-metric-statement)
2. [Why This Metric](#why-this-metric)
3. [Formal Definition](#formal-definition)
4. [Counting Rules](#counting-rules)
5. [Exclusions](#exclusions)
6. [Input Metrics (Drivers)](#input-metrics-drivers)
7. [Guardrail Metrics](#guardrail-metrics)
8. [Targets and Milestones](#targets-and-milestones)
9. [Segmentation and Reporting](#segmentation-and-reporting)
10. [Governance](#governance)
11. [Business Examples](#business-examples)
12. [Business Decisions](#business-decisions)
13. [Risks](#risks)
14. [Assumptions](#assumptions)
15. [Open Questions](#open-questions)
16. [Next Steps](#next-steps)

---

## North Star Metric Statement

**Successfully Completed Assisted Jobs (SCAJ)**

Every team at Salik Assist optimizes for jobs where a motorist received real roadside help—matched through the platform, fulfilled by a verified provider, and settled with payment captured or B2B invoice recorded.

---

## Why This Metric

| Alternative Metric | Why Not North Star |
|--------------------|-------------------|
| App downloads | No value until jobs complete |
| Service requests created | Requests without fulfillment waste customer trust |
| GMV (Gross Merchandise Value) | Inflates with price; doesn't measure fulfillment |
| Provider sign-ups | Supply without demand is idle |
| Offers sent | Providers responding ≠ customer rescued |
| Customer NPS | Lagging indicator; doesn't capture volume |

**SCAJ** uniquely captures **demand fulfilled**, **supply paid**, and **platform value delivered** in one countable event—aligned with commission revenue and the top-3 marketplace promise.

---

## Formal Definition

A **Successfully Completed Assisted Job** is recorded when **all** of the following conditions are met:

| # | Condition | Description |
|---|-----------|-------------|
| 1 | **Valid request** | Customer submitted a legitimate service request with location, vehicle type, and issue category |
| 2 | **Offer accepted** | Customer explicitly accepted one provider's offer from the marketplace (top-3 or fewer if supply-limited) |
| 3 | **Service completed** | Provider marked job complete; customer confirmed or auto-confirm window elapsed without dispute |
| 4 | **Payment settled** | Customer payment captured, or B2B partner invoice line item generated per contract |
| 5 | **No fraud flag** | Job passed anti-fraud checks; not under active investigation for collusion or synthetic activity |

**Formula:**

```
SCAJ = COUNT(jobs meeting conditions 1–5 in period T)
```

**Period reporting:** Daily, weekly, monthly, and cumulative since launch.

---

## Counting Rules

### Job Identity

- One SCAJ per accepted offer that reaches completion
- Multi-stop tows (e.g., highway → garage) count as **one SCAJ** if single accepted offer
- Customer requests second service same day = **two SCAJs** if two separate acceptances

### Timing

- SCAJ attributed to **completion date** (not request date) for revenue alignment
- B2B jobs attributed on partner invoice acknowledgment date if payment timing differs

### Partial Completion

- Provider arrives but cannot fix (e.g., needs garage tow instead of battery jump) → counts as SCAJ if customer accepts revised scope and payment reflects actual service
- Customer refuses revised price after diagnosis → does **not** count; may count as cancellation

### Top-3 Model Alignment

- SCAJ only increments after customer **chooses** among competitive offers (or accepts sole available offer with explicit acknowledgment when <3 providers respond)
- Auto-assigned jobs (B2B exception contracts only) count if all other conditions met—reported separately

---

## Exclusions

| Scenario | Counts as SCAJ? | Counts Toward |
|----------|-----------------|---------------|
| Customer cancels before provider arrival | No | Cancellation rate |
| Provider no-show; full refund | No | SLA breach, dispute |
| Payment fails after service | No | Payment failure rate |
| Fraudulent collusion (customer + provider) | No | Fraud loss |
| Test/sandbox jobs | No | Internal QA only |
| Provider arrives; customer absent | No | Provider cancellation |
| Job in active dispute (unresolved) | No (pending) | Dispute queue |
| Duplicate request merged | No | Ops efficiency |

---

## Input Metrics (Drivers)

SCAJ is an output metric driven by marketplace inputs. Teams own levers on these drivers:

### Demand Drivers

| Input Metric | Owner | Relationship to SCAJ |
|--------------|-------|----------------------|
| Monthly Active Requesters (MAR) | Growth | More requesters → more potential SCAJ |
| Request-to-Accept Rate | Product | Higher conversion after offers shown |
| Customer Repeat Rate | Product + Growth | Returning users compound SCAJ |

### Supply Drivers

| Input Metric | Owner | Relationship to SCAJ |
|--------------|-------|----------------------|
| Active Providers (30-day) | Operations | More supply → more completions |
| Offer Response Rate | Operations | Faster offers → higher acceptance |
| Fill Rate (accepted → completed) | Operations + Product | Reduces drop-off post-acceptance |

### Marketplace Drivers

| Input Metric | Owner | Relationship to SCAJ |
|--------------|-------|----------------------|
| Liquidity Index (% requests with ≥3 offers in 5 min) | Operations | Enables top-3 promise |
| Time to First Offer (median) | Product + Ops | Speed drives acceptance |
| Zone Coverage Score | Operations | Geographic completeness |

### B2B Drivers

| Input Metric | Owner | Relationship to SCAJ |
|--------------|-------|----------------------|
| B2B Job Volume | Partnerships | Predictable SCAJ increment |
| B2B SLA Adherence | Operations | Partner retention → sustained volume |

---

## Guardrail Metrics

Optimizing SCAJ alone can cause harm. Monitor these guardrails alongside the North Star:

| Guardrail | Threshold | Why |
|-----------|-----------|-----|
| Customer NPS | ≥35 (Y1); ≥40 (Y2) | Volume without satisfaction churns users |
| Provider Cancellation Rate | ≤5% | Supply reliability |
| Dispute Rate | ≤4% of completions | Quality of counted jobs |
| SLA Breach Rate | ≤8% | Safety and trust |
| Refund Rate | ≤2.5% of GMV | False completions |
| Fraud Rate | ≤0.5% of SCAJ | Metric integrity |
| Contribution Margin per Job | Positive by M9 | Growth must be sustainable |

---

## Targets and Milestones

### Dubai Launch Year (Year 1)

| Milestone | Target SCAJ | Cumulative |
|-----------|-------------|------------|
| Launch Month (M1) | 2,500 | 2,500 |
| M3 | 5,500 / month | 12,000 |
| M6 | 7,500 / month | 32,000 |
| M12 | 10,500 / month | 85,000 |

### Long-Range

| Year | Annual SCAJ | Notes |
|------|-------------|-------|
| Year 1 | 85,000 | Dubai + early corridor expansion |
| Year 2 | 320,000 | UAE-wide + B2B scale |
| Year 3 | 780,000 | KSA entry + category maturity |

### Launch Readiness Gate

Pre-launch soft launch must achieve **500 SCAJ** in 30-day beta with:
- Fill rate ≥88%
- Dispute rate ≤6% (relaxed beta threshold)
- Liquidity Index ≥55% in beta zones

---

## Segmentation and Reporting

Report SCAJ sliced by dimensions that inform decisions:

| Dimension | Use |
|-----------|-----|
| **Geography** | Zone, emirate, highway corridor |
| **Category** | Tow, battery, tire, fuel, mechanic |
| **Channel** | Organic, paid, referral, B2B partner |
| **Customer type** | New vs. repeat |
| **Provider tier** | Standard vs. premium (future) |
| **Offer count** | 3 offers vs. 2 vs. 1 (supply stress indicator) |
| **Language** | Arabic vs. English session |

**Weekly North Star Review** agenda:
1. SCAJ vs. plan (WoW)
2. Top 3 driver deltas (MAR, liquidity, fill rate)
3. Guardrail breaches
4. Zone-level underperformers

---

## Governance

| Role | Responsibility |
|------|----------------|
| **CEO / GM** | North Star accountability; resolves cross-team trade-offs |
| **Head of Product** | Definition owner; change control |
| **Finance** | Reconciliation of SCAJ to GMV and revenue |
| **Operations** | Fill rate, SLA, supply drivers |
| **Growth** | MAR and channel-attributed SCAJ |
| **Partnerships** | B2B-attributed SCAJ |

**Definition changes** require Product + Finance approval; maximum one revision per 12 months post-launch except fraud/exclusion clarifications.

---

## Business Examples

**Example 1 — Standard SCAJ:** Customer in JLT requests battery jump. Three offers arrive in 3 minutes. Customer accepts AED 160 offer. Provider arrives in 18 minutes, completes jump, payment captured via card. **SCAJ = 1.**

**Example 2 — Excluded no-show:** Customer accepts tow offer. Provider cancels 40 minutes later; customer receives refund. Job never completed. **SCAJ = 0.** Counted in provider cancellation and SLA breach metrics.

**Example 3 — B2B SCAJ:** Insurer policyholder taps roadside help in partner app. Two in-network providers offer; customer selects one. Service completes; insurer invoiced AED 220 per contract. **SCAJ = 1** (B2B segment).

**Example 4 — Supply-limited honesty:** Remote highway request receives only 1 offer in 8 minutes. Customer accepts with "Only 1 provider available" acknowledgment. Job completes. **SCAJ = 1** (tagged `offer_count=1` for liquidity reporting).

---

## Business Decisions

| Decision | Rationale |
|----------|-----------|
| SCAJ over GMV as North Star | Measures real marketplace output, not price inflation |
| Completion-date attribution | Aligns with revenue recognition and provider payout |
| Separate reporting for <3 offer jobs | Transparency on top-3 model delivery |
| Fraud exclusion non-negotiable | Protects metric integrity and investor trust |
| Guardrails alongside NSM | Prevents toxic growth (bad jobs counted) |
| Beta gate of 500 SCAJ before public launch | Prove fulfillment before scaling marketing |

---

## Risks

| Risk | Impact | Mitigation |
|------|--------|------------|
| **Gaming** — fake completions | Inflated NSM | GPS audit sampling; payment verification |
| **Premature completion** — provider marks done early | Customer harm; disputes | Customer confirm step; dispute window |
| **SCAJ obsession ignores margin** | Unprofitable growth | Contribution margin guardrail |
| **Zone averaging** — weak areas hidden | Dubai launch failure masked | Zone-level dashboards mandatory |
| **B2B bulk without quality** | Partner churn | B2B SLA guardrails |

---

## Assumptions

- SCAJ correlates with net revenue (commission on completed GMV) within 95% confidence
- Completion confirmation within 24 hours is sufficient for customer dispute initiation
- Dubai launch can achieve 2,500 SCAJ in M1 with controlled beta + soft launch
- Top-3 model improves accept-to-complete rate vs. auto-assign baseline by ≥10%

---

## Open Questions

- Auto-confirm completion after 24h if customer silent—ethical and metric implications?
- Include partial refunds (goodwill) jobs as SCAJ with reduced GMV?
- Public SCAJ counter for marketing ("10,000 rescues and counting")—competitive sensitivity?
- Weight SCAJ by job value for internal prioritization, while headline remains count?

---

## Next Steps

1. Socialize SCAJ definition with all department heads and board
2. Align [KPIs](./KPIs.md) and [OKRs](./OKRs.md) to NSM drivers
3. Define zone-level SCAJ targets for Dubai launch corridors
4. Establish weekly North Star review calendar starting pre-launch beta
5. Document reconciliation process between SCAJ and finance revenue reports
