# Provider Verification — Salik Assist

| Field | Value |
|-------|-------|
| **Version** | 1.0 |
| **Status** | Draft |
| **Author** | Product & Strategy Team |
| **Last Updated** | July 4, 2026 |

## Purpose

Establish the verification standards, process, and ongoing compliance checks that ensure every provider on Salik Assist meets legal, safety, and quality requirements—forming the primary trust moat for customers in emergency contexts.

## Scope

Covers initial verification at onboarding, periodic re-verification, category-specific requirements, and verification badge display rules for UAE operations. Excludes technical identity verification systems.

## Related Documents

- [Provider Onboarding](./Provider-Onboarding.md)
- [Provider Agreement](../07-Legal/Provider-Agreement.md)
- [Compliance](../07-Legal/Compliance.md)
- [Quality Control](./Quality-Control.md)
- [Provider Performance](./Provider-Performance.md)

## Table of Contents

1. [Verification Framework](#verification-framework)
2. [Verification Tiers](#verification-tiers)
3. [Document Verification Checklist](#document-verification-checklist)
4. [Category-Specific Requirements](#category-specific-requirements)
5. [Verification Process Steps](#verification-process-steps)
6. [Ongoing Compliance & Re-Verification](#ongoing-compliance--re-verification)
7. [Verification Badges & Customer Display](#verification-badges--customer-display)
8. [Rejection & Appeal Process](#rejection--appeal-process)
9. [Verification SLAs & Team Structure](#verification-slas--team-structure)
10. [Business Examples](#business-examples)
11. [Business Decisions](#business-decisions)
12. [Risks](#risks)
13. [Assumptions](#assumptions)
14. [Open Questions](#open-questions)
15. [Next Steps](#next-steps)

---

## Verification Framework

Salik Assist verification operates on four pillars:

| Pillar | What We Verify | Why It Matters |
|--------|----------------|----------------|
| **Legal** | Trade license, permits, business registration | Marketplace liability; regulatory compliance |
| **Financial** | Insurance coverage, bank account legitimacy | Customer protection; payout integrity |
| **Identity** | Owner/signatory identity, background check | Fraud prevention; accountability |
| **Operational** | Vehicle condition, equipment, service capability | Service quality; safety |

**Principle:** No provider receives customer-facing offers until all mandatory checks pass. Conditional approval permitted only for non-critical missing items with 14-day remediation deadline.

---

## Verification Tiers

### Tier 1: Standard Verified (Default)

All launch providers must achieve Tier 1:

- Valid UAE trade license
- Commercial vehicle insurance (min. AED 1M third-party liability)
- Vehicle registration for all fleet units in matching pool
- Owner Emirates ID verified
- Category-appropriate permits
- Bank account matching business name
- Platform training certification

**Customer display:** "Verified Provider" badge

### Tier 2: Premium Verified

Optional upgrade with enhanced checks:

- In-person vehicle inspection by Salik field agent
- AED 2M insurance coverage
- 6+ months operating history on platform with ≥4.5 rating
- Background check on all active drivers
- GPS tracking device confirmation on all fleet units

**Customer display:** "Premium Verified" badge + priority in matching tie-breaks

**Benefits:** T+1 payout, 2% commission discount, featured placement in competitive zones

### Tier 3: Partner Verified (B2B)

For providers serving insurance/fleet contracts:

- All Tier 2 requirements
- Signed B2B rate card adherence audit
- Quarterly performance review with partnerships team
- Dedicated SLA compliance (see [SLA](./SLA.md))

**Customer display:** "Insurance Approved" or partner co-brand where applicable

---

## Document Verification Checklist

| # | Document | Verification Method | Pass Criteria | Fail Action |
|---|----------|---------------------|---------------|-------------|
| 1 | Trade License | Manual review + DED/public registry cross-check | Active; business activity includes relevant services | Reject; request renewal |
| 2 | Emirates ID (owner) | Photo review; name match to license | Valid; not expired | Reject until updated |
| 3 | Vehicle Registration (each unit) | Photo review | Commercial registration; matches submitted plate | Exclude vehicle from pool |
| 4 | Vehicle Insurance | Certificate review; insurer validation call (10% sample) | Commercial use covered; min. AED 1M liability; valid dates | Reject until corrected |
| 5 | RTA Recovery Permit | Permit photo review (tow category) | Valid for tow/recovery operations | Reject tow category until obtained |
| 6 | Bank IBAN Letter | Document review | Business name matches license | Reject until corrected |
| 7 | VAT TRN | FTA registry check (if provided) | Valid and matches business | Flag for finance review |
| 8 | Driver license (each driver) | Photo review | Valid UAE or recognized license; appropriate class | Driver excluded until valid |

**Document freshness:** All documents must be current at verification. Expiry tracked; auto-reminder at 60, 30, and 7 days before expiration.

---

## Category-Specific Requirements

| Category | Additional Requirements | Minimum Equipment |
|----------|------------------------|-------------------|
| **Tow / Recovery** | RTA recovery permit; tow truck registration | Working winch/flatbed; safety chains; warning triangles |
| **Battery** | — | Jump cables or portable power unit; battery stock (if replacement offered) |
| **Tire** | — | Jack, wrench, portable inflator or tire repair kit |
| **Fuel Delivery** | Fuel transport authorization where applicable | Approved containers; spill kit |
| **Mobile Mechanic** | — | Basic diagnostic tools; common parts inventory list declared |
| **Lockout** | — | Professional lockout tools (no destructive entry without consent) |

**Photo evidence required at onboarding:**
- Front and rear of each service vehicle with visible plate
- Insurance certificate
- Equipment photo (category-specific)
- Business storefront or yard (if applicable)

---

## Verification Process Steps

```
Application Received → Document Review → Identity Check → Insurance Validation → 
Category Compliance → Risk Scoring → Decision → Notification
```

### Step 1: Document Review (Day 1–2)
Verification specialist reviews all submitted documents against checklist. Incomplete applications paused with specific deficiency list sent to provider.

### Step 2: Identity & Background Check (Day 2–4)
- Owner Emirates ID matched to trade license authorized signatory
- Background check via approved UAE screening partner for fraud, financial crimes, and violent offenses
- **Automatic disqualification:** Fraud conviction, active warrant, falsified documents

### Step 3: Insurance Validation (Day 3–5)
- Certificate authenticity review
- Confirm policy covers commercial roadside activity (not personal auto policy)
- 10% random sample: direct call to insurer for validation

### Step 4: Category Compliance (Day 3–5)
- Equipment photos reviewed against category requirements
- Service radius and base location validated against launch geography

### Step 5: Risk Scoring (Day 4–5)
Composite risk score (0–100):

| Factor | Weight |
|--------|--------|
| Document completeness | 25% |
| Insurance coverage level | 20% |
| Business tenure (years licensed) | 15% |
| Background check result | 20% |
| Category compliance | 10% |
| Referral from existing verified provider | 10% |

**Thresholds:**
- Score ≥70: Approve
- Score 50–69: Conditional approval (remediation required within 14 days)
- Score <50: Reject with appeal option

### Step 6: Decision & Notification (Day 5)
- Approved: Welcome email + training enrollment
- Conditional: Specific remediation list + 14-day deadline
- Rejected: Reason code + appeal instructions

---

## Ongoing Compliance & Re-Verification

| Check | Frequency | Trigger for Immediate Review |
|-------|-----------|------------------------------|
| Trade license validity | Continuous monitoring | Expiry or suspension |
| Insurance validity | Continuous monitoring | Lapse or coverage reduction |
| Vehicle registration | Annual | New vehicle added |
| Background check (owner) | Every 24 months | Safety complaint or fraud flag |
| Random document audit | 10% of active providers quarterly | — |
| In-person inspection | Tier 2: annual; Tier 1: on complaint | Quality score drop |

**Auto-suspension rules:**
- Insurance lapse: Immediate suspension; no new offers
- License expired >30 days: Suspension until renewed
- Failed random audit: 7-day suspension pending remediation

---

## Verification Badges & Customer Display

| Badge | Display Location | Customer Message |
|-------|------------------|------------------|
| Verified Provider | Offer card, profile, tracking screen | "Licensed & insured provider verified by Salik Assist" |
| Premium Verified | Offer card (highlighted) | "Premium verified — enhanced insurance & inspection" |
| New Provider | Offer card (first 30 days) | "New to Salik Assist — verified and monitored" |
| Insurance Approved | B2B jobs | "Approved by [Partner Name]" |

Badges removed immediately upon suspension. Reinstatement requires re-verification if suspension exceeded 30 days.

---

## Rejection & Appeal Process

**Rejection categories:**
1. **Documentation deficiency** — May reapply immediately upon correction
2. **Insurance inadequate** — Reapply when compliant policy obtained
3. **Background check failure** — Appeal within 14 days with supporting evidence
4. **Fraud / falsification** — Permanent ban; no appeal

**Appeal process:**
1. Provider submits appeal form within 14 days of rejection
2. Senior verification manager reviews within 5 business days
3. Decision final unless new material evidence provided within 7 days
4. Appeal outcomes: Uphold rejection, overturn (approve), or request additional documentation

---

## Verification SLAs & Team Structure

| Activity | SLA | Team |
|----------|-----|------|
| Initial document review | ≤48 hours of complete submission | Verification specialists (2 at launch) |
| Full verification decision | ≤5 business days | Verification team |
| Appeal review | ≤5 business days | Senior verification manager |
| Re-verification (expired docs) | ≤3 business days | Verification specialists |
| Random audit completion | ≤10 business days of selection | Field ops + verification |

**Launch staffing:** 2 verification specialists + 1 senior manager; scale to 5 specialists by Month 6.

---

## Business Examples

**Example 1 — Standard approval:** Al Quoz tow company submits complete documentation. Trade license active since 2019. Insurance AED 1.5M liability confirmed. RTA permit valid. Background check clear. Risk score 82. Approved Tier 1 in 4 business days.

**Example 2 — Conditional approval:** Battery specialist submits all documents except VAT TRN ( turnover below threshold — not required). Insurance valid. Conditional approval granted; TRN waived. Provider completes training and activates.

**Example 3 — Rejection and appeal:** Applicant submits trade license under Company A but bank account under Company B (owner's personal account). Rejected for financial integrity. Applicant opens business bank account under Company A, re-applies, approved on second submission.

**Example 4 — Mid-operation suspension:** Verified provider's insurance expires. System auto-detects on expiry date. Provider suspended at midnight; 2 pending offers cancelled. Provider uploads renewed certificate within 24 hours; re-verified and reactivated in 2 business days.

---

## Business Decisions

| Decision | Rationale |
|----------|-----------|
| No offers until full Tier 1 verification | Trust is non-negotiable in emergency marketplace; partial verification erodes brand |
| AED 1M minimum insurance | Balances provider cost with basic customer protection; Tier 2 requires AED 2M |
| 10% random insurer validation calls | Deterrent against fraudulent certificates without verifying 100% (cost control) |
| Risk scoring with conditional band | Allows promising providers with minor gaps to remediate rather than outright reject |
| Auto-suspension on insurance lapse | Zero tolerance; operating without insurance creates unacceptable liability |
| Permanent ban for document falsification | Protects marketplace integrity; one bad actor damages all providers |

---

## Risks

| Risk | Impact | Mitigation |
|------|--------|------------|
| Fraudulent documents pass manual review | High | Random audits; insurer calls; field inspections for Tier 2 |
| Verification bottleneck delays supply | Medium | Dedicated team; clear SLAs; conditional approval path |
| Provider operates with expired docs between checks | High | Continuous expiry monitoring; auto-suspension |
| Over-verification slows onboarding vs. competitors | Medium | Photo-based MVP; Tier 2 optional premium path |
| Background check false positives | Low | Appeal process; manual review of edge cases |

---

## Assumptions

- UAE public registries (DED, RTA) are accessible for cross-checking within verification SLA
- Approved background check partner covers UAE residents and common expat nationalities
- 85% of applicants can achieve Tier 1 within 5 business days
- Providers will maintain document validity if reminded at 60/30/7 days
- Customers actively look for verification badges when choosing offers

---

## Open Questions

- Third-party verification API partnership (e.g., UAE Pass integration) for faster identity checks?
- Require dashcam or body camera for Tier 2 premium verification?
- Verify driver-level credentials separately from business entity?
- Cross-border provider verification for KSA expansion — replicate or localize?

---

## Next Steps

1. Contract background check screening partner
2. Build document expiry tracking and auto-reminder workflow
3. Train verification team on checklist and risk scoring
4. Define random audit selection algorithm (weighted toward new providers and complaint history)
5. Publish verification badge guidelines for marketing and customer education
