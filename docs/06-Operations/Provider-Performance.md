# Provider Performance — Salik Assist

| Field | Value |
|-------|-------|
| **Version** | 1.0 |
| **Status** | Draft |
| **Author** | Product & Strategy Team |
| **Last Updated** | July 4, 2026 |

## Purpose

Define how Salik Assist measures, scores, rewards, and manages provider performance to maintain marketplace quality, customer trust, and fair competition among independent service providers.

## Scope

Covers performance metrics, scoring methodology, tier benefits, improvement programs, and corrective actions. Excludes technical analytics implementation.

## Related Documents

- [Provider Onboarding](./Provider-Onboarding.md)
- [Provider Verification](./Provider-Verification.md)
- [SLA](./SLA.md)
- [Quality Control](./Quality-Control.md)
- [Escalation Policy](./Escalation-Policy.md)
- [Provider Agreement](../07-Legal/Provider-Agreement.md)

## Table of Contents

1. [Performance Philosophy](#performance-philosophy)
2. [Core Performance Metrics](#core-performance-metrics)
3. [Salik Performance Score (SPS)](#salik-performance-score-sps)
4. [Performance Tiers](#performance-tiers)
5. [Matching Algorithm Weighting](#matching-algorithm-weighting)
6. [Rewards & Incentives](#rewards--incentives)
7. [Performance Improvement Program](#performance-improvement-program)
8. [Corrective Actions & Consequences](#corrective-actions--consequences)
9. [Reporting & Review Cadence](#reporting--review-cadence)
10. [Business Examples](#business-examples)
11. [Business Decisions](#business-decisions)
12. [Risks](#risks)
13. [Assumptions](#assumptions)
14. [Open Questions](#open-questions)
15. [Next Steps](#next-steps)

---

## Performance Philosophy

Salik Assist performance management balances three objectives:

1. **Customer safety and satisfaction** — Non-negotiable floor metrics
2. **Provider fairness** — Score reflects recent behavior, not permanent labels; improvement paths exist
3. **Marketplace health** — Performance drives matching priority, creating meritocratic competition

**Principle:** Performance data is shared transparently with providers via weekly dashboard. Customers see rating and verification; internal SPS is not displayed to customers.

---

## Core Performance Metrics

| Metric | Definition | Target | Weight in SPS |
|--------|------------|--------|---------------|
| **Customer Rating** | Average stars (1–5) over rolling 30 jobs | ≥4.5 | 30% |
| **Acceptance Rate** | Offers accepted ÷ offers received | ≥70% | 15% |
| **Response Time** | Median seconds to respond to offer invitation | ≤60 sec | 10% |
| **ETA Accuracy** | % of jobs where arrival within committed ETA ±15 min | ≥85% | 20% |
| **Completion Rate** | Jobs completed ÷ jobs accepted | ≥95% | 15% |
| **Cancellation Rate (provider-initiated)** | Provider cancellations ÷ jobs accepted | ≤5% | 10% |

**Hard floor metrics (automatic review if breached):**

| Metric | Floor | Consequence |
|--------|-------|-------------|
| Customer Rating | <3.5 (30 jobs) | Performance review; possible suspension |
| No-show rate | >3% (90 days) | Immediate suspension |
| Safety incident | Any confirmed | Immediate suspension pending investigation |
| Fraud / overcharge | Any confirmed | Permanent removal |

---

## Salik Performance Score (SPS)

SPS is a composite score from 0–100 calculated weekly for each active provider.

**Formula:** Weighted average of normalized metric scores (each metric scored 0–100 against target, capped at 100).

| SPS Range | Label | Matching Impact |
|-----------|-------|-----------------|
| 90–100 | Elite | +20% matching priority boost |
| 75–89 | Strong | Standard matching priority |
| 60–74 | Developing | −10% matching priority |
| 40–59 | At Risk | −30% matching priority; improvement plan required |
| <40 | Critical | Suspension review; limited to 5 offers/week max |

**Minimum sample:** SPS calculated only after 10 completed jobs. New providers receive neutral SPS of 75 ("Developing") for first 10 jobs.

**Recalculation:** Every Monday 6 AM GST based on rolling 90-day window (minimum 10 jobs).

---

## Performance Tiers

| Tier | SPS Requirement | Additional Criteria | Benefits |
|------|-----------------|---------------------|----------|
| **Standard** | Default | Tier 1 verified | Base commission rate (18%) |
| **Preferred** | SPS ≥75 for 8 consecutive weeks | Rating ≥4.3 | 1% commission discount; T+1 payout |
| **Elite** | SPS ≥90 for 12 consecutive weeks | Rating ≥4.7; completion ≥97% | 2% commission discount; priority matching; featured badge |
| **Partner Elite** | SPS ≥85 + B2B contract | Insurance/fleet SLA compliance | B2B job priority; dedicated account manager |

Tier demotion: 2 consecutive weeks below tier threshold triggers demotion. Grace period of 1 week for Preferred tier.

---

## Matching Algorithm Weighting

Provider SPS influences matching alongside distance and availability:

| Factor | Weight in Matching |
|--------|-------------------|
| Distance to customer | 35% |
| Salik Performance Score | 25% |
| Customer rating | 20% |
| Response time (historical) | 10% |
| Availability / idle time | 10% |

**Geographic override:** In zones with <5 eligible providers within radius, distance weight increases to 50%; SPS weight reduces to 15% to ensure coverage.

**New provider boost:** First 30 days — neutral SPS 75 plus +5% matching boost in underserved zones.

---

## Rewards & Incentives

| Reward | Trigger | Value |
|--------|---------|-------|
| Weekly top performer | Highest SPS in zone (min. 5 jobs/week) | AED 500 bonus |
| Monthly excellence | SPS ≥90 for full month | AED 2,000 bonus |
| Streak bonus | 20 consecutive jobs rated 5 stars | AED 300 bonus |
| Referral bonus | Verified provider referred and completes 10 jobs | AED 500 |
| Tier commission discount | Preferred (−1%) / Elite (−2%) | Ongoing |
| Surge share bonus | Complete job during surge window | +10% of surge premium |

Bonuses paid via provider payout cycle (T+2 or T+1 per tier).

---

## Performance Improvement Program

Providers with SPS 40–59 ("At Risk") enter mandatory improvement program:

| Week | Action |
|------|--------|
| 1 | Automated email with metric breakdown and specific gaps |
| 1 | Assigned ops coach for 30-min call |
| 2 | Retraining module on weakest metric (e.g., ETA communication) |
| 3 | Monitored jobs: ops reviews next 5 jobs in real time |
| 4 | Reassessment: SPS ≥60 to exit program; <40 triggers suspension review |

**Voluntary improvement:** Any provider may request coaching regardless of SPS.

---

## Corrective Actions & Consequences

| Violation | First Occurrence | Second (90 days) | Third (90 days) |
|-----------|------------------|------------------|-----------------|
| ETA miss >30 min without notification | Warning + coaching | SPS −10 penalty | Suspension 7 days |
| Provider-initiated cancellation (non-emergency) | Warning | SPS −5 penalty | Offer limit 10/week |
| Customer rating 1 star (unresolved) | Investigation within 24 hr | Performance review | Suspension |
| Price overcharge >20% without consent | Full refund + warning | Suspension 14 days | Permanent removal |
| No-show | Suspension 7 days | Suspension 30 days | Permanent removal |
| Rude / unsafe behavior (confirmed) | Suspension 14 days | Permanent removal | — |

All corrective actions documented; provider notified via app and email with appeal option per [Escalation Policy](./Escalation-Policy.md).

---

## Reporting & Review Cadence

| Report | Audience | Frequency |
|--------|----------|-----------|
| Provider performance dashboard | Provider (self-serve) | Real-time metrics; weekly SPS |
| Zone performance summary | Ops team | Daily |
| At-risk provider list | Ops + Quality | Weekly |
| Tier promotion/demotion | Provider + Finance | Weekly |
| Marketplace health report | Leadership | Monthly |
| Quarterly business review | Elite/Partner providers | Quarterly |

---

## Business Examples

**Example 1 — Elite provider:** Tow operator maintains 4.8 rating, 92% acceptance, 88% ETA accuracy over 12 weeks. SPS reaches 94. Promoted to Elite tier: 2% commission discount, featured in JLT zone, wins monthly excellence bonus AED 2,000.

**Example 2 — At-risk recovery:** Battery provider's rating drops to 3.8 after 3 rushed jobs with poor communication. SPS falls to 52. Enters improvement program. Retraining on customer communication. After 4 weeks, rating recovers to 4.2; SPS 68; exits program.

**Example 3 — No-show suspension:** Provider accepts job, does not arrive, does not respond to calls. Customer waits 45 minutes. Ops dispatches backup provider. First no-show: 7-day suspension. Provider appeals citing vehicle breakdown; evidence accepted; suspension reduced to 3 days with mandatory backup vehicle policy acknowledgment.

---

## Business Decisions

| Decision | Rationale |
|----------|-----------|
| Rolling 90-day SPS window | Rewards recent behavior; allows recovery from bad streaks |
| SPS hidden from customers | Avoids gaming; customers see ratings which are intuitive |
| Hard floor on no-show (3%) | No-shows are highest-severity customer experience failure |
| New provider neutral score of 75 | Prevents cold-start penalty while maintaining quality monitoring |
| Improvement program before suspension (40–59 band) | Provider-friendly; many issues are training-fixable |
| Geographic override in low-density zones | Performance scoring must not sacrifice coverage |

---

## Risks

| Risk | Impact | Mitigation |
|------|--------|------------|
| Providers game metrics (e.g., selective acceptance) | Medium | Monitor acceptance patterns; minimum offer volume requirements |
| Over-penalization causes provider churn | Medium | Improvement program; transparent scoring; appeal process |
| Elite providers dominate matching in dense zones | Medium | Cap elite boost; rotate featured placement |
| Insufficient job volume for fair SPS | Low | Minimum 10 jobs; neutral score for new providers |
| Customer rating bias (harsh/lenient raters) | Low | Weight recent ratings; investigate 1-star patterns |

---

## Assumptions

- Providers will actively check performance dashboard if bonuses are tied to SPS
- 80% of at-risk providers improve after coaching program
- Weekly recalculation is sufficient; daily not needed at launch scale
- Matching weight of 25% for SPS is noticeable but not dominant vs. distance
- Commission discounts (1–2%) are sufficient Elite incentive without excessive margin erosion

---

## Open Questions

- Display simplified "performance badge" to customers (e.g., "Top Rated") for Elite providers?
- Category-specific SPS weights (tow ETA vs. battery response time)?
- Team/driver-level scoring for multi-vehicle operators?
- Public leaderboard by zone — motivational or encourages unhealthy competition?

---

## Next Steps

1. Build provider performance dashboard mockup for launch
2. Define ops coaching playbook for improvement program
3. Configure weekly SPS calculation and tier promotion rules
4. Communicate performance framework to pre-launch provider pipeline
5. Pilot SPS weighting in matching with ops override capability
