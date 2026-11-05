# Pricing Strategy — Salik Assist

| Field | Value |
|-------|-------|
| **Version** | 1.0 |
| **Status** | Draft |
| **Author** | Product & Strategy Team |
| **Last Updated** | July 4, 2026 |

## Purpose

Define Salik Assist's pricing strategy for customers, providers, and B2B partners—balancing marketplace liquidity, trust, competitive positioning, and unit economics in the GCC roadside assistance market.

## Scope

Pricing philosophy, rate structures, guardrails, promotions, and surge policy. Excludes payment processing implementation and billing system design.

## Related Documents

- [Revenue Model](./Revenue-Model.md)
- [Business Rules](./Business-Rules.md)
- [Competitive Matrix](../03-Competitors/Competitive-Matrix.md)
- [Unit Economics](../08-Finance/Unit-Economics.md)
- [Value Proposition](./Value-Proposition.md)

## Table of Contents

1. [Pricing Philosophy](#pricing-philosophy)
2. [Customer Pricing Model](#customer-pricing-model)
3. [Service Category Rate Guardrails](#service-category-rate-guardrails)
4. [Provider Pricing Freedom & Constraints](#provider-pricing-freedom--constraints)
5. [Surge Pricing Strategy](#surge-pricing-strategy)
6. [B2B Partner Pricing](#b2b-partner-pricing)
7. [Promotional & Launch Pricing](#promotional--launch-pricing)
8. [Competitive Pricing Position](#competitive-pricing-position)
9. [Pricing Governance](#pricing-governance)
10. [Business Examples](#business-examples)
11. [Business Decisions](#business-decisions)
12. [Risks](#risks)
13. [Assumptions](#assumptions)
14. [Open Questions](#open-questions)
15. [Next Steps](#next-steps)

---

## Pricing Philosophy

Salik Assist pricing follows four principles:

| Principle | Application |
|-----------|-------------|
| **Transparency before commitment** | Customer sees price range before accepting offer |
| **Provider autonomy within guardrails** | Providers set competitive rates; platform prevents predatory low and exploitative high |
| **Emergency fairness** | Surge capped; no hidden fees; final price within disclosed band |
| **Value-aligned platform fee** | Commission earned only on completed jobs |

**We do not compete on being the cheapest.** We compete on trust, choice, and certainty.

---

## Customer Pricing Model

Customers pay the **provider's declared rate** for service rendered, plus any disclosed surge increment. Salik Assist does not add a separate customer service fee at launch.

| Element | Customer Experience |
|---------|---------------------|
| Price estimate | Range shown on each offer (e.g., AED 180–220) |
| Final price | Within estimate band ± 15% (Rule 30) |
| Payment timing | Upon service completion |
| Payment methods | Card, Apple Pay, Samsung Pay, approved wallets |
| Receipt | Digital receipt with itemized service |
| Promotional discounts | Applied at checkout; funded per promotion rules |

**Average expected customer spend (UAE metro):**

| Scenario | Expected Range (AED) |
|----------|---------------------|
| Battery jump-start | 80–150 |
| Flat tire | 100–180 |
| Emergency fuel (5L) | 60–100 |
| Local tow | 180–350 |
| Mobile mechanic (minor) | 150–280 |

---

## Service Category Rate Guardrails

Providers must set rates within platform minimums and maximums per category and zone:

| Category | Min (AED) | Max (AED) | Notes |
|----------|-----------|-----------|-------|
| Battery jump-start | 60 | 200 | Includes basic cables; battery sale separate |
| Battery replacement | 150 | 450 | Excludes battery part cost (provider itemizes) |
| Flat tire change | 80 | 250 | Customer must have spare |
| Emergency fuel (per 5L) | 50 | 120 | Fuel cost at market rate |
| Local tow (0–20 km) | 150 | 450 | Standard sedan |
| Medium tow (SUV/truck) | 200 | 550 | Vehicle class modifier |
| Long-distance tow (20–80 km) | 350 | 900 | Per-km adder allowed above base |
| Mobile mechanic (call-out) | 100 | 200 | Diagnostic; parts additional |
| Desert/off-road recovery | 500 | 2,500 | Specialist providers only |

Guardrails reviewed quarterly based on market data and provider feedback.

---

## Provider Pricing Freedom & Constraints

| Freedom | Constraint |
|---------|------------|
| Set base rate within guardrails | Cannot undercut minimum (prevents unsustainable race to bottom) |
| Offer competitive estimates in top-3 | Cannot exceed maximum without specialist designation |
| Adjust rates anytime | Changes apply to new offers only; not retroactive |
| Decline jobs | No penalty for declining; penalty for accept-then-cancel |
| Participate in surge | Must accept surge terms when available toggle is on |

| Provider Cost | Amount |
|---------------|--------|
| Standard commission | 18% of job value |
| Launch promo | 0% (first 30 days, launch zone) |
| Professional subscription | AED 299/month (optional) |
| Premium subscription | AED 499/month (optional) |

---

## Surge Pricing Strategy

| Parameter | Value |
|-----------|-------|
| Activation trigger | Demand/supply ratio > 1.5 in zone for 15+ minutes |
| Maximum multiplier | 1.5× base rate |
| Customer disclosure | Surge badge on offer before acceptance |
| Provider share of surge increment | 70% |
| Platform share of surge increment | 30% |
| Categories eligible | All except B2B contract jobs (unless contract allows) |

**Peak periods (UAE):**
- June–August, 10 AM–6 PM (battery/tire)
- Friday–Sunday highway egress (tow)
- First rain after dry season (accidents)

Surge is a **supply incentive tool**, not a primary revenue strategy.

---

## B2B Partner Pricing

| Component | Insurer / B2B2C | Fleet / B2B |
|-----------|-----------------|-------------|
| Platform fee | AED 8,000–15,000/month | AED 10,000–25,000/month |
| Per-dispatch fee | AED 8–12 | AED 10–15 |
| Commission on job value | 12–14% | 12–15% |
| Pre-negotiated rate cards | Yes (by zone, category) | Yes (volume tiers) |
| SLA penalty clauses | Optional credit for missed SLA | Standard in enterprise contracts |

B2B customers receive **rate certainty** in exchange for volume commitment. End customer (policyholder) may pay zero out-of-pocket for covered events.

---

## Promotional & Launch Pricing

| Promotion | Audience | Terms | Duration |
|-----------|----------|-------|----------|
| Zero commission | Providers (launch zone) | 0% platform fee | First 30 days |
| First rescue free (up to AED 100) | New customers | Platform-funded credit | Launch month |
| Refer-a-friend | Customers | AED 30 credit both parties | Ongoing Year 1 |
| Provider referral bonus | Providers | AED 200 per verified referral | Ongoing Year 1 |
| Insurer co-marketing | B2B2C | Custom; co-funded | Per partnership |

Promotional budget: 8% of Year 1 gross revenue (marketing allocation).

---

## Competitive Pricing Position

| Alternative | Typical Customer Cost | Salik Assist Position |
|-------------|----------------------|----------------------|
| Informal tow (cash) | AED 150–300 (negotiated) | Comparable mid-range with transparency |
| Insurer hotline | "Free" to policyholder | Salik B2B2C replicates; B2C competitive |
| Single-brand app | Fixed rate, no comparison | Salik enables 10–20% savings via choice |
| Category app | AED 80–150 (battery) | Parity with multi-category convenience premium |

**Positioning:** Mid-market pricing with premium trust and transparency—not budget, not luxury.

---

## Pricing Governance

| Decision Type | Authority | Review |
|---------------|-----------|--------|
| Guardrail changes | Head of Operations + Finance | Quarterly |
| Surge activation thresholds | Operations (automated) + weekly review | Weekly in peak season |
| B2B contract pricing | Head of Partnerships + CEO | Per deal |
| Promotional campaigns | Head of Marketing + Finance | Monthly |
| Commission rate changes | CEO + Board | Annual; 60-day provider notice |

All pricing changes documented with effective date and communicated to providers 14 days in advance (except automated surge).

---

## Business Examples

**Example 1 — Competitive offer savings:** Customer receives three tow offers: AED 220–260, AED 190–230, AED 250–300. Selects middle offer. Final tow AED 210—within band. Customer saved ~AED 40 vs. highest offer.

**Example 2 — Surge transparency:** July 2 PM battery request in Deira. Surge 1.3× active. Offers show "Peak demand" badge with AED 104–130 range vs. normal AED 80–100. Customer accepts with full knowledge.

**Example 3 — B2B zero out-of-pocket:** Insurer policyholder with roadside coverage requests tow. Pre-negotiated rate AED 250. Customer pays AED 0; insurer billed AED 250 + AED 10 dispatch fee + 13% commission. Policyholder NPS improves.

---

## Business Decisions

| Decision | Rationale |
|----------|-----------|
| No separate customer service fee at launch | Reduce adoption friction; commission from provider side |
| Guardrails vs. fixed prices | Preserves provider autonomy; enables competition |
| Surge cap at 1.5× | Emergency context requires customer protection |
| B2B lower commission for volume | Demand acquisition through partnerships |
| Launch zero-commission for providers | Supply-side seeding in launch zone |

---

## Risks

| Risk | Impact | Mitigation |
|------|--------|------------|
| Providers price at maximum guardrail always | Medium | Competitive top-3 model pressure |
| Customer sticker shock on long-distance tow | Medium | Clear estimate bands; approval for overruns |
| Surge during genuine emergencies backlash | High | Cap; badge; PR messaging on supply incentive |
| B2B rate cards outdated vs. market | Medium | Quarterly rate card review with partners |
| Promotional cost exceeds budget | Medium | CAC caps; referral limits |

---

## Assumptions

- UAE customers accept mid-range pricing when transparency is delivered
- Providers prefer guardrails to completely free pricing (prevents race to bottom)
- 1.5× surge sufficient to mobilize supply without customer outrage
- B2B partners value rate certainty over lowest possible per-job cost
- Average job value grows 5% annually with inflation and category mix

---

## Open Questions

- Category-specific commission vs. uniform 18%?
- Dynamic guardrails based on real-time market data?
- Should customers see provider payout (transparency vs. conflict)?
- Flat customer membership (e.g., AED 49/year for discounted rates)?
- KSA pricing guardrails differ due to market rates?

---

## Next Steps

1. Validate guardrails with 15 provider pricing interviews
2. Model surge impact on Year 1 revenue (base case vs. peak)
3. Finalize B2B rate card template for partnerships team
4. Approve launch promotional budget with Finance
5. Publish customer-facing pricing FAQ for app and website
