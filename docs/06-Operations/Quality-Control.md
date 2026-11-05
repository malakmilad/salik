# Quality Control — Salik Assist

| Field | Value |
|-------|-------|
| **Version** | 1.0 |
| **Status** | Draft |
| **Author** | Product & Strategy Team |
| **Last Updated** | July 4, 2026 |

## Purpose

Define quality standards, monitoring processes, audit procedures, and corrective actions that ensure every Salik Assist job meets customer expectations and marketplace trust requirements across all service categories.

## Scope

Covers service quality standards, quality monitoring methods, audit programs, complaint handling integration, and continuous improvement for UAE operations. Excludes technical quality assurance of software products.

## Related Documents

- [Provider Performance](./Provider-Performance.md)
- [Provider Verification](./Provider-Verification.md)
- [SLA](./SLA.md)
- [Refund Policy](./Refund-Policy.md)
- [Escalation Policy](./Escalation-Policy.md)
- [Customer Support](./Customer-Support.md)

## Table of Contents

1. [Quality Framework](#quality-framework)
2. [Service Category Standards](#service-category-standards)
3. [Quality Monitoring Methods](#quality-monitoring-methods)
4. [Quality Triggers & Auto-Flags](#quality-triggers--auto-flags)
5. [Audit Program](#audit-program)
6. [Complaint Investigation Process](#complaint-investigation-process)
7. [Quality Scoring & Provider Impact](#quality-scoring--provider-impact)
8. [Continuous Improvement](#continuous-improvement)
9. [Quality Metrics & Targets](#quality-metrics--targets)
10. [Business Examples](#business-examples)
11. [Business Decisions](#business-decisions)
12. [Risks](#risks)
13. [Assumptions](#assumptions)
14. [Open Questions](#open-questions)
15. [Next Steps](#next-steps)

---

## Quality Framework

Salik Assist quality control operates on four layers:

| Layer | Focus | Frequency |
|-------|-------|-----------|
| **Prevention** | Verification, training, pricing guardrails | At onboarding + ongoing |
| **Detection** | Ratings, automated flags, random audits | Real-time + weekly |
| **Correction** | Refunds, coaching, suspension | Within 72 hours of flag |
| **Improvement** | Root cause analysis, policy updates | Monthly |

**Quality north star:** ≥92% of jobs rated 4+ stars; ≤2% quality-related refund rate.

---

## Service Category Standards

### Universal Standards (All Categories)

| Standard | Requirement |
|----------|-------------|
| Professional appearance | Uniform or branded vest; clean vehicle |
| Communication | Contact customer within 2 min of acceptance; ETA updates if >10 min change |
| Identification | Provider identifies self and Salik Assist affiliation on arrival |
| Pricing transparency | No additional charges without in-app customer approval |
| Safety | Warning triangles deployed on highway; PPE where applicable |
| Documentation | Completion photo uploaded for jobs >AED 200 (optional at MVP; mandatory Phase 1) |
| Cleanliness | No damage to customer vehicle interior/exterior during service |
| Payment | No cash demand outside platform payment flow (except approved exceptions) |

### Category-Specific Standards

| Category | Additional Standards |
|----------|-------------------|
| **Tow / Recovery** | Proper attachment points used; vehicle secured before transit; destination confirmed in-app |
| **Battery** | Voltage tested before/after; old battery disposed responsibly if replaced; 30-day warranty on replacements |
| **Tire** | Torque specifications followed; spare tire condition verified; damaged tire secured if removed |
| **Fuel Delivery** | Correct fuel type confirmed before dispensing; spill prevention; receipt of quantity dispensed |
| **Mobile Mechanic** | Diagnosis explained before repair; parts cost approved in-app; test drive/verification after repair |
| **Lockout** | Non-destructive entry attempted first; customer consent for any damage-risk method; ID verification if vehicle ownership unclear |

---

## Quality Monitoring Methods

| Method | Description | Coverage |
|--------|-------------|----------|
| **Customer ratings** | 1–5 stars + optional comment post-job | 100% of completed jobs |
| **Automated keyword flagging** | Comments containing: damage, rude, overcharge, scam, unsafe, never arrived | 100% of comments |
| **Random job audit** | Ops reviews 5% of completed jobs weekly (GPS, timestamps, pricing) | 5% sample |
| **Mystery shopper program** | Salik-contracted testers submit real requests monthly | 20 jobs/month at launch |
| **Provider self-reporting** | Provider uploads completion evidence | Target 80% compliance |
| **B2B partner feedback** | Fleet/insurance SLA scorecards | 100% of B2B jobs |
| **Support ticket correlation** | Quality complaints linked to job records | 100% of PJ-QUA tickets |

---

## Quality Triggers & Auto-Flags

| Trigger | Threshold | Auto-Action |
|---------|-----------|-------------|
| Rating ≤2 stars | Any single job | Quality review within 24 hours |
| Rating ≤3 stars | 3 in rolling 10 jobs | Provider coaching notification |
| Keyword flag | Any flagged comment | Quality review within 24 hours |
| Refund processed (quality reason) | Any | Provider performance impact; quality log |
| SLA breach + completion | ETA >45 min past commitment | Auto-flag for review |
| Price variance | Final >120% of estimate without approval | Auto-flag; hold provider payout |
| Same customer complaint | 2nd complaint about same provider | Escalated review |
| Mystery shop failure | Any failed criterion | Provider coaching within 48 hours |

---

## Audit Program

### Random Audit (Weekly)

**Selection criteria (weighted):**
- 30% — New providers (<30 days active)
- 25% — Providers with SPS <75
- 20% — Jobs >AED 500
- 15% — B2B/insurance jobs
- 10% — Random from remaining pool

**Audit checklist:**
- [ ] Timestamps align (acceptance → en route → arrive → complete)
- [ ] GPS route reasonable (no excessive detours)
- [ ] Price within estimate or approved revision on record
- [ ] Customer rating and comment reviewed
- [ ] Completion evidence present (if required)
- [ ] No open support tickets unresolved

**Outcome:** Pass / Fail (minor) / Fail (major). Major fail triggers provider review.

### Provider Site Audit (Quarterly)

- 10% of active providers receive in-person or video audit annually
- Checklist: vehicle condition, equipment, insurance docs current, driver presentation
- Tier 2 Premium Verified providers: mandatory annual in-person audit

### Mystery Shop Program

| Element | Standard |
|---------|----------|
| Frequency | 20 jobs/month (launch); 50/month (Year 1) |
| Distribution | Across all categories and Dubai zones |
| Evaluation | 20-point scorecard per category standards |
| Pass threshold | ≥16/20 |
| Fail consequence | Provider coaching; 2 fails in 90 days → performance review |

---

## Complaint Investigation Process

```
Flag/Complaint → Triage → Evidence Collection → Adjudication → Resolution → Follow-up
```

| Step | Timeline | Actions |
|------|----------|---------|
| **Triage** | ≤4 hours | Classify severity (minor/moderate/severe); assign investigator |
| **Evidence collection** | ≤24 hours | Customer statement, photos; provider statement; job record; GPS |
| **Adjudication** | ≤48 hours | Quality team decision: upheld, partially upheld, not upheld |
| **Resolution** | ≤72 hours total | Refund per [Refund Policy](./Refund-Policy.md); coaching; suspension |
| **Follow-up** | +7 days | Verify no repeat; close case |

**Evidence standards:**
- Customer photos of damage: sufficient for moderate/severe vehicle damage claims
- Provider completion photos: sufficient to verify service performed
- GPS data: authoritative for no-show and ETA disputes
- Communication logs: reviewed for professionalism assessment

---

## Quality Scoring & Provider Impact

**Provider Quality Index (PQI)** — subset of SPS focused on quality-specific metrics:

| Component | Weight |
|-----------|--------|
| Average customer rating (30 jobs) | 40% |
| Quality complaint rate | 25% |
| Mystery shop score | 15% |
| Audit pass rate | 10% |
| Completion evidence compliance | 10% |

| PQI Range | Action |
|-----------|--------|
| ≥85 | Eligible for quality excellence bonus |
| 70–84 | Standard operations |
| 55–69 | Mandatory coaching |
| 40–54 | Probation (30 days); weekly monitoring |
| <40 | Suspension pending review |

**Quality excellence bonus:** AED 500/month for providers with PQI ≥85 and zero quality complaints.

---

## Continuous Improvement

| Activity | Frequency | Owner |
|----------|-----------|-------|
| Quality review meeting | Weekly | Head of Quality + Ops |
| Top complaint category analysis | Monthly | Quality team |
| Provider feedback session (focus group) | Quarterly | Ops + top 20 providers |
| Standard revision | As needed (min. semi-annual review) | Quality + Legal |
| Training content update | Within 30 days of new standard | Onboarding team |

**Feedback loop:** Quality findings → training update → provider communication → metric monitoring → repeat.

---

## Quality Metrics & Targets

| Metric | Launch Target | Year 1 Target |
|--------|---------------|---------------|
| Jobs rated 4+ stars | 88% | 92% |
| Jobs rated ≤2 stars | <3% | <2% |
| Quality-related refund rate | <3% | <2% |
| Complaint resolution within 72 hr | 90% | 95% |
| Mystery shop pass rate | 80% | 90% |
| Random audit pass rate | 85% | 90% |
| Repeat complaint rate (same provider) | <5% | <3% |
| Provider coaching completion rate | 90% | 95% |

---

## Business Examples

**Example 1 — Minor quality issue:** Customer rates 3 stars: "Service fine but provider was 20 minutes late without update." Auto-flagged. Quality review confirms ETA breach. Provider coached on communication. Customer offered AED 30 credit (25% partial refund declined; credit accepted).

**Example 2 — Severe quality failure:** Customer reports tow provider damaged bumper during loading. Photos submitted. Provider denies. GPS and timestamp confirm provider on-site. Quality team upholds complaint. 75% refund (AED 210 on AED 280 job). Provider suspended 14 days; retraining required.

**Example 3 — Mystery shop fail:** Mystery shopper requests battery jump. Provider arrives without branded vest, does not test voltage, attempts to sell unnecessary replacement. Scores 11/20. Provider coached within 48 hours. Re-test in 30 days required.

**Example 4 — False complaint:** Customer claims service not performed. Provider uploads completion photo with timestamp and customer signature equivalent (in-app acknowledgment). GPS confirms provider on-site 25 minutes. Complaint not upheld. Customer educated on dispute process.

---

## Business Decisions

| Decision | Rationale |
|----------|-----------|
| 4+ stars as quality north star (not 5) | Realistic target; 5-star inflation reduces signal quality |
| Mystery shop program from launch | Proactive quality detection beyond customer-initiated feedback |
| Auto-flag on ≤2 stars and keywords | Emergency category requires fast response to trust erosion |
| PQI separate weighting from overall SPS | Quality-specific focus for coaching and bonus eligibility |
| 72-hour complaint resolution SLA | Matches customer expectation; aligns with refund policy |
| Provider coaching before suspension (first offense minor) | Many quality issues are training gaps, not bad faith |

---

## Risks

| Risk | Impact | Mitigation |
|------|--------|------------|
| Low rating participation rate | Medium | Prompt immediately post-job; incentive (credit entry) |
| Mystery shop program cost | Low | 20/month at launch; high ROI on trust |
| Provider resistance to completion photos | Medium | Phase in: optional MVP, mandatory Phase 1 |
| Quality team understaffed at scale | Medium | Hire 1 quality specialist at launch; 3 by Year 1 |
| Subjective quality adjudication | Medium | Standardized scorecards; supervisor review on severe cases |

---

## Assumptions

- 75% of customers will leave a rating post-job
- 8% of rated jobs will be ≤3 stars
- Mystery shop pass rate will start at ~80% and improve with coaching
- Providers will comply with completion photo requirement when enforced via payout hold
- Quality complaints correlate strongly with ≤2 star ratings (85% overlap)

---

## Open Questions

- Mandatory in-app customer sign-off before provider marks complete?
- Third-party quality certification (ISO or industry body) for Elite providers?
- Customer quality panel (trusted raters) for disputed cases?
- Quality standards harmonization for KSA expansion?

---

## Next Steps

1. Hire quality specialist for launch
2. Build 20-point mystery shop scorecard per category
3. Define automated keyword flag list and review queue
4. Integrate quality triggers with provider performance system
5. Conduct first mystery shop batch 2 weeks before public launch
