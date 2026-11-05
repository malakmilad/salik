# Cancellation Policy — Salik Assist

| Field | Value |
|-------|-------|
| **Version** | 1.0 |
| **Status** | Draft |
| **Author** | Product & Strategy Team |
| **Last Updated** | July 4, 2026 |

## Purpose

Define explicit rules, fees, timelines, and exceptions for cancelling roadside assistance jobs on Salik Assist—protecting customers, providers, and platform economics while maintaining fairness in high-stress emergency contexts.

## Scope

Covers customer-initiated, provider-initiated, and platform-initiated cancellations for B2C and B2B jobs in UAE. Excludes subscription product cancellations (Phase 2).

## Related Documents

- [Refund Policy](./Refund-Policy.md)
- [Escalation Policy](./Escalation-Policy.md)
- [SLA](./SLA.md)
- [Operations Workflow](./Operations-Workflow.md)
- [Terms Summary](../07-Legal/Terms-Summary.md)

## Table of Contents

1. [Policy Overview](#policy-overview)
2. [Cancellation Stages & Definitions](#cancellation-stages--definitions)
3. [Customer-Initiated Cancellation Rules](#customer-initiated-cancellation-rules)
4. [Provider-Initiated Cancellation Rules](#provider-initiated-cancellation-rules)
5. [Platform-Initiated Cancellation Rules](#platform-initiated-cancellation-rules)
6. [Cancellation Fee Schedule](#cancellation-fee-schedule)
7. [B2B Cancellation Rules](#b2b-cancellation-rules)
8. [Dispute & Exception Process](#dispute--exception-process)
9. [Provider & Customer Consequences](#provider--customer-consequences)
10. [Business Examples](#business-examples)
11. [Business Decisions](#business-decisions)
12. [Risks](#risks)
13. [Assumptions](#assumptions)
14. [Open Questions](#open-questions)
15. [Next Steps](#next-steps)

---

## Policy Overview

A cancellation occurs when a confirmed job (offer accepted) does not proceed to successful service completion. Cancellation rules depend on **who cancels**, **job stage**, and **reason**.

**Core principles:**
1. Customer never penalized for provider fault
2. Fees reflect provider opportunity cost, not punitive charges
3. Free cancellation window before provider dispatch commitment
4. All fees disclosed before offer acceptance

---

## Cancellation Stages & Definitions

| Stage | Definition | Timestamp Reference |
|-------|------------|---------------------|
| **S0 — Request Open** | Request submitted; no offer accepted | Request creation |
| **S1 — Offer Accepted** | Customer accepted provider offer; provider not yet en route | Acceptance timestamp |
| **S2 — Provider En Route** | Provider marked en route or moving toward customer | En route timestamp |
| **S3 — Provider Arrived** | Provider at customer location | Arrival timestamp |
| **S4 — Service In Progress** | Service actively being performed | Service start timestamp |

Cancellation fees apply based on stage at cancellation moment.

---

## Customer-Initiated Cancellation Rules

| Stage | Fee | Refund of Pre-Auth | Notes |
|-------|-----|-------------------|-------|
| **S0 — Request Open** | AED 0 | N/A (no charge) | Instant; no penalty |
| **S1 — Offer Accepted (<3 min after acceptance)** | AED 0 | Full release | Grace period for buyer's remorse |
| **S1 — Offer Accepted (≥3 min after acceptance)** | AED 25 | N/A | Covers provider mobilization |
| **S2 — Provider En Route (<50% of ETA elapsed)** | AED 40 | N/A | Partial mobilization cost |
| **S2 — Provider En Route (≥50% of ETA elapsed)** | AED 60 | N/A | Provider nearly arrived |
| **S3 — Provider Arrived** | AED 75 | N/A | Provider on-site; call-out fee |
| **S4 — Service In Progress** | Not permitted* | — | *Customer may stop service; charged for work completed |

**Customer free cancellation exceptions (AED 0 at any stage):**
- Provider ETA exceeded by >25 minutes without notification
- Provider no-show (accepted but never en route within 15 minutes)
- Provider requests price increase >20% without prior in-app approval
- Customer safety concern (verified by support)
- Platform/system error caused incorrect booking
- B2B partner authorization revoked mid-job

**Monthly limit:** Customers may receive maximum 3 free exception cancellations per 30 days; further exceptions require supervisor approval.

---

## Provider-Initiated Cancellation Rules

Providers may cancel only for legitimate reasons. Unilateral cancellation after acceptance is heavily penalized.

| Stage | Allowed Reason | Provider Penalty | Customer Compensation |
|-------|----------------|------------------|----------------------|
| **S1 — Before en route** | Vehicle breakdown; emergency; incorrect service match | Warning (1st); SPS −10 (2nd in 90 days) | Auto re-dispatch; AED 0 customer fee |
| **S2 — En route** | Vehicle breakdown; accident; safety emergency | SPS −15; offer limit 10/week for 7 days | Auto re-dispatch; AED 30 credit |
| **S3 — Arrived** | Issue not as described (wrong category); safety hazard at location | Case-by-case review | Re-dispatch or cancel free; provider may receive partial call-out fee if legitimate mismatch |
| **S3 — Arrived** | Provider refuses without valid reason | SPS −25; suspension 7 days | Full cancel free + AED 50 credit |
| **Any stage** | Provider no-show (no cancellation, no arrival) | Suspension 7 days (1st); 30 days (2nd) | Re-dispatch + AED 50 credit |

**Valid provider cancellation reasons (documentation required):**
- Service vehicle mechanical failure (photo evidence)
- Customer location inaccessible or unsafe (photo + support verification)
- Issue category mismatch (customer requested tow; issue is battery — re-match, not cancel)
- Customer unreachable after 15 minutes on-site (3 call attempts logged)

**Invalid reasons (penalty applies):**
- Found closer/higher-paying job
- Customer location too far (accepted offer knowing distance)
- Traffic delay (should update ETA, not cancel)
- Personal convenience

---

## Platform-Initiated Cancellation Rules

Salik Assist may cancel jobs in these scenarios:

| Scenario | Stage | Customer Impact | Provider Impact |
|----------|-------|-----------------|-----------------|
| No provider available after 15 min | S0 | Free; AED 50 credit offered | N/A |
| Provider suspended mid-job | S1–S3 | Free; auto re-dispatch | Job reassigned; suspension proceeds |
| Fraud detection (either party) | Any | Free; account review | Suspension pending investigation |
| Force majeure (severe weather, road closure) | Any | Free | Partial call-out fee at platform discretion |
| Duplicate request detected | S0–S1 | Free; merge or cancel duplicate | N/A |
| Payment pre-authorization failure | S1 | Cancel; prompt to update payment | Provider released |

---

## Cancellation Fee Schedule

| Fee Tier | Amount (AED) | Recipient Split |
|----------|--------------|-----------------|
| S1 late cancel (≥3 min) | 25 | Provider AED 20 / Platform AED 5 |
| S2 early en route (<50% ETA) | 40 | Provider AED 32 / Platform AED 8 |
| S2 late en route (≥50% ETA) | 60 | Provider AED 48 / Platform AED 12 |
| S3 arrived call-out | 75 | Provider AED 60 / Platform AED 15 |

**Fee caps:**
- Cancellation fee never exceeds 30% of quoted job estimate
- Minimum cancellation fee: AED 25 (when applicable)
- B2B jobs: fees per partner contract (typically platform absorbs)

**Fee waiver authority:**
- Support agent: Waive fees for defined exception triggers
- Supervisor: Discretionary waiver ≤2 per customer per 90 days
- Ops manager: Any waiver with documented reason

---

## B2B Cancellation Rules

| Partner Type | Customer Fee | Billing Impact | SLA Credit |
|--------------|--------------|----------------|------------|
| **Insurance (covered event)** | AED 0 | No charge to customer or partner if cancelled before S3 | N/A if provider fault; partner credited if platform fault |
| **Insurance (non-covered cancel)** | Per B2C rules | Customer billed if applicable | N/A |
| **Fleet** | AED 0 (fleet policy) | Fleet billed call-out fee if S3 reached | SLA miss if platform/provider fault |
| **Concierge** | AED 0 | Third party billed per contract | Per contract |

B2B partners may negotiate custom cancellation terms in master service agreement.

---

## Dispute & Exception Process

**Customer disputes cancellation fee:**
1. Contact support within 48 hours of cancellation
2. Agent reviews job timeline and reason code
3. If exception trigger met: full fee refund within 24 hours
4. If disputed without valid exception: supervisor review within 48 hours
5. Final decision communicated; appeal to ops manager within 7 days

**Provider disputes cancellation penalty:**
1. Submit dispute via provider app within 48 hours
2. Provide evidence (photos, call logs, support ticket reference)
3. Ops manager review within 72 hours
4. Penalty upheld, reduced, or reversed with documented reasoning

---

## Provider & Customer Consequences

### Customer Abuse Patterns

| Pattern | Threshold | Action |
|---------|-----------|--------|
| Excessive cancellations | >5 cancellations in 30 days (non-exception) | Warning email |
| Repeat accept-and-cancel | >3 accept-and-cancel (S1 <3 min) in 7 days | 24-hour request cooldown |
| Fee dispute abuse | >3 rejected fee disputes in 90 days | Disputes require supervisor pre-approval |
| Fraud (false exception claims) | Any confirmed | Account suspension |

### Provider Abuse Patterns

| Pattern | Threshold | Action |
|---------|-----------|--------|
| High cancellation rate | >10% provider-initiated in 30 days | Performance review |
| Post-acceptance cancel pattern | >3 cancels after S1 in 30 days | Offer limit 5/week |
| No-show pattern | 2 no-shows in 90 days | Suspension 30 days |
| No-show pattern | 3 no-shows in 90 days | Permanent removal |

---

## Business Examples

**Example 1 — Customer grace cancel:** Customer accepts battery jump offer, realizes friend is arriving with cables 2 minutes later. Cancels at S1 within grace period. Fee: AED 0. Provider notified; no penalty.

**Example 2 — Customer late cancel en route:** Customer accepts tow (AED 250 estimate). 8 minutes later, traffic clears and car restarts. Cancels at S2 with 60% ETA elapsed. Fee: AED 60 (Provider AED 48 / Platform AED 12).

**Example 3 — Provider fault free cancel:** Provider accepted job but goes offline. 18 minutes pass, no en route update. Customer calls support. Platform cancels (provider no-show). Customer fee: AED 0 + AED 50 credit. Provider suspended 7 days.

**Example 4 — B2B insurance job:** Policyholder accepts tow. Provider en route. Insurer confirms coverage applies. Provider arrives; insurer pre-authorizes. Customer decides garage is wrong location. Cancels at S3. Per insurance contract: AED 0 to customer; AED 75 call-out split between insurer and platform per rate card.

---

## Business Decisions

| Decision | Rationale |
|----------|-----------|
| 3-minute grace period after acceptance | Emergency context causes quick reconsideration; zero fee prevents resentment |
| Escalating fee by stage | Aligns with provider opportunity cost; industry-standard call-out structure |
| 30% fee cap relative to estimate | Prevents disproportionate fees on low-value jobs |
| Provider receives 80% of cancellation fee | Incentivizes providers to accept knowing partial compensation on cancel |
| Auto re-dispatch on provider cancel | Customer experience priority; don't leave stranded customer |
| Free cancel on 25+ min ETA breach | Platform accountability for SLA failures |

---

## Risks

| Risk | Impact | Mitigation |
|------|--------|------------|
| Customer backlash on cancellation fees | High | Clear disclosure pre-acceptance; generous exception triggers |
| Provider cancels to avoid difficult jobs | Medium | Penalty structure; performance tracking; offer limits |
| Fee disputes increase support load | Medium | Automated fee calculation; clear stage timestamps |
| B2B contract divergence complexity | Medium | Standard B2C rules as default; documented partner exceptions |
| Gaming via accept-and-cancel grace period | Low | Cooldown after 3 rapid cancels in 7 days |

---

## Assumptions

- 8% of accepted jobs will be cancelled before completion
- 70% of cancellations occur at S0–S1 (low or no fee)
- Provider-initiated cancellations will be <3% of accepted jobs
- AED 25–75 fee range is acceptable to UAE customers if disclosed upfront
- Automated stage timestamping is accurate and dispute-resistant

---

## Open Questions

- Allow customer to cancel S4 (in progress) with partial charge for work done?
- Dynamic cancellation fees during surge pricing periods?
- Subscription members (Phase 2) receive reduced or zero cancellation fees?
- Provider cancellation insurance / contingency fund for vehicle breakdown?

---

## Next Steps

1. Display cancellation fee schedule in offer acceptance flow
2. Implement automated fee calculation by stage timestamp
3. Train support team on exception triggers and waiver authority
4. Include cancellation terms in [Terms Summary](../07-Legal/Terms-Summary.md)
5. Monitor cancellation rate and fee dispute rate weekly post-launch
