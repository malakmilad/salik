# Escalation Policy — Salik Assist

| Field | Value |
|-------|-------|
| **Version** | 1.0 |
| **Status** | Draft |
| **Author** | Product & Strategy Team |
| **Last Updated** | July 4, 2026 |

## Purpose

Define explicit escalation triggers, tiers, response times, ownership, and resolution standards for situations that exceed normal support and operations workflows—ensuring customer safety, marketplace integrity, and timely executive visibility on critical incidents.

## Scope

Covers operational, customer, provider, B2B, legal, and media escalations for Salik Assist UAE operations. Excludes IT/security incident response.

## Related Documents

- [Customer Support](./Customer-Support.md)
- [SLA](./SLA.md)
- [Cancellation Policy](./Cancellation-Policy.md)
- [Refund Policy](./Refund-Policy.md)
- [Quality Control](./Quality-Control.md)
- [Compliance](../07-Legal/Compliance.md)

## Table of Contents

1. [Escalation Framework](#escalation-framework)
2. [Escalation Tiers](#escalation-tiers)
3. [Tier 1 — Operational Escalations](#tier-1--operational-escalations)
4. [Tier 2 — Customer & Dispute Escalations](#tier-2--customer--dispute-escalations)
5. [Tier 3 — Critical & Safety Escalations](#tier-3--critical--safety-escalations)
6. [Tier 4 — Executive & External Escalations](#tier-4--executive--external-escalations)
7. [Escalation Response Matrix](#escalation-response-matrix)
8. [Communication Protocols](#communication-protocols)
9. [Post-Escalation Review](#post-escalation-review)
10. [Business Examples](#business-examples)
11. [Business Decisions](#business-decisions)
12. [Risks](#risks)
13. [Assumptions](#assumptions)
14. [Open Questions](#open-questions)
15. [Next Steps](#next-steps)

---

## Escalation Framework

Every escalation is classified by **severity (P1–P4)**, assigned an **owner**, and tracked to **resolution** with documented outcome.

| Severity | Definition | Max Response Time | Max Resolution Time |
|----------|------------|-------------------|---------------------|
| **P1 — Critical** | Safety risk, legal threat, media exposure, platform outage affecting active jobs | 5 minutes | 4 hours |
| **P2 — High** | SLA breach on active job, B2B partner complaint, fraud allegation | 15 minutes | 24 hours |
| **P3 — Medium** | Post-job dispute >AED 1,000, repeat provider violation, customer social media complaint | 1 hour | 72 hours |
| **P4 — Low** | Process improvement, minor policy exception, non-urgent B2B billing | 4 hours | 5 business days |

---

## Escalation Tiers

```
Tier 1: Support Agent / Ops Coordinator
    ↓ (triggers met)
Tier 2: Support Supervisor / Ops Manager
    ↓ (triggers met)
Tier 3: Head of Operations / Head of Quality
    ↓ (triggers met)
Tier 4: GM / CEO / Legal Counsel
```

**Rule:** Escalations skip tiers when severity warrants (e.g., P1 safety goes directly to Tier 3/4).

---

## Tier 1 — Operational Escalations

**Owner:** Support agent or ops coordinator  
**Auto-triggered system alerts included**

| Trigger | Threshold | Automatic Action | Escalate to Tier 2 If |
|---------|-----------|------------------|----------------------|
| Zero provider offers | 5 minutes after request | Expand radius; notify backup pool | No offer by 8 minutes |
| Provider no response after acceptance | 10 minutes | Contact provider; notify customer | Unresponsive 15 minutes |
| Provider ETA exceeded | 15 minutes past committed ETA | Contact provider; offer customer re-dispatch | 25 minutes past ETA |
| Provider stationary en route | 5 minutes without movement | Contact provider | 10 minutes stationary |
| Customer cancellation during active job | Any | Process per cancellation policy | Dispute over fee |
| Matching queue backlog | >10 unassigned requests in zone | Alert ops coordinator | >20 requests or >15 min oldest |

**Tier 1 authority:**
- Re-dispatch provider
- Waive cancellation fee (customer-initiated, provider fault)
- Issue service credit ≤AED 100
- Contact provider for status update

---

## Tier 2 — Customer & Dispute Escalations

**Owner:** Support supervisor or ops manager

| Trigger | Threshold | Required Action | Escalate to Tier 3 If |
|---------|-----------|-----------------|----------------------|
| Refund request | >AED 300 | Supervisor review and decision within 24 hr | >AED 1,000 or fraud suspected |
| Active job safety concern | Customer reports feeling unsafe | Supervisor joins call; document location | Any confirmed safety threat |
| Provider no-show (confirmed) | Provider accepted but never arrived | Re-dispatch; provider suspension initiation | Customer injury or stranded >60 min |
| Pricing dispute on-site | Price increase >20% without in-app approval | Halt service; mediate | Provider refuses to comply |
| B2B partner dispatch failure | SLA miss on partner job | Account manager notified; manual dispatch | 2nd failure same partner in 7 days |
| Repeat customer complaint | Same customer 3+ complaints in 30 days | Root cause analysis | Pattern indicates systemic issue |
| Provider performance breach | 2nd no-show or rating <3.0 in 30 days | Performance review initiation | Safety or fraud element |

**Tier 2 authority:**
- Refund up to AED 1,000
- Service credit up to AED 300
- Temporary provider suspension (≤7 days)
- Override cancellation fees
- Authorize manual dispatch with surge pricing waived

---

## Tier 3 — Critical & Safety Escalations

**Owner:** Head of Operations + Head of Quality (joint)

| Trigger | Threshold | Required Action | Escalate to Tier 4 If |
|---------|-----------|-----------------|----------------------|
| Physical injury | Any injury during job | Immediate provider suspension; incident report; insurance notification | Hospitalization or third-party injury |
| Assault or harassment | Confirmed by either party | Provider suspension; police report guidance; victim support | Criminal investigation |
| Vehicle damage dispute | Claim >AED 5,000 | Quality investigation; insurance coordination | Legal threat or no insurance |
| Fraud — provider | Documented overcharge, fake completion, identity fraud | Permanent removal review; refund all affected customers | Criminal fraud |
| Fraud — customer | Chargeback abuse, false claims pattern | Account suspension; finance review | >AED 10,000 exposure |
| Data/privacy complaint | Customer alleges data misuse | Privacy review within 24 hr | Regulatory inquiry |
| Regulatory inquiry | Any government or RTA contact | Legal counsel engaged | Formal investigation opened |

**Tier 3 authority:**
- Refund any amount (with finance notification)
- Permanent provider removal recommendation
- Customer account suspension
- Engage legal counsel (preliminary)
- Public statement draft (requires Tier 4 approval)

---

## Tier 4 — Executive & External Escalations

**Owner:** GM / CEO + Legal Counsel

| Trigger | Threshold | Required Action |
|---------|-----------|-----------------|
| Fatality or serious injury | Any | CEO notified immediately; legal counsel; insurance carrier; regulatory notification per legal advice |
| Media inquiry | Any journalist or major social media (>10K followers) | CEO or designated spokesperson only; legal review of response |
| Lawsuit or legal threat | Written legal notice | Legal counsel owns response; preserve all records |
| B2B contract termination threat | Partner representing >5% volume | CEO + Partnerships director joint call within 24 hr |
| Platform-wide failure | >50% jobs affected >30 minutes | CEO war room; customer communication; partner notification |
| Government investigation | Formal notice | Legal counsel primary; executive brief within 2 hours |

**Tier 4 authority:** Unlimited refund authority, external communications, legal settlement up to pre-approved limits, regulatory cooperation.

---

## Escalation Response Matrix

| Scenario | Severity | Tier | Response Time | Resolution Time | Customer Compensation |
|----------|----------|------|---------------|-----------------|----------------------|
| Provider 20 min late | P3 | 1 | 15 min | 30 min | AED 30 credit (optional) |
| Provider 30+ min late | P2 | 2 | 5 min | 15 min | Free re-dispatch or cancel + AED 50 credit |
| Provider no-show | P2 | 2 | 5 min | 30 min | Full refund + AED 50 credit |
| Zero offers 8+ min | P2 | 2 | Immediate | 15 min | AED 50 credit if customer cancels |
| On-site price dispute | P3 | 2 | 10 min | 30 min | Cancel without fee; mediate |
| Customer feels unsafe | P1 | 3 | 5 min | 1 hr | Re-dispatch priority + AED 100 credit |
| Vehicle damage >AED 5K | P2 | 3 | 15 min | 72 hr | Case-by-case refund/insurance |
| Injury during service | P1 | 4 | Immediate | Ongoing | Support + insurance process |
| B2B SLA miss (1st) | P3 | 2 | 30 min | 4 hr | Partner SLA credit per contract |
| B2B SLA miss (3rd in 7 days) | P2 | 3 | 15 min | 24 hr | Executive partner call |
| Social media complaint (>1K engagement) | P3 | 3 | 1 hr | 24 hr | Public response + private resolution |

---

## Communication Protocols

### Internal Escalation Notification

| Severity | Notification Method | Recipients |
|----------|---------------------|------------|
| P1 | Phone call + Slack alert | On-call supervisor → Head of Ops → GM |
| P2 | Slack alert + ticket flag | Supervisor + Ops manager |
| P3 | Ticket flag + email | Assigned owner + supervisor |
| P4 | Ticket queue | Assigned owner |

### Customer Communication During Escalation

| Stage | Customer Update Frequency |
|-------|--------------------------|
| Active job (P1/P2) | Every 5 minutes until resolved |
| Active job (P3) | Every 15 minutes |
| Post-job dispute | Initial ack ≤1 hr; update every 24 hr until resolved |
| Safety (P1) | Continuous contact until safe resolution |

### Provider Communication During Escalation

- Provider notified of complaint within 2 hours (P2/P3) or immediately (P1)
- Provider statement collected within 24 hours for disputes
- Suspension effective immediately upon P1 safety trigger; provider notified via app + SMS

---

## Post-Escalation Review

| Severity | Review Required | Timeline | Output |
|----------|---------------|----------|--------|
| P1 | Mandatory root cause analysis (RCA) | Within 48 hours | RCA document + action items |
| P2 | Supervisor review | Within 72 hours | Ticket closure notes + process fix if needed |
| P3 | Standard closure | Within 5 days | Ticket closed with resolution code |
| P4 | Optional | As needed | Process improvement backlog item |

**Monthly escalation report** to leadership: volume by tier, resolution time compliance, top trigger categories, repeat offenders, compensation cost.

---

## Business Examples

**Example 1 — Tier 1 to Tier 2 (no-show):** Customer accepts tow offer. Provider goes stationary 8 minutes after acceptance, then unresponsive. Tier 1 contacts provider — no answer at 10 min. At 15 min, escalates to Tier 2. Supervisor re-dispatches backup provider. Original provider suspended 7 days. Customer receives AED 50 credit.

**Example 2 — Tier 3 (safety):** Female customer reports provider made her uncomfortable during lockout service. Tier 1 escalates immediately to Tier 3 (P1). Provider suspended pending investigation. Quality team interviews both parties within 12 hours. Provider permanently removed; customer refunded and offered AED 100 credit.

**Example 3 — Tier 4 (media):** Influencer posts video claiming Salik Assist overcharged during desert recovery (AED 2,500 vs. estimate AED 800). Engagement exceeds 50K views. Tier 4 engaged. Legal reviews; investigation finds provider failed to obtain in-app price approval. Full refund issued publicly in response; provider removed. CEO statement within 6 hours.

---

## Business Decisions

| Decision | Rationale |
|----------|-----------|
| P1 safety escalations skip to Tier 3 | Speed over hierarchy when customer safety at risk |
| Automatic system triggers at defined minute thresholds | Removes human judgment delay for common failure modes |
| AED 50 standard credit for no-show/zero-offer | Consistent, predictable customer compensation |
| Provider suspension immediate on P1 | Protects other customers while investigation proceeds |
| Monthly escalation report to leadership | Pattern detection prevents repeat systemic failures |
| Tier 1 agents cannot resolve refunds >AED 300 | Balances empowerment with financial control |

---

## Risks

| Risk | Impact | Mitigation |
|------|--------|------------|
| Escalation fatigue (too many auto-triggers) | Medium | Tune thresholds after 90 days of launch data |
| Under-escalation by frontline agents | High | Mandatory escalation triggers; QA audits |
| Slow Tier 3/4 response off-hours | High | On-call roster for P1/P2; clear wake-up protocol |
| Compensation costs from generous credits | Medium | Track escalation cost per job; cap repeat credits per customer |
| Provider disputes escalation fairness | Medium | Documented appeal process; transparent criteria |

---

## Assumptions

- 5% of jobs will trigger at least Tier 1 escalation
- 0.5% of jobs will reach Tier 2 or above
- P1 events will occur <0.1% of jobs (approximately 1 per 1,000 jobs)
- On-call supervisor available 24/7 from launch
- Automated system alerts reduce Tier 1 response time by 50% vs. manual detection

---

## Open Questions

- Customer-initiated escalation button in app (vs. support contact only)?
- Escalation SLA credits automatically applied or agent-discretion?
- Third-party ombudsman for unresolved disputes (Phase 2)?
- Escalation data shared with B2B partners in real time?

---

## Next Steps

1. Configure automated escalation alerts at defined thresholds
2. Publish on-call roster for P1/P2 coverage
3. Train all support and ops staff on tier triggers and authority limits
4. Create escalation ticket templates with required fields
5. Conduct escalation drill before launch (simulate P1 safety and P2 no-show)
