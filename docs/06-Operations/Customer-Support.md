# Customer Support — Salik Assist

| Field | Value |
|-------|-------|
| **Version** | 1.0 |
| **Status** | Draft |
| **Author** | Product & Strategy Team |
| **Last Updated** | July 4, 2026 |

## Purpose

Define the customer support operating model for Salik Assist—including channels, staffing, response standards, issue categories, and resolution authority—for motorists and B2B users during and after roadside assistance jobs.

## Scope

Covers B2C and B2B customer support operations for UAE launch. Excludes provider support (handled by separate provider success team) and technical incident response.

## Related Documents

- [Escalation Policy](./Escalation-Policy.md)
- [Cancellation Policy](./Cancellation-Policy.md)
- [Refund Policy](./Refund-Policy.md)
- [SLA](./SLA.md)
- [Operations Workflow](./Operations-Workflow.md)
- [Quality Control](./Quality-Control.md)

## Table of Contents

1. [Support Philosophy](#support-philosophy)
2. [Support Channels](#support-channels)
3. [Support Hours & Coverage](#support-hours--coverage)
4. [Issue Categories & Routing](#issue-categories--routing)
5. [Response Time Standards](#response-time-standards)
6. [Support Agent Authority Matrix](#support-agent-authority-matrix)
7. [In-Job vs. Post-Job Support](#in-job-vs-post-job-support)
8. [B2B Support Model](#b2b-support-model)
9. [Support Quality & Training](#support-quality--training)
10. [Business Examples](#business-examples)
11. [Business Decisions](#business-decisions)
12. [Risks](#risks)
13. [Assumptions](#assumptions)
14. [Open Questions](#open-questions)
15. [Next Steps](#next-steps)

---

## Support Philosophy

Roadside assistance customers contact support when stressed, stranded, or frustrated. Salik Assist support prioritizes:

1. **Speed** — Live job issues answered within 60 seconds
2. **Empowerment** — Agents can refund, re-dispatch, and cancel without manager approval (within limits)
3. **Single contact** — Customer never re-explains issue across handoffs
4. **Proactive outreach** — Support initiates contact when SLA breach detected

**Tone:** Calm, empathetic, action-oriented. Arabic and English fluency required for all customer-facing agents.

---

## Support Channels

| Channel | Use Case | Priority |
|---------|----------|----------|
| **In-app live chat** | Active job issues; post-job disputes | Primary |
| **Phone hotline** | Emergency; customers unable to use app | Primary (active jobs) |
| **WhatsApp Business** | Follow-up; document sharing; Arabic preference | Secondary |
| **Email** | Receipts; non-urgent disputes; B2B billing | Tertiary |
| **In-app help center** | Self-service FAQs; cancellation; refund status | Self-service |

**Active job rule:** Phone and live chat must be accessible within 2 taps from tracking screen.

---

## Support Hours & Coverage

| Period | Coverage | Staffing (Launch) |
|--------|----------|-------------------|
| **Peak (6 AM – 11 PM GST)** | Full channels | 4 agents + 1 supervisor |
| **Off-peak (11 PM – 6 AM GST)** | Phone + chat (on-call) | 1 agent + supervisor on-call |
| **Public holidays** | Reduced; phone + chat maintained | 2 agents |
| **Ramadan adjusted** | Extended evening coverage | +1 agent 6 PM – 2 AM |

**Scale target (Year 1):** 8 agents + 2 supervisors for 24/7 full coverage.

---

## Issue Categories & Routing

| Category | Code | Description | Route To |
|----------|------|-------------|----------|
| **Active job — delay** | AJ-DEL | Provider late; no update | Tier 1 agent (immediate) |
| **Active job — no provider** | AJ-NOP | Zero offers or provider no-show | Tier 1 + Ops dispatch |
| **Active job — safety** | AJ-SAF | Customer feels unsafe | Tier 1 + Supervisor + Ops |
| **Active job — pricing dispute** | AJ-PRC | On-site price disagreement | Tier 1 agent |
| **Post-job — refund request** | PJ-REF | Customer wants money back | Tier 1 (≤AED 300) / Tier 2 (>AED 300) |
| **Post-job — quality complaint** | PJ-QUA | Service quality issue | Tier 1 + Quality team |
| **Post-job — rating dispute** | PJ-RAT | Provider disputes customer rating | Provider success (not customer support) |
| **Account & billing** | ACC | Payment method; receipt; account access | Tier 1 |
| **B2B — dispatch issue** | B2B | Fleet/insurance job problem | B2B support specialist |
| **General inquiry** | GEN | How it works; coverage area | Self-service / Tier 1 |

---

## Response Time Standards

| Channel | Active Job | Post-Job | General Inquiry |
|---------|------------|----------|-----------------|
| Phone | Answer ≤30 sec | Answer ≤60 sec | Answer ≤60 sec |
| Live chat | First response ≤60 sec | First response ≤3 min | First response ≤5 min |
| WhatsApp | ≤3 min | ≤15 min | ≤30 min |
| Email | N/A (redirect to phone/chat for active) | ≤4 business hours | ≤8 business hours |

**Resolution targets:**

| Issue Type | Target Resolution |
|------------|-------------------|
| Active job re-dispatch | ≤10 minutes |
| Active job safety | ≤5 minutes (supervisor involved) |
| Refund ≤AED 300 | Same interaction |
| Refund >AED 300 | ≤24 hours |
| Quality complaint | ≤72 hours |
| B2B dispatch issue | ≤30 minutes |

---

## Support Agent Authority Matrix

| Action | Tier 1 Agent | Tier 2 / Supervisor | Ops Manager |
|--------|--------------|---------------------|-------------|
| Issue refund ≤AED 300 | ✓ | ✓ | ✓ |
| Issue refund AED 301–1,000 | — | ✓ | ✓ |
| Issue refund >AED 1,000 | — | — | ✓ |
| Cancel job (any party) | ✓ | ✓ | ✓ |
| Re-dispatch new provider | ✓ (with ops notification) | ✓ | ✓ |
| Apply service credit ≤AED 100 | ✓ | ✓ | ✓ |
| Apply service credit >AED 100 | — | ✓ | ✓ |
| Suspend provider (temporary) | — | ✓ | ✓ |
| Override cancellation fee | — | ✓ | ✓ |
| Escalate to legal | — | ✓ (recommend) | ✓ (approve) |

All actions logged with reason code, job ID, and agent ID.

---

## In-Job vs. Post-Job Support

### In-Job Support Playbook

**Provider delayed (AJ-DEL):**
1. Confirm customer location and safety
2. Contact provider for ETA update
3. If ETA >20 min past commitment: offer re-dispatch or cancellation without fee
4. If provider unresponsive >10 min: auto re-dispatch per [Escalation Policy](./Escalation-Policy.md)

**No provider / no-show (AJ-NOP):**
1. Apologize; confirm customer safety
2. Trigger ops manual dispatch immediately
3. If no provider within 15 min: offer full cancellation + AED 50 service credit
4. Log incident for provider performance action

**Safety concern (AJ-SAF):**
1. Stay on line with customer
2. Supervisor notified immediately
3. Offer police/emergency services guidance if needed
4. Re-dispatch to nearest available provider
5. Post-incident review within 24 hours

**On-site pricing dispute (AJ-PRC):**
1. Review job estimate vs. provider quoted price
2. If increase >20% without in-app approval: instruct provider to revert to estimate or stop service
3. Customer may cancel without fee if dispute unresolved
4. Flag provider for quality review

### Post-Job Support Playbook

**Refund request (PJ-REF):** Follow [Refund Policy](./Refund-Policy.md) decision tree.

**Quality complaint (PJ-QUA):**
1. Collect description and photos if available
2. Contact provider for statement within 24 hours
3. Quality team adjudicates within 72 hours
4. Resolution: refund (partial/full), credit, or upheld charge with explanation

---

## B2B Support Model

| Element | B2B Approach |
|---------|--------------|
| Dedicated contact | Named account manager for fleet/insurance partners |
| SLA | 30-minute response for dispatch issues; 4-hour for billing |
| Channel | Partner portal ticket + direct phone line |
| Reporting | Weekly job summary; monthly SLA compliance report |
| Escalation | B2B specialist → Partnerships director → GM |

B2B customers (fleet dispatchers) receive training during onboarding with direct support line.

---

## Support Quality & Training

**Agent training (2 weeks pre-launch):**
- Platform walkthrough (customer and provider views)
- All policy documents (cancellation, refund, escalation, SLA)
- Role-play: delayed provider, no-show, pricing dispute, safety, refund
- Arabic and English communication standards
- CRM/ticketing system usage

**Quality monitoring:**
- 10% call/chat review weekly by supervisor
- CSAT survey after every support interaction (target ≥4.2/5)
- QA scorecard: empathy, accuracy, resolution, policy adherence

**Agent KPIs:**

| KPI | Target |
|-----|--------|
| First response time (active job) | ≤60 sec |
| First contact resolution | ≥70% |
| CSAT | ≥4.2/5 |
| Policy compliance (QA audit) | ≥95% |
| Escalation rate | ≤15% |

---

## Business Examples

**Example 1 — Delayed provider:** Customer waiting 35 minutes past ETA. Calls hotline. Agent contacts provider — stuck in traffic. Agent offers: wait 15 more minutes (AED 30 credit) or re-dispatch (no fee). Customer chooses re-dispatch. New provider arrives in 18 minutes. Original provider receives ETA penalty on performance score.

**Example 2 — Post-job refund:** Customer charged AED 280 for battery replacement but claims battery failed again next day. Agent collects receipt photo. Quality team contacts provider; provider confirms 30-day warranty. Provider agrees to free re-service. Customer accepts; no refund needed. Case closed in 48 hours.

**Example 3 — B2B fleet issue:** Fleet dispatcher reports provider refused corporate rate on job #4471. B2B specialist reviews contract rate card; confirms provider error. Customer (driver) charged correct rate AED 195. Provider coached on B2B pricing rules. Fleet manager receives corrected invoice within 24 hours.

---

## Business Decisions

| Decision | Rationale |
|----------|-----------|
| Tier 1 agents can refund up to AED 300 | Empowers fast resolution; covers 85% of dispute value |
| Phone + chat mandatory during active jobs | Emergency context demands immediate human contact |
| Proactive outreach on SLA breach | Reduces inbound angry calls; demonstrates platform accountability |
| Separate B2B support track | Fleet/insurance clients have distinct SLAs and billing complexity |
| 60-second chat response for active jobs | Matches customer anxiety level during roadside wait |
| CSAT on every interaction | Support quality directly impacts brand in high-stress category |

---

## Risks

| Risk | Impact | Mitigation |
|------|--------|------------|
| Under-staffing during peak breakdown hours | High | Surge staffing playbook; on-call roster |
| Agent policy inconsistency | Medium | Authority matrix; QA audits; decision tree tools |
| Support becomes cost center without deflection | Medium | Help center investment; in-app self-service for post-job |
| Language barriers (Urdu, Hindi speakers) | Medium | Arabic/English primary; translation support for common phrases |
| Agent burnout from emergency calls | Medium | Shift limits; supervisor debrief; mental health resources |

---

## Assumptions

- 12% of jobs generate a support contact (industry benchmark for on-demand services)
- 70% of support contacts occur during active job (delay, no-show, pricing)
- AED 300 refund authority covers 85% of post-job disputes
- 4 agents sufficient for launch volume (~700 jobs/week at Month 1)
- WhatsApp is preferred follow-up channel for 40% of Arabic-speaking customers

---

## Open Questions

- 24/7 full staffing from launch or phased (on-call off-peak initially)?
- AI chatbot for Tier 0 deflection on general inquiries before launch?
- Video call support option for safety/damage assessment disputes?
- Outsource overflow support to BPO partner for night shifts?

---

## Next Steps

1. Hire 4 Tier 1 agents + 1 supervisor for launch
2. Set up phone hotline, WhatsApp Business, and chat tooling
3. Build support decision trees integrated with CRM
4. Conduct 2-week training program 3 weeks before launch
5. Run support simulation drill with ops team (no-show, safety, refund scenarios)
