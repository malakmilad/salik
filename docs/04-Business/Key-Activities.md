# Key Activities — Salik Assist

| Field | Value |
|-------|-------|
| **Version** | 1.0 |
| **Status** | Draft |
| **Author** | Product & Strategy Team |
| **Last Updated** | July 4, 2026 |

## Purpose

Define the core business activities Salik Assist must perform to operate, grow, and defend its position as the leading roadside assistance marketplace in the GCC.

## Scope

Business and operational activities, ownership, and success criteria. Excludes technical development tasks, engineering sprints, and system administration.

## Related Documents

- [Business Model Canvas](./Business-Model-Canvas.md)
- [Key Partnerships](./Key-Partnerships.md)
- [Business Requirements](./Business-Requirements.md)
- [Business Rules](./Business-Rules.md)
- [Cost Structure](./Cost-Structure.md)

## Table of Contents

1. [Activities Overview](#activities-overview)
2. [Marketplace Core Activities](#marketplace-core-activities)
3. [Supply-Side Activities](#supply-side-activities)
4. [Demand-Side Activities](#demand-side-activities)
5. [B2B & Partnership Activities](#b2b--partnership-activities)
6. [Trust & Quality Activities](#trust--quality-activities)
7. [Financial & Commercial Activities](#financial--commercial-activities)
8. [Expansion Activities](#expansion-activities)
9. [Activity Ownership Matrix](#activity-ownership-matrix)
10. [Business Examples](#business-examples)
11. [Business Decisions](#business-decisions)
12. [Risks](#risks)
13. [Assumptions](#assumptions)
14. [Open Questions](#open-questions)
15. [Next Steps](#next-steps)

---

## Activities Overview

Salik Assist key activities cluster into six domains aligned to marketplace health:

```
┌─────────────────────────────────────────────────────────────┐
│                    MARKETPLACE CORE                          │
│  Matching • Dispatch • Job Lifecycle • Zone Management       │
├──────────────────────┬──────────────────────────────────────┤
│   SUPPLY-SIDE        │         DEMAND-SIDE                   │
│  Recruit • Verify    │  Acquire • Support • Retain           │
│  Onboard • Train     │  Promote • Refer                      │
├──────────────────────┴──────────────────────────────────────┤
│  TRUST & QUALITY          │  FINANCIAL & COMMERCIAL          │
│  Disputes • Audits        │  Payouts • Reconciliation        │
│  Ratings • Compliance     │  Pricing • Reporting             │
├───────────────────────────┴─────────────────────────────────┤
│              EXPANSION: New zones • Categories • Markets      │
└─────────────────────────────────────────────────────────────┘
```

---

## Marketplace Core Activities

| Activity | Description | Frequency | Owner |
|----------|-------------|-----------|-------|
| **Request intake & validation** | Ensure customer requests have valid location, category, and coverage | Continuous | Operations |
| **Provider matching** | Identify eligible providers by proximity, category, availability, rating | Continuous | Operations |
| **Offer orchestration** | Manage 5-minute offer window; compile top-3 for customer | Continuous | Operations |
| **Dispatch confirmation** | Confirm acceptance; notify all parties; initiate tracking | Continuous | Operations |
| **Job lifecycle monitoring** | Track jobs through all states; escalate stalled jobs (Rule 40) | Continuous | Operations |
| **Zone & coverage management** | Define, gate, and expand geographic service zones | Weekly | Operations |
| **Surge management** | Activate/deactivate surge; monitor supply/demand ratios | Daily (peak season) | Operations |
| **Marketplace health reporting** | Fill rate, offer rate, completion rate, avg ETA | Weekly | Operations |

**Success metrics:** 90%+ offer rate in 5 min; 95%+ completion rate; median ETA accuracy ±5 min.

---

## Supply-Side Activities

| Activity | Description | Frequency | Owner |
|----------|-------------|-----------|-------|
| **Provider prospecting** | Identify tow yards, mechanics, battery shops in target zones | Daily | Field Sales |
| **Provider recruitment events** | Association events, yard visits, referral campaigns | Weekly | Field Sales |
| **Document verification** | Review license, insurance, ID, vehicle registration | Daily | Verification Team |
| **Background checks** | Coordinate driver screening with partner | Per new driver | Verification Team |
| **Provider onboarding** | App setup, rules training, test job walkthrough | Per provider | Operations |
| **Provider support** | Operational queries, payout issues, account changes | Continuous | Support |
| **Performance management** | Rating monitoring; improvement plans (Rules 7–8) | Weekly | Operations |
| **Provider retention** | Check-ins with top and at-risk providers | Monthly | Account Management |
| **Subscription upsell** | Professional/Premium tier conversion | Monthly | Field Sales |

**Success metrics:** 150+ verified providers at launch; <5% monthly provider churn; 4.2+ avg provider rating.

---

## Demand-Side Activities

| Activity | Description | Frequency | Owner |
|----------|-------------|-----------|-------|
| **Performance marketing** | Paid search, social, app store optimization | Daily | Marketing |
| **Brand marketing** | PR, content, highway signage, event sponsorship | Monthly | Marketing |
| **Referral program management** | Customer and provider referral tracking and rewards | Continuous | Marketing |
| **SEO & emergency-intent capture** | "Tow truck near me" and Arabic equivalent content | Ongoing | Marketing |
| **Customer support** | Pre-job queries, active job assistance, post-job follow-up | Continuous | Support |
| **Customer retention** | Re-engagement campaigns; app rating prompts | Monthly | Marketing |
| **Launch promotions** | First rescue free; zone-specific campaigns | Per campaign | Marketing |

**Success metrics:** CAC < $28 Year 1; 40%+ monthly active user retention; 4.5+ app store rating.

---

## B2B & Partnership Activities

| Activity | Description | Frequency | Owner |
|----------|-------------|-----------|-------|
| **Partner pipeline development** | Insurer, fleet, dealer prospect identification | Weekly | Partnerships |
| **Partnership negotiation** | Commercial terms, rate cards, SLA agreements | Per deal | Partnerships |
| **Partner onboarding** | Contract execution; co-marketing plan; training | Per partner | Partnerships |
| **SLA reporting & QBRs** | Monthly reports; quarterly business reviews | Monthly/Quarterly | Account Management |
| **Co-marketing execution** | Joint campaigns, app embeds, policyholder comms | Per campaign | Partnerships + Marketing |
| **B2B billing & invoicing** | Monthly partner invoices with job detail | Monthly | Finance |

**Success metrics:** 1 insurer live by Month 8; 3 LOIs Year 1; B2B 25% of volume by Year 3.

---

## Trust & Quality Activities

| Activity | Description | Frequency | Owner |
|----------|-------------|-----------|-------|
| **Dispute intake & resolution** | Customer and provider disputes (Rules 56–60) | Continuous | Operations |
| **Job audit & fraud detection** | GPS verification; photo review; pattern analysis | Daily | Quality Assurance |
| **Rating moderation** | Review profanity, fraud, discriminatory content | Daily | Support |
| **Insurance expiry monitoring** | Auto-suspend providers with lapsed documents | Daily (automated alert) | Verification |
| **Compliance reporting** | Regulatory audit support; consumer protection | As needed | Legal |
| **Safety incident response** | Escalation protocol for customer/provider safety events | As needed | Operations + Legal |
| **Customer guarantee fund management** | Dispute refund processing | Per dispute | Finance |

**Success metrics:** <2% dispute rate; <72 hr dispute resolution; 100% verification compliance.

---

## Financial & Commercial Activities

| Activity | Description | Frequency | Owner |
|----------|-------------|-----------|-------|
| **Commission collection** | Automatic deduction at payment | Per job | Finance |
| **Provider payout processing** | 48-hour payout SLA (Rule 47) | Daily | Finance |
| **Payment reconciliation** | Match payments, commissions, payouts | Daily | Finance |
| **Pricing guardrail management** | Update min/max rates by zone and category | Quarterly | Operations + Finance |
| **Promotional budget tracking** | Monitor CAC and promo ROI | Weekly | Finance + Marketing |
| **Financial reporting** | P&L, cash flow, unit economics dashboards | Monthly | Finance |
| **Tax documentation for providers** | Annual earnings statements | Annual | Finance |

**Success metrics:** 98%+ payout within 48 hours; 100% commission capture; monthly close within 10 days.

---

## Expansion Activities

| Activity | Description | Timing | Owner |
|----------|-------------|--------|-------|
| **New zone launch** | Provider density check; marketing; zone gating lift | Per zone | City Launch Manager |
| **New service category** | Provider recruitment; guardrails; customer education | Per category | Operations |
| **New emirate launch** | Abu Dhabi, Sharjah expansion playbook | Month 7–12 | City Launch Manager |
| **KSA market entry** | Regulatory review; local partnerships; provider recruitment | Year 2 | GM + Partnerships |
| **Category expansion (desert/EV)** | Specialist provider tier; premium guardrails | Year 2 | Operations |

**Success metrics:** 3 UAE emirates by Month 12; KSA plan approved by Month 12.

---

## Activity Ownership Matrix

| Activity Domain | Primary Owner | Supporting Functions |
|----------------|---------------|---------------------|
| Marketplace core | Head of Operations | Product, Support |
| Supply-side | Head of Operations | Field Sales, Verification |
| Demand-side | Head of Marketing | Support, Partnerships |
| B2B & partnerships | Head of Partnerships | Legal, Finance, Operations |
| Trust & quality | Head of Operations | Legal, Finance |
| Financial | CFO / Finance Lead | Operations, Partnerships |
| Expansion | GM / City Launch Manager | All functions |

---

## Business Examples

**Example 1 — Daily operations rhythm:** Monday 8 AM: ops reviews weekend fill rate (91%), identifies Deira zone offer rate drop to 82%. Field sales deploys to recruit 5 battery providers in Deira by Friday. Offer rate recovers to 94% following week.

**Example 2 — Verification activity:** New tow provider submits documents Tuesday. Verification team reviews within 24 hours; background check initiated. Thursday: approved and onboarded. Friday: completes first job with 5-star rating.

**Example 3 — B2B QBR activity:** Quarterly business review with insurer partner: presents 4,200 dispatches, 93% within 45-min ETA, 4.6 CSAT, 1.8% dispute rate. Partner renews contract and adds Sharjah coverage.

---

## Business Decisions

| Decision | Rationale |
|----------|-----------|
| Operations owns marketplace core (not outsourced) | Quality and trust are core product |
| Field sales for provider recruitment (not digital-only) | Tow yards require in-person relationship |
| Verification as dedicated activity (not ops generalist) | Bottleneck prevention at scale |
| Dispute resolution human-led at launch | Trust-critical; automation later |
| City launch managers for geographic expansion | Local knowledge and accountability |

---

## Risks

| Risk | Impact | Mitigation |
|------|--------|------------|
| Operations team overwhelmed at launch | High | Pre-hire; playbooks; escalation tiers |
| Verification bottleneck delays supply | High | Dedicated team; contractor surge capacity |
| Field sales underperforms on provider targets | High | Association partnerships; referral bonuses |
| B2B activities distract from B2C core | Medium | Separate partnerships team |
| Expansion activities premature | Medium | Milestone gates on zone/emirate launch |

---

## Assumptions

- 22 FTE equivalent sufficient for Year 1 activity coverage
- Operations runs 16/7 coverage at launch (UAE hours + peak extension)
- Field sales can recruit 150 providers in 90 days with association support
- Dispute volume < 2% of jobs manageable with 2 dedicated staff
- City launch manager model scales to KSA in Year 2

---

## Open Questions

- 16/7 vs. 24/7 operations at launch?
- Outsource verification at launch or keep in-house?
- Single city launch manager for all UAE or per-emirate?
- When to introduce automated dispute triage?
- Which activity to deprioritize if hiring behind plan?

---

## Next Steps

1. Hire Head of Operations and verification team (priority)
2. Document SOPs for top 10 activities before launch
3. Define weekly ops review cadence and dashboard
4. Field sales pilot: 30 providers in 30 days test
5. Align activity ownership with Series A hiring plan
