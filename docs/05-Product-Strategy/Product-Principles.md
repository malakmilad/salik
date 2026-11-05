# Product Principles — Salik Assist

| Field | Value |
|-------|-------|
| **Version** | 1.0 |
| **Status** | Draft |
| **Author** | Product & Strategy Team |
| **Last Updated** | July 4, 2026 |

## Purpose

Establish the non-negotiable product principles that guide every feature decision, design choice, and trade-off for Salik Assist. Principles translate strategy into daily product judgment—what we build, what we refuse, and how we resolve conflicts.

## Scope

Product and experience principles for customer, provider, and partner surfaces. Excludes engineering principles, security policies, and technical architecture standards.

## Related Documents

- [Product Vision](./Product-Vision.md)
- [Product Strategy](./Product-Strategy.md)
- [Vision](../01-Executive/Vision.md)
- [Mission](../01-Executive/Mission.md)
- [Personas](../02-Market-Research/Personas.md)
- [Business Rules](../04-Business/Business-Rules.md)
- [SLA](../06-Operations/SLA.md)
- [North Star Metric](./North-Star-Metric.md)
- [User Flows](../09-UX/User-Flows.md)

## Table of Contents

1. [How to Use These Principles](#how-to-use-these-principles)
2. [Principle 1: Rescue the Stressed User First](#principle-1-rescue-the-stressed-user-first)
3. [Principle 2: Three Offers Beat One Surprise](#principle-2-three-offers-beat-one-surprise)
4. [Principle 3: Trust Is Visible](#principle-3-trust-is-visible)
5. [Principle 4: Complete the Job, Not the Click](#principle-4-complete-the-job-not-the-click)
6. [Principle 5: Providers Are Partners, Not Pixels](#principle-5-providers-are-partners-not-pixels)
7. [Principle 6: Price Clarity Before Commitment](#principle-6-price-clarity-before-commitment)
8. [Principle 7: Arabic and English Are Equals](#principle-7-arabic-and-english-are-equals)
9. [Principle 8: Liquidity Over Novelty](#principle-8-liquidity-over-novelty)
10. [Principle 9: Fairness in Matching](#principle-9-fairness-in-matching)
11. [Principle 10: Disputes Deserve Dignity](#principle-10-disputes-deserve-dignity)
12. [Principle Conflict Resolution](#principle-conflict-resolution)
13. [Business Examples](#business-examples)
14. [Business Decisions](#business-decisions)
15. [Risks](#risks)
16. [Assumptions](#assumptions)
17. [Open Questions](#open-questions)
18. [Next Steps](#next-steps)

---

## How to Use These Principles

When evaluating any product initiative, ask:

1. Which principles does this strengthen?
2. Which principles does this weaken?
3. If two principles conflict, which serves the North Star (**Successfully Completed Assisted Jobs**) and the distressed customer more directly?

Principles are ranked implicitly by urgency in emergency contexts: **stress reduction and trust** outweigh **growth hacks**; **completed jobs** outweigh **vanity engagement**.

---

## Principle 1: Rescue the Stressed User First

**Statement:** Every product flow assumes the customer may be stranded, unsafe, overheated, or panicking.

**In practice:**
- Minimize steps from open app to help requested (target: ≤5 taps)
- Large touch targets, high contrast, readable in sunlight
- Location auto-detected; manual override always available
- No mandatory account creation before first rescue request (if legally permissible)
- Error messages are calm, specific, and action-oriented—not technical

**We reject:** Onboarding tutorials, social sharing prompts, or upsell modals before help is dispatched.

---

## Principle 2: Three Offers Beat One Surprise

**Statement:** Customers deserve competitive choice at the moment of need—not opaque auto-assignment.

**In practice:**
- Surface up to three matched provider offers with comparable information density
- Show ETA, price estimate, rating, and verification status on every offer card
- If fewer than three providers are available, show honest count and expected wait—not fake placeholders
- Never auto-accept on behalf of the customer without explicit consent

**We reject:** Dark patterns that rush acceptance of the first or only offer; hidden platform-preferred routing.

---

## Principle 3: Trust Is Visible

**Statement:** Verification, insurance, licenses, and ratings appear where customers decide—not buried in settings.

**In practice:**
- Verification badges on offer cards and provider profiles
- Expired credentials automatically hide provider from results
- Post-job ratings influence future matching visibility
- Safety incident history triggers review before reactivation

**We reject:** Unverified providers in customer-facing results; "verified" labels without defined criteria.

---

## Principle 4: Complete the Job, Not the Click

**Statement:** Product success is measured by Successfully Completed Assisted Jobs—not downloads, sign-ups, or requests alone.

**In practice:**
- Optimize funnels for acceptance → arrival → payment → rating
- Celebrate and instrument completion milestones in internal metrics
- Deprioritize features that inflate top-of-funnel without improving fill rate
- Provider product equally optimized for job completion and payout

**We reject:** Growth metrics that reward abandoned requests or unfulfilled dispatches.

---

## Principle 5: Providers Are Partners, Not Pixels

**Statement:** Providers are independent businesses; the product must help them earn more with dignity and clarity.

**In practice:**
- Transparent commission and fee disclosure at onboarding
- Fair offer distribution—not perpetual starvation of new providers
- Fast, reliable payout after job completion
- Provider-facing tools for earnings, ratings, and schedule control
- No punitive deactivation without explanation and appeal path

**We reject:** Treating providers as interchangeable supply units; surprise fee deductions; unilateral policy changes without notice.

---

## Principle 6: Price Clarity Before Commitment

**Statement:** Customers should understand expected cost before accepting an offer, with narrow, explained variance after service.

**In practice:**
- Price ranges or caps shown on offer cards
- Surcharges (night, highway, heavy vehicle) disclosed upfront
- Final price within agreed tolerance or customer notified before proceeding
- Receipt itemization after payment

**We reject:** Bait pricing; post-service price surprises without customer approval; hidden platform fees at checkout.

---

## Principle 7: Arabic and English Are Equals

**Statement:** UAE launch requires full Arabic and English parity—not translation as an afterthought.

**In practice:**
- All customer and provider flows available in both languages
- RTL layout quality matches LTR
- Support content and dispute communications in customer's language
- Marketing and in-app tone culturally appropriate, not machine-translated

**We reject:** English-only launch with "Arabic coming soon"; broken RTL layouts; Romanized Arabic substitutes.

---

## Principle 8: Liquidity Over Novelty

**Statement:** No new category, city, or feature ships if it degrades core zone liquidity.

**In practice:**
- Launch gates tied to Liquidity Index and SCAJ density
- Geographic expansion only after Dubai zones meet thresholds
- New service categories added only when anchor categories are healthy
- Marketing spend follows supply density, not vice versa

**We reject:** National marketing blitz with hollow coverage; feature launches that distract ops from supply recruitment.

---

## Principle 9: Fairness in Matching

**Statement:** Matching balances customer need, provider merit, proximity, and marketplace sustainability.

**In practice:**
- Proximity and ETA weighted heavily for emergencies
- Ratings and completion history influence offer visibility—not pay-to-win alone
- New providers receive onboarding exposure windows to build reputation
- Promoted listings labeled clearly if introduced

**We reject:** Pure auction to lowest bidder; permanent shadowban without cause; pay-for-rank without disclosure.

---

## Principle 10: Disputes Deserve Dignity

**Statement:** Breakdowns are stressful; disputes must be fast, fair, and human.

**In practice:**
- In-app dispute initiation with photo/evidence upload
- Target resolution within 48 hours for standard cases
- Interim credits when provider no-show is verified
- Clear escalation to human support for safety issues

**We reject:** Opaque dispute black holes; forcing phone-only resolution; blaming customers for provider failures.

---

## Principle Conflict Resolution

| Conflict | Resolution |
|----------|------------|
| Speed vs. choice | Show partial offers quickly; refresh as more arrive; never fake three |
| Provider earnings vs. low customer price | Platform absorbs promo cost, not provider payout |
| B2B rate caps vs. provider margin | Negotiate B2B within provider-acceptable floors |
| Growth vs. verification | Slow onboarding before unverified supply in market |
| Feature richness vs. stress UX | Cut scope; ship minimal rescue path |

---

## Business Examples

**Example 1 — Principle 1 in action:** Design proposes a 6-screen onboarding before first request. Product rejects; implements phone-verify on first request and profile completion post-rescue.

**Example 2 — Principle 2 vs. ops efficiency:** Ops suggests auto-assign to fastest provider. Product rejects; data shows customer acceptance 23% higher when choosing among three offers.

**Example 3 — Principle 8 gate:** Marketing requests UAE-wide launch campaign. Product blocks until Dubai Marina Liquidity Index exceeds 65% for 4 consecutive weeks.

**Example 4 — Principle 5 payout:** Provider complains of 14-day payout. Product prioritizes 48-hour settlement in roadmap—provider retention linked directly to Principle 5.

---

## Business Decisions

| Decision | Principle Applied |
|----------|-------------------|
| Top-3 offer model at launch | #2 Three Offers Beat One Surprise |
| Verification required before activation | #3 Trust Is Visible |
| SCAJ as North Star metric | #4 Complete the Job, Not the Click |
| Zero-commission launch period for providers | #5 Providers Are Partners |
| Upfront price ranges on offers | #6 Price Clarity Before Commitment |
| Bilingual launch requirement | #7 Arabic and English Are Equals |
| Deferred Sharjah launch until Dubai gates | #8 Liquidity Over Novelty |

---

## Risks

| Risk | Description |
|------|-------------|
| Principles honored in docs, ignored in sprint pressure | Shortcuts erode trust at launch |
| Over-literal interpretation slows shipping | Balance principles with MVP pragmatism |
| Provider principles conflict with margin pressure | Commission disputes if Principle 5 violated |
| B2B partners demand auto-assign | Contract terms may force Principle 2 exceptions |

---

## Assumptions

- Product team has authority to veto features that violate core principles
- Principles remain stable for 12 months post-launch to build team muscle memory
- Customer and provider research validates stress-first and top-3 assumptions
- Leadership supports liquidity gates even when growth targets pressure geographic expansion

---

## Open Questions

- Guest checkout for first request—does it violate trust/compliance or serve Principle 1?
- Should Principle 2 allow auto-assign after 10 minutes if customer hasn't chosen?
- Provider appeal process owner—product or operations?
- How to label promoted provider placement without violating Principle 9?

---

## Next Steps

1. Distribute principles to product, design, operations, and support teams
2. Add principle checklist to feature review template
3. Audit [MVP](../09-Roadmap/MVP.md) scope against principles; cut conflicts
4. Include principles in provider onboarding materials
5. Quarterly principle retrospective post-launch—what held, what needs amendment
