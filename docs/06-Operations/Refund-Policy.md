# Refund Policy — Salik Assist

| Field | Value |
|-------|-------|
| **Version** | 1.0 |
| **Status** | Draft |
| **Author** | Product & Strategy Team |
| **Last Updated** | July 4, 2026 |

## Purpose

Define explicit refund eligibility criteria, amounts, processing timelines, and authority levels for Salik Assist—ensuring fair resolution of customer payment disputes while protecting providers and platform from abuse.

## Scope

Covers full and partial refunds for B2C consumer jobs in UAE. B2B/insurance billing adjustments follow partner contracts with reference to analogous principles. Excludes provider payout disputes (separate provider finance process).

## Related Documents

- [Cancellation Policy](./Cancellation-Policy.md)
- [Escalation Policy](./Escalation-Policy.md)
- [Customer Support](./Customer-Support.md)
- [Quality Control](./Quality-Control.md)
- [Terms Summary](../07-Legal/Terms-Summary.md)

## Table of Contents

1. [Policy Overview](#policy-overview)
2. [Refund Eligibility Matrix](#refund-eligibility-matrix)
3. [Full Refund Triggers](#full-refund-triggers)
4. [Partial Refund Triggers](#partial-refund-triggers)
5. [Non-Refundable Scenarios](#non-refundable-scenarios)
6. [Refund Amount Calculation](#refund-amount-calculation)
7. [Processing Timelines & Methods](#processing-timelines--methods)
8. [Refund Authority Levels](#refund-authority-levels)
9. [Provider Impact & Chargebacks](#provider-impact--chargebacks)
10. [Dispute Resolution Process](#dispute-resolution-process)
11. [Business Examples](#business-examples)
12. [Business Decisions](#business-decisions)
13. [Risks](#risks)
14. [Assumptions](#assumptions)
15. [Open Questions](#open-questions)
16. [Next Steps](#next-steps)

---

## Policy Overview

Salik Assist processes refunds when service delivery fails to meet agreed standards, platform or provider fault is established, or cancellation rules mandate return of fees. Refunds are not automatic goodwill—they require eligibility verification.

**Core principles:**
1. Customer receives refund when platform or provider failed to deliver promised service
2. Partial refunds reflect proportional service failure, not arbitrary discounts
3. Refund requests must be submitted within **48 hours** of job completion (72 hours for B2B)
4. Service credits may be offered as alternative where appropriate (customer choice)

---

## Refund Eligibility Matrix

| Scenario | Refund Type | Amount | Auto-Approved |
|----------|-------------|--------|---------------|
| Provider no-show | Full | 100% of charge + cancellation fee if paid | Yes |
| Service not performed | Full | 100% of charge | Yes (with verification) |
| SLA breach (ETA >45 min past commitment) | Partial or full | 25–100% per matrix below | Partial auto at 25% |
| Price overcharge without consent | Partial or full | Overcharge amount + 10% goodwill | Supervisor approval |
| Quality failure (verified) | Partial | 25–75% per quality matrix | No |
| Duplicate charge | Full | 100% of duplicate | Yes |
| Platform system error | Full | 100% of charge | Yes |
| Customer changed mind (service completed) | None | — | — |
| Customer-provided incorrect info causing failure | None | — | — |
| Cancellation fee dispute (valid exception) | Full fee refund | 100% of cancellation fee | Agent approval |

---

## Full Refund Triggers

Automatic full refund (100% of job charge) when ANY of the following are confirmed:

| # | Trigger | Verification |
|---|---------|--------------|
| 1 | Provider no-show after acceptance | GPS/timestamp + support confirmation |
| 2 | Service marked complete but not performed | Customer evidence + provider no response or admission |
| 3 | Wrong service category delivered without customer consent | Job record review |
| 4 | Duplicate charge on same job | Payment system match |
| 5 | Platform error (wrong amount, wrong customer charged) | Finance audit |
| 6 | Provider permanently removed for fraud on this job | Quality investigation |
| 7 | Safety incident caused by provider | Tier 3 investigation |
| 8 | Customer cancelled under free-cancel exception per [Cancellation Policy](./Cancellation-Policy.md) | Timeline review |

**Processing:** Auto-initiated within 24 hours of trigger confirmation. Customer notified via app + email.

---

## Partial Refund Triggers

| Trigger | Refund % | Conditions |
|---------|----------|------------|
| ETA exceeded 30–45 min past commitment | 25% | Service eventually completed; no safety issue |
| ETA exceeded >45 min past commitment | 50% | Service eventually completed |
| Service partially completed (e.g., jump-start failed; tow not needed) | 25–50% | Assessed by support based on effort/expense incurred |
| Quality complaint — minor (verified) | 25% | e.g., rude behavior, minor delay, incomplete cleanup |
| Quality complaint — moderate (verified) | 50% | e.g., damage to minor vehicle component, wrong part installed then corrected |
| Quality complaint — severe (verified) | 75% | e.g., significant damage, service made issue worse |
| Price overcharge 10–20% without in-app approval | Overcharge amount only | Provider at fault |
| Price overcharge >20% without in-app approval | Overcharge + 10% goodwill | Provider at fault; quality review triggered |
| Provider arrived but customer cancelled (platform fault re-dispatch failed) | 100% of any charge | Platform error |

**Quality refund % determined by:** Quality team adjudication using evidence from both parties. Default to 50% if evidence inconclusive and complaint is credible.

---

## Non-Refundable Scenarios

| Scenario | Reason | Alternative |
|----------|--------|-------------|
| Service completed satisfactorily; customer changed mind | No fault | None |
| Customer provided wrong location | Customer fault | Re-dispatch at customer cost |
| Customer provided wrong vehicle/issue description causing mismatch | Customer fault | Partial charge for provider call-out per cancellation policy |
| Issue resolved before provider arrival (customer S2 cancel) | Customer-initiated | Cancellation fee applies; no job charge refund |
| Customer absent on-site after provider arrival (15+ min, 3 call attempts) | Customer fault | Call-out fee charged; no refund |
| Normal wear/tear unrelated to service | Not provider caused | None |
| Refund request after 48-hour window | Policy limit | Case-by-case supervisor review up to 7 days |
| Chargeback filed before support contact | Process bypass | Chargeback dispute process; account review |

---

## Refund Amount Calculation

**Standard formula:**

```
Refund Amount = (Eligible Percentage × Job Charge) + Applicable Fee Returns − Prior Credits Applied
```

**Examples:**
- Job charge AED 280; full refund trigger → AED 280
- Job charge AED 280; 50% partial (ETA breach) → AED 140
- Job charge AED 280; overcharge AED 50 without consent → AED 50 + AED 5 goodwill = AED 55
- Cancellation fee AED 60 paid; valid exception → AED 60 fee return

**Caps and floors:**
- Minimum refund processed: AED 10 (smaller amounts issued as service credit)
- Maximum auto-refund (Tier 1 agent): AED 300
- Refund never exceeds total amount charged on job

**Service credit alternative:**
- Customer may choose 120% of refund amount as service credit (e.g., AED 100 refund → AED 120 credit)
- Credit expires 90 days from issuance
- Credit non-transferable

---

## Processing Timelines & Methods

| Refund Type | Initiation | Customer Receipt | Method |
|-------------|------------|------------------|--------|
| Auto-approved full refund | ≤24 hours | 3–5 business days | Original payment method |
| Agent-approved (≤AED 300) | Same interaction | 3–5 business days | Original payment method |
| Supervisor-approved (AED 301–1,000) | ≤24 hours | 5–7 business days | Original payment method |
| Manager-approved (>AED 1,000) | ≤48 hours | 5–10 business days | Original payment method or bank transfer |
| Service credit | Immediate | Immediate (in-app) | Platform credit balance |

**Provider payout impact:**
- Full refund for provider fault: Provider receives AED 0 for job; may face performance penalty
- Partial refund: Provider payout reduced proportionally (provider receives net minus refund)
- Platform fault refund: Provider paid full amount; platform absorbs refund cost

---

## Refund Authority Levels

| Amount (AED) | Approver | Documentation Required |
|--------------|----------|------------------------|
| ≤300 | Tier 1 support agent | Reason code + job timeline |
| 301–1,000 | Support supervisor | Reason code + evidence summary |
| 1,001–5,000 | Ops manager | Investigation report |
| >5,000 | GM + Finance | Full RCA + legal review if applicable |

**Monthly refund budget:** Ops manager monitors total refund volume. If refunds exceed 3% of GMV in any month, root cause review mandatory.

---

## Provider Impact & Chargebacks

### Provider Financial Impact

| Refund Reason | Provider Payout | Performance Impact |
|---------------|-----------------|-------------------|
| Provider no-show | AED 0 | Suspension + SPS penalty |
| Quality failure (verified) | Reduced by refund amount | SPS −10 to −25 |
| Price overcharge | Reduced by overcharge + platform may absorb goodwill | Warning to suspension |
| Platform/SLA issue | Full payout maintained | None |
| Customer fault (no refund) | Full payout | None |

### Customer Chargeback Handling

1. Customer files chargeback with bank before contacting Salik Assist
2. Finance team receives notification within 24 hours
3. Evidence package submitted to payment processor within 48 hours (job record, GPS, photos, communication)
4. If chargeback upheld AND Salik investigation finds provider/platform not at fault: customer account suspended
5. If chargeback upheld AND fault confirmed: refund processed; provider adjusted; chargeback accepted

**Chargeback target:** <0.5% of transactions

---

## Dispute Resolution Process

```
Customer Request → Eligibility Check → Evidence Collection → Decision → Processing → Closure
```

| Step | Timeline | Owner |
|------|----------|-------|
| 1. Customer submits refund request | Within 48 hr of job | Customer |
| 2. Initial eligibility check | ≤4 hours | Tier 1 agent |
| 3. Provider statement request (if needed) | Provider has 24 hr to respond | Support |
| 4. Quality adjudication (if needed) | ≤72 hours from request | Quality team |
| 5. Decision communicated | ≤72 hours total (≤24 for auto) | Support |
| 6. Refund processed | Per timeline above | Finance |
| 7. Appeal window | 7 days from decision | Customer |
| 8. Appeal review | ≤5 business days | Ops manager |

**Stalemate rule:** If evidence inconclusive after provider and customer statements, default to 25% partial refund as goodwill (once per customer per 90 days).

---

## Business Examples

**Example 1 — Full refund (no-show):** Customer charged AED 250 pre-authorization for tow. Provider never arrives. Support confirms no-show at 35 minutes. Full refund AED 250 auto-processed. Customer also receives AED 50 service credit. Provider suspended.

**Example 2 — Partial refund (ETA breach):** Battery jump completed successfully but provider arrived 52 minutes past committed ETA. Customer requests refund. Auto-eligible for 50% partial. AED 90 refunded on AED 180 job. Provider receives AED 90 payout minus commission.

**Example 3 — Price overcharge:** Customer agreed to AED 200 tow estimate. Provider charged AED 290 without in-app approval. Customer disputes within 24 hours. Supervisor approves AED 90 overcharge refund + AED 9 goodwill = AED 99. Provider warned; second offense triggers suspension.

**Example 4 — Non-refundable:** Customer requests refund because tire was changed but they later found a cheaper garage. Service completed satisfactorily with 4-star rating. Refund denied. Customer offered AED 20 credit as retention gesture (supervisor discretion).

**Example 5 — Service credit choice:** Customer eligible for AED 100 partial refund. Chooses 120% service credit = AED 120 platform credit. Uses AED 120 on next job within 60 days.

---

## Business Decisions

| Decision | Rationale |
|----------|-----------|
| 48-hour refund request window | Balances customer protection with operational certainty |
| Auto-refund on confirmed no-show | Highest-trust signal; removes support friction |
| 120% service credit option | Retains customer at lower cash cost than refund |
| Provider payout reduced on fault refunds | Aligns provider incentives with quality |
| 25% default for inconclusive disputes | Goodwill gesture prevents escalation without admitting fault |
| 3% monthly GMV refund cap trigger for review | Early warning on systemic quality or policy issues |

---

## Risks

| Risk | Impact | Mitigation |
|------|--------|------------|
| Refund abuse by customers | Medium | Pattern detection; account suspension; 48-hour window |
| Excessive refunds erode provider trust | Medium | Only provider-fault refunds reduce provider payout |
| Slow refund processing damages brand | High | Auto-refund triggers; clear timelines |
| Chargeback rate increase | High | Proactive support; evidence packages; pre-dispute outreach |
| Inconsistent refund decisions | Medium | Eligibility matrix; authority levels; QA audits |

---

## Assumptions

- 2.5% of completed jobs will generate a refund request
- 60% of refund requests will be auto-approved or resolved at Tier 1
- Average refund amount: AED 85 (blended full and partial)
- 15% of eligible customers will choose service credit over cash refund
- 3–5 business day bank refund processing is acceptable to UAE customers

---

## Open Questions

- Extend refund window to 7 days for B2C (industry comparison)?
- Proactive partial refund (auto 25%) on SLA breach without customer request?
- Refund insurance or guarantee fund marketed to customers as trust signal?
- Partial refund tiers for subscription members (Phase 2)?

---

## Next Steps

1. Integrate refund eligibility checks into support CRM decision trees
2. Configure auto-refund triggers for no-show and duplicate charge
3. Train support team on matrix, authority levels, and service credit option
4. Establish monthly refund reporting dashboard for finance and ops
5. Include refund policy summary in customer terms and in-app help center
