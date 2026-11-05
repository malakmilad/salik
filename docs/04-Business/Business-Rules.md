# Business Rules — Salik Assist

| Field | Value |
|-------|-------|
| **Version** | 1.0 |
| **Status** | Draft |
| **Author** | Product & Strategy Team |
| **Last Updated** | July 4, 2026 |

## Purpose

Define explicit, numbered business rules governing marketplace operations for Salik Assist—covering provider eligibility, matching, pricing, job lifecycle, payments, disputes, and partner interactions. These rules are authoritative for operations, legal, and product teams.

## Scope

Operational and commercial business rules for the UAE launch marketplace. Excludes technical implementation, system configuration, and engineering logic.

## Related Documents

- [Business Requirements](./Business-Requirements.md)
- [Pricing Strategy](./Pricing-Strategy.md)
- [Revenue Model](./Revenue-Model.md)
- [Constraints](./Constraints.md)
- [Risk Register](./Risk-Register.md)

## Table of Contents

1. [Rules Overview](#rules-overview)
2. [Provider Eligibility & Verification Rules](#provider-eligibility--verification-rules)
3. [Provider Conduct & Account Rules](#provider-conduct--account-rules)
4. [Customer Request & Eligibility Rules](#customer-request--eligibility-rules)
5. [Matching & Offer Rules](#matching--offer-rules)
6. [Pricing & Surge Rules](#pricing--surge-rules)
7. [Job Lifecycle Rules](#job-lifecycle-rules)
8. [Cancellation Rules](#cancellation-rules)
9. [Payment & Commission Rules](#payment--commission-rules)
10. [Rating, Review & Quality Rules](#rating-review--quality-rules)
11. [Dispute Resolution Rules](#dispute-resolution-rules)
12. [B2B Partner Rules](#b2b-partner-rules)
13. [Geographic & Service Rules](#geographic--service-rules)
14. [Business Examples](#business-examples)
15. [Business Decisions](#business-decisions)
16. [Risks](#risks)
17. [Assumptions](#assumptions)
18. [Open Questions](#open-questions)
19. [Next Steps](#next-steps)

---

## Rules Overview

| Attribute | Value |
|-----------|-------|
| Total rules | 70 |
| Rule format | **Rule [N]:** [Statement] |
| Enforcement | Operations, automated policy, and legal terms |
| Change authority | Product & Strategy Team with Legal and Operations sign-off |
| Review cadence | Quarterly or upon material market change |

---

## Provider Eligibility & Verification Rules

**Rule 1:** No provider may receive or accept job offers until all mandatory verification documents are submitted, reviewed, and approved by Salik Assist operations.

**Rule 2:** Mandatory verification documents include: valid UAE trade license (or equivalent for applicable free zone), commercial vehicle insurance certificate, vehicle registration for each service vehicle, and government-issued ID for the account owner and each active driver.

**Rule 3:** Provider insurance must cover minimum third-party liability of AED 1,000,000 per incident and include roadside assistance or recovery operations as covered activity.

**Rule 4:** Background checks must be completed for all drivers before the driver is authorized to perform jobs. Providers must notify Salik Assist within 48 hours of adding or replacing a driver.

**Rule 5:** Providers whose insurance, license, or background check expires or fails renewal review must be suspended from receiving new offers immediately upon expiry date. In-progress jobs may be completed.

**Rule 6:** Salik Assist reserves the right to reject or revoke provider status for falsified documents, without refund of any fees paid.

**Rule 7:** Providers must maintain a minimum platform rating of 3.5 stars over a rolling 90-day period. Providers falling below this threshold enter a 30-day performance improvement period.

**Rule 8:** Providers falling below 3.0 stars over a rolling 90-day period, or failing improvement period conditions, may be deactivated from the platform.

---

## Provider Conduct & Account Rules

**Rule 9:** Providers operate as independent businesses. Salik Assist does not employ providers, direct their work methods, or provide service vehicles or equipment.

**Rule 10:** Provider accounts are non-exclusive. Providers may operate on competing platforms and accept offline jobs, provided they honor accepted Salik Assist commitments.

**Rule 11:** Providers must not solicit customers to complete jobs off-platform to avoid commission. First violation results in warning; second violation results in account suspension.

**Rule 12:** Providers must respond to incoming job offers within 3 minutes during declared available hours. Repeated non-response (≥5 instances in 7 days) may reduce offer priority.

**Rule 13:** Providers must use the registered service vehicle and authorized driver listed on the accepted job. Substitutions require customer consent via platform.

**Rule 14:** Providers must maintain professional conduct, bilingual communication capability (Arabic or English minimum), and branded identification visible to customers upon arrival.

---

## Customer Request & Eligibility Rules

**Rule 15:** Customers must be 18 years or older to create an account and request services.

**Rule 16:** Customers must provide accurate location, vehicle type, and issue category. Knowingly false information that results in provider dispatch may incur a no-show or misrepresentation fee.

**Rule 17:** Customers may have no more than 2 active (uncompleted) service requests at any time.

**Rule 18:** Customers with 3 or more unresolved payment disputes or chargebacks in 12 months may have account restrictions applied pending review.

**Rule 19:** Salik Assist may refuse service requests in areas outside active coverage zones, with a clear message to the customer before request submission where possible.

---

## Matching & Offer Rules

**Rule 20:** Upon a valid service request, the platform must identify and notify eligible providers based on proximity, service category match, availability status, and verification standing.

**Rule 21:** The platform must present up to three (3) provider offers to the customer when three or more eligible providers respond within the offer window.

**Rule 22:** The offer window is 5 minutes from request submission. If fewer than three providers respond, all valid offers received within the window are presented.

**Rule 23:** If zero providers respond within the offer window, the customer is notified with option to retry, expand radius (if available), or contact support.

**Rule 24:** Each offer must include: provider name, rating, estimated arrival time (ETA), price estimate range, service category confirmation, and verification badge.

**Rule 25:** Customers select one offer to accept. Once accepted, other offers are automatically withdrawn.

**Rule 26:** Providers whose offer is not selected receive no penalty for non-selection. Providers who accept but fail to proceed may incur reliability penalties.

**Rule 27:** Auto-assignment without customer choice is not permitted in standard B2C flows unless explicitly configured under a B2B partner contract with prior customer consent.

---

## Pricing & Surge Rules

**Rule 28:** Providers set their base rates within platform-defined minimum and maximum guardrails per service category and zone.

**Rule 29:** Price estimates shown to customers are ranges based on provider-declared rates and estimated job scope. Final price may vary within the disclosed band based on actual service delivered.

**Rule 30:** Final job price must not exceed the upper bound of the accepted offer estimate by more than 15% without prior customer approval through the platform.

**Rule 31:** Surge pricing may activate when demand exceeds supply by a validated threshold in a defined zone and time window. Surge multiplier is capped at 1.5× base rate.

**Rule 32:** Surge status must be visible to both customer and provider before offer acceptance. Surge revenue is shared: 70% provider / 30% platform on the surge increment only.

**Rule 33:** B2B partner jobs operate under pre-negotiated rate cards that override Rules 28–32 unless contract specifies otherwise.

**Rule 34:** Promotional discounts funded by Salik Assist are deducted from platform revenue, not provider payout, unless explicitly co-funded.

---

## Job Lifecycle Rules

**Rule 35:** A job progresses through defined states: Requested → Offers Presented → Offer Accepted → Provider En Route → Provider Arrived → Service In Progress → Service Completed → Payment Processed → Rated.

**Rule 36:** Provider must mark "Arrived" only when physically at the customer location (within 200 meters). Misuse may trigger audit.

**Rule 37:** Service may not be marked "Completed" by the provider until the customer confirms completion or 15 minutes pass after provider completion request without customer objection.

**Rule 38:** Customers may not be charged until service is marked completed per Rule 37.

**Rule 39:** Providers must upload photographic evidence for jobs exceeding AED 500 in value or involving vehicle towing, as defined in provider guidelines.

**Rule 40:** Jobs unresolved for more than 24 hours in an active (non-completed) state escalate to operations review automatically.

---

## Cancellation Rules

**Rule 41:** Customer cancellation before provider acceptance: no charge.

**Rule 42:** Customer cancellation after provider acceptance but before provider en route: cancellation fee of AED 15 or 10% of estimate (whichever is lower) may apply, shared 50/50 platform and provider.

**Rule 43:** Customer cancellation after provider en route: cancellation fee of AED 30 or 20% of estimate (whichever is lower) applies, with minimum AED 20 provider compensation.

**Rule 44:** Provider cancellation after acceptance without valid reason (breakdown, safety) incurs reliability penalty and potential fee of AED 25 to customer credit.

**Rule 45:** B2B partner cancellation terms follow partner contract; default to Rules 41–44 if contract silent.

---

## Payment & Commission Rules

**Rule 46:** Platform commission (take rate) on standard B2C jobs is 18% of final job value, deducted before provider payout.

**Rule 47:** Provider payout is initiated within 48 hours of job completion and successful payment collection, excluding disputed jobs.

**Rule 48:** Disputed jobs hold provider payout until dispute resolution, up to a maximum hold of 14 days, after which partial release rules apply per dispute outcome.

**Rule 49:** Payment methods accepted from customers include major credit/debit cards and approved local digital wallets. Cash payment is not supported on-platform.

**Rule 50:** Provider subscription fees (if applicable) are billed monthly in advance and are non-refundable for the current billing period.

---

## Rating, Review & Quality Rules

**Rule 51:** Customers may rate completed jobs on a 1–5 star scale within 7 days of completion. Ratings are public on provider profiles.

**Rule 52:** Providers may rate customers on a 1–5 scale for cooperation and accessibility. Customer ratings are internal and not publicly displayed.

**Rule 53:** Reviews containing profanity, personal attacks, or discriminatory language may be removed by moderation.

**Rule 54:** Providers may respond publicly to customer reviews once per review within 14 days of posting.

**Rule 55:** Salik Assist may remove fraudulent ratings identified through pattern analysis or investigation.

---

## Dispute Resolution Rules

**Rule 56:** Customers may file a dispute within 48 hours of job completion for: overcharge vs. estimate, incomplete service, provider no-show, or unprofessional conduct.

**Rule 57:** Salik Assist operations must acknowledge disputes within 4 business hours and aim for resolution within 72 hours.

**Rule 58:** Dispute resolution outcomes include: full refund, partial refund, credit, provider penalty, or no action. Decisions are based on job audit trail, photos, and both party statements.

**Rule 59:** Salik Assist maintains a customer guarantee fund for validated dispute refunds when provider is unable to refund.

**Rule 60:** Providers may dispute commission deductions or customer claims within 7 days, with operations review within 5 business days.

---

## B2B Partner Rules

**Rule 61:** B2B partners must execute a platform agreement before routing customer requests through Salik Assist.

**Rule 62:** B2B partner jobs are tagged at request origin. Commission and dispatch fees follow partner contract terms, which may differ from standard B2C rates.

**Rule 63:** B2B partners receive monthly SLA reports including: total dispatches, average ETA, completion rate, CSAT, and dispute rate.

**Rule 64:** B2B partner branding may appear in the customer journey per contract. Salik Assist verification badges remain visible.

**Rule 65:** B2B partners may not circumvent the platform by directing policyholders to pay providers directly for jobs initiated through Salik Assist.

---

## Geographic & Service Rules

**Rule 66:** Service categories available at launch: vehicle towing, battery jump-start/replacement, flat tire change, emergency fuel delivery, and mobile mechanic (diagnostics + minor repair).

**Rule 67:** Desert and off-road recovery require specialist provider designation and may carry separate rate guardrails.

**Rule 68:** Launch coverage is limited to defined zones in Dubai emirate. Requests outside active zones are rejected with guidance on expected expansion.

**Rule 69:** Cross-emirate jobs (e.g., tow from Dubai to Abu Dhabi) require provider opt-in for long-distance category and may have extended ETA disclosures.

**Rule 70:** Salik Assist may temporarily suspend service in a zone due to supply shortage, safety advisory, or regulatory directive, with customer notification.

---

## Business Examples

**Example 1 — Rule 21 & 24:** Customer requests battery jump-start. Four providers respond in 3 minutes. Customer sees top 3 offers ranked by composite score (ETA, rating, price). Each shows AED 80–120 estimate and 12–20 min ETA. Customer selects middle option.

**Example 2 — Rule 30 violation:** Provider completes tow and enters AED 350 final price vs. AED 250 upper estimate (40% over). System blocks charge; customer must approve override or dispute opens automatically.

**Rule 43 application:** Customer cancels after provider is 5 minutes away. AED 30 cancellation fee applied; provider receives AED 20 minimum compensation; customer receives credit option for future use per ops discretion.

**Example 4 — Rule 5 suspension:** Provider insurance expires midnight Sunday. Monday 12:01 AM: provider auto-suspended from new offers. One in-progress job from Sunday evening completes normally; payout processes per Rule 47.

---

## Business Decisions

| Decision | Rationale |
|----------|-----------|
| 70 explicit numbered rules | Operations clarity; legal enforceability; investor diligence |
| Top-3 offer rules are non-negotiable (Rules 20–27) | Core marketplace differentiation |
| 18% standard commission (Rule 46) | Market-aligned; sustainable unit economics |
| No cash on platform (Rule 49) | Payment guarantee and audit trail |
| 48-hour payout SLA (Rule 47) | Provider recruitment competitive advantage |
| Non-exclusive providers (Rule 10) | Supply side adoption; reduces churn risk |
| Surge cap at 1.5× (Rule 31) | Customer protection in emergency context |

---

## Risks

| Risk | Impact | Mitigation |
|------|--------|------------|
| Rules too complex for providers to follow | Medium | Provider onboarding playbook; simplified summary card |
| Rule 30 price cap conflicts with variable tow distances | Medium | Zone-based estimate bands; customer approval flow |
| Dispute volume overwhelms ops (Rules 56–60) | High | Hire dispute specialists; clear photo evidence rules |
| B2B contract exceptions fragment rule consistency | Medium | Contract template aligned to base rules |
| Regulatory challenge to independent contractor classification | High | Legal review; Rule 9 prominently in terms |

---

## Assumptions

- 70 rules (numbered 1–70) cover launch marketplace operations comprehensively
- Operations team can enforce manual rules (disputes, verification) at launch scale
- Providers accept 18% commission when rules 47 and 21–27 deliver value
- Customers accept digital-only payment in UAE metro market
- B2B partners accept Rule 63 SLA reporting as sufficient for Year 1

---

## Open Questions

- Should Rule 7 minimum rating be 3.5 or 4.0 for stricter quality?
- Is 15% price overrun cap (Rule 30) sufficient for long-distance tows?
- Should provider nonexistent penalty (Rule 44) increase after repeat offenses?
- Are 70 rules too many for provider terms acceptance UX?
- Which rules require UAE legal review before launch?

---

## Next Steps

1. Legal review of all 70 rules for enforceability under UAE law
2. Publish provider-facing rules summary (1-page) derived from this document
3. Publish customer-facing policy equivalent for app and website
4. Train operations team on dispute rules (56–60) and cancellation rules (41–45)
5. Map rules to [Business Requirements](./Business-Requirements.md) traceability matrix
6. Establish quarterly rule review with change log process
