# Business Terminology — Salik Assist

| Field | Value |
|-------|-------|
| **Version** | 1.0 |
| **Status** | Draft |
| **Author** | Product & Strategy Team |
| **Last Updated** | July 4, 2026 |

## Purpose

Define key business concepts, frameworks, and terminology used in Salik Assist strategy and operations—beyond single-term definitions in the [Glossary](./Glossary.md).

## Scope

Business models, strategic frameworks, operational concepts, and marketplace dynamics relevant to Salik Assist. Excludes technical and engineering terminology.

## Related Documents

- [Glossary](./Glossary.md)
- [Business Model Canvas](../04-Business/Business-Model-Canvas.md)
- [Executive Summary](../01-Executive/Executive-Summary.md)
- [Unit Economics](../08-Finance/Unit-Economics.md)
- [Open Questions](./Open-Questions.md)

## Table of Contents

1. [Marketplace Concepts](#marketplace-concepts)
2. [Two-Sided Platform Dynamics](#two-sided-platform-dynamics)
3. [Roadside Assistance Industry Concepts](#roadside-assistance-industry-concepts)
4. [Operations Frameworks](#operations-frameworks)
5. [Financial & Growth Concepts](#financial--growth-concepts)
6. [Go-To-Market Concepts](#go-to-market-concepts)
7. [Strategic Frameworks](#strategic-frameworks)
8. [Business Examples](#business-examples)
9. [Business Decisions](#business-decisions)
10. [Risks](#risks)
11. [Assumptions](#assumptions)
12. [Open Questions](#open-questions)
13. [Next Steps](#next-steps)

---

## Marketplace Concepts

### Asset-Light Marketplace Model

Salik Assist operates without owning tow trucks, employing drivers, or maintaining garages. The platform orchestrates discovery, matching, payment, and quality assurance between independent supply (providers) and demand (customers). Capital efficiency enables faster geographic expansion than fleet-based competitors.

### Intermediary Positioning

Salik Assist is legally and operationally an **intermediary** — not a transport operator, recovery company, or insurer. The service contract exists between customer and provider. The platform facilitates the transaction and enforces quality standards without performing the service directly.

### Take Rate (Commission) Economics

The platform retains a percentage (18% standard) of each completed job's value. Take rate aligns platform revenue with successful job completion — both parties benefit only when service is delivered. Take rate must balance unit economics (platform sustainability) with provider acceptance (supply retention).

### Liquidity

Marketplace **liquidity** is the probability that a customer request matches with a provider quickly. Measured by time-to-first-offer and offer acceptance rate. Insufficient liquidity (thin provider density) is the primary launch failure mode. Salik Assist targets ≤5 minute P90 time-to-offer.

### Network Effects

As more providers join, customers receive faster/better offers (more choice, lower ETAs). As more customers join, providers receive more demand (higher utilization, better earnings). **Cross-side network effects** are Salik Assist's primary competitive moat once liquidity is established.

---

## Two-Sided Platform Dynamics

### Chicken-and-Egg Problem

Marketplaces face simultaneous need for supply (providers) and demand (customers). Salik Assist strategy: **supply-first** — pre-sign 150+ verified providers before consumer launch; use zero-commission promo to attract supply; concentrate geographically to achieve density.

### Multi-Homing

Providers and customers can use multiple platforms simultaneously. Salik Assist assumes **multi-homing on provider side** (providers use Salik + phone dispatch + competitor apps). Differentiation through verification, payment guarantee, demand quality, and performance rewards — not exclusivity (at launch).

### Disintermediation Risk

Customers and providers may circumvent the platform to avoid commission (direct payment). Mitigated by: payment convenience, dispute protection, verification trust, provider penalties, and customer incentives (credits, subscription).

### Surge Pricing / Dynamic Pricing

During peak demand (summer heat, holiday weekends, rush hour), prices increase to balance supply and demand. Salik Assist caps surge at 2.5× base. Provider receives 80% of surge premium. Manual surge at MVP; automated in Phase 1.

### Top-3 Competitive Offer Model

Unlike ride-hail auto-assign, Salik Assist presents up to 3 provider offers for customer choice. Balances transparency (customer selects based on ETA, price, rating) with speed (limited to 3 to avoid choice paralysis in emergencies).

---

## Roadside Assistance Industry Concepts

### Breakdown Event

An incident where a vehicle becomes immobilized or unsafe to drive — flat tire, dead battery, engine failure, accident, out of fuel, lockout. High-stress, time-sensitive, often in unsafe locations (highway shoulder, desert, parking structure).

### Service Category Mix

Roadside assistance demand splits across categories: tow (~45%), battery (~25%), tire (~15%), fuel/mechanic/lockout (~15%). Category mix affects average job value, margin, and provider recruitment strategy. UAE climate skews toward battery failures (extreme heat).

### Insurance-Linked Roadside

Most motor insurance policies in UAE include roadside assistance as a benefit — typically via insurer call center dispatching to contracted providers. Salik Assist **B2B2C model** digitizes this flow: insurer routes policyholders to Salik network with pre-negotiated rates.

### Informal Supply Market

Majority of UAE roadside assistance today flows through informal channels: phone numbers on tow truck signage, WhatsApp groups, highway patrol referrals. Salik Assist digitizes this fragmented supply without requiring providers to abandon existing channels.

### Call-Out Fee Structure

Industry standard: if provider arrives on-site but service is not performed (customer cancels, issue resolved), a call-out/dispatch fee applies. Salik Assist implements this at cancellation stage S3 (AED 75) with provider receiving 80%.

---

## Operations Frameworks

### Seven-Stage Operations Workflow

Salik Assist standard job lifecycle: Request → Matching → Acceptance → En Route → Service → Payment → Review. Each stage has defined owners, time targets, and escalation triggers. See [Operations Workflow](../06-Operations/Operations-Workflow.md).

### Salik Performance Score (SPS)

Composite provider score (0–100) from weighted metrics: rating (30%), ETA accuracy (20%), acceptance rate (15%), completion rate (15%), response time (10%), cancellation rate (10%). Drives matching priority and tier benefits.

### Verification as Trust Moat

In emergency contexts, trust is the primary purchase driver. Salik Assist verification (trade license, insurance, permits, background check) creates differentiation vs. informal alternatives. No provider receives offers until Tier 1 verified.

### Escalation Tier System

Four-tier escalation (Support Agent → Supervisor → Head of Ops/Quality → GM/Legal) with severity levels P1–P4. Automatic triggers at defined time thresholds (e.g., zero offers at 5 minutes, no-show at 15 minutes).

### Quality Control Layers

Four layers: Prevention (verification, training), Detection (ratings, flags, audits), Correction (refunds, coaching, suspension), Improvement (root cause analysis, policy updates).

---

## Financial & Growth Concepts

### Unit Economics

Per-job profitability: Platform revenue (commission) minus variable costs (payment processing, support, remedies). Target contribution margin ≥12% of GMV at maturity. See [Unit Economics](../08-Finance/Unit-Economics.md).

### LTV:CAC in Low-Frequency Categories

Roadside assistance is inherently low-frequency (1–2 events/customer/year). LTV:CAC ratio starts below 1:1 in Year 1. **Subscription product (Phase 2)** and **B2B2C channels** are required to reach 3:1 LTV:CAC target.

### Cohort Retention

Tracking customer behavior by acquisition month. Key metric: D365 repeat rate (% completing second job within 365 days). Target: 15% Y1 → 35% Y3. Repeat rate is the primary LTV lever.

### Break-Even Volume

Fixed costs divided by contribution margin per job. Salik Assist break-even: ~24,000 jobs/month (Month 22–26). Achieved through geographic expansion and B2B volume, not B2C alone.

### GMV vs. Net Revenue

**GMV** = total customer spend (AED 154M Year 3). **Net revenue** = platform's share (AED 27.9M Year 3). Investors evaluate both: GMV shows market traction; net revenue shows business scale.

---

## Go-To-Market Concepts

### Supply-First Launch

Recruit and verify providers before marketing to customers. Prevents liquidity failure at launch. Target: 150 providers activated 2 weeks before consumer app go-live.

### Geographic Zone Gating

Launch in constrained geography (Dubai metro + highways) to concentrate liquidity. Expand only when zone SLA metrics met. Prevents thin coverage across wide area.

### Emergency Intent Marketing

Customers often discover roadside assistance during active breakdown (search "tow truck Dubai"). Guest checkout and mobile web capture emergency intent. SEO and performance marketing target high-intent keywords.

### Preparedness Marketing

Long-term strategy: install Salik Assist app **before** breakdown occurs. Content marketing (battery checks, tire safety), dealership partnerships, subscription product. Shifts customer from emergency acquisition to planned retention.

### B2B as Demand Anchor

Insurance and fleet partnerships provide predictable, high-volume demand at lower effective CAC. B2B2C end users cost AED 10 to acquire vs. AED 55 for paid marketing. Target: 32% B2B share by Phase 3.

---

## Strategic Frameworks

### Phase-Gated Roadmap

MVP (prove) → Phase 1 (expand) → Phase 2 (deepen) → Phase 3 (scale). Each phase has entry criteria (go/no-go gates) preventing premature expansion. Kill criteria if MVP fails Day 90 review.

### Competitive Moat Stack

Salik Assist moats layered over time:
1. **Verification trust** (launch)
2. **Provider density / liquidity** (Phase 1)
3. **B2B partnerships** (Phase 1–2)
4. **Brand recognition** (Phase 2)
5. **Subscription retention** (Phase 2)
6. **Regional scale** (Phase 3)

### SAM / SOM / TAM

- **TAM:** Total roadside assistance spending in GCC
- **SAM:** Digitally addressable marketplace transactions (~AED 660–880M UAE)
- **SOM:** Salik Assist realistic capture Year 3 (~AED 154M GMV = ~18% digital share)

### Series A Readiness Narrative

Documentation phase produces investor-ready materials: market size, business model, unit economics, roadmap, ops policies, legal framework. Salik Assist targets $6–8M Series A at launch readiness.

---

## Business Examples

**Example 1 — Network effects in action:** Month 6 Dubai. Provider density reaches 280. Time-to-offer drops from 6 min (M1) to 3.5 min (M6). Customer satisfaction rises. More customers leave 4+ star ratings. More providers join seeing demand. Virtuous cycle begins.

**Example 2 — Chicken-and-egg resolution:** Pre-launch: 150 providers signed with zero-commission promo before any customer marketing. Launch day: 94 jobs, 88% get offers within 5 minutes. Supply-first strategy prevents liquidity failure.

**Example 3 — LTV:CAC with subscription:** Without subscription: customer LTV AED 40, CAC AED 50 = 0.8:1 (unprofitable). With 12% subscription adoption: blended LTV AED 63, CAC AED 45 = 1.4:1 (improving). Subscription is structural fix for low-frequency economics.

---

## Business Decisions

| Decision | Rationale |
|----------|-----------|
| Separate Business Terminology from Glossary | Concepts need explanation; terms need definitions |
| Document marketplace dynamics explicitly | Team may not have marketplace experience |
| Include low-frequency LTV:CAC challenge | Honest framing for investors and team |
| Phase-gated framework as core concept | Prevents over-expansion; capital discipline |
| Supply-first as documented strategy | Most common marketplace launch failure is thin liquidity |

---

## Risks

| Risk | Impact | Mitigation |
|------|--------|------------|
| Concepts not understood consistently | Medium | Training; glossary cross-reference |
| Framework over-application | Low | Frameworks guide, not dictate |
| Outdated concepts as business evolves | Medium | Quarterly review with roadmap |
| Investor terminology mismatch | Low | Align with standard VC marketplace vocabulary |

---

## Assumptions

- Team includes members new to marketplace businesses
- Investors familiar with marketplace terminology but not roadside specifically
- Concepts remain stable across MVP through Phase 3
- Arabic business terminology translation needed for KSA team (Phase 3)

---

## Open Questions

- Develop internal marketplace training module based on this document?
- Add competitive terminology (how incumbents describe their model)?
- Include visual diagrams for network effects and workflow?
- Business terminology workshop for launch team?

---

## Next Steps

1. Use as onboarding reading for new ops, support, and sales hires
2. Reference in investor deck speaker notes
3. Update as new business concepts emerge (subscription, KSA localization)
4. Cross-link from Glossary terms to relevant concept sections
5. Review at quarterly roadmap sessions
