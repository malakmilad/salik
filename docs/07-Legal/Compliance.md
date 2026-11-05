# Compliance — Salik Assist

| Field | Value |
|-------|-------|
| **Version** | 1.0 |
| **Status** | Draft |
| **Author** | Product & Strategy Team |
| **Last Updated** | July 4, 2026 |

## Purpose

Identify regulatory, legal, and industry compliance requirements applicable to Salik Assist as a roadside assistance marketplace operating in the UAE and GCC—establishing a compliance framework for launch and expansion.

## Scope

Covers business-relevant compliance domains for UAE launch: marketplace regulation, consumer protection, data privacy, transport/recovery licensing context, insurance, payments, and employment. Excludes technical compliance certifications (PCI-DSS implementation details).

## Related Documents

- [Terms Summary](./Terms-Summary.md)
- [Privacy Summary](./Privacy-Summary.md)
- [Provider Agreement](./Provider-Agreement.md)
- [Provider Verification](../06-Operations/Provider-Verification.md)
- [Compliance](../07-Legal/Compliance.md)

## Table of Contents

1. [Compliance Framework](#compliance-framework)
2. [Marketplace & Platform Regulation](#marketplace--platform-regulation)
3. [Consumer Protection](#consumer-protection)
4. [Data Protection & Privacy](#data-protection--privacy)
5. [Transport & Recovery Licensing](#transport--recovery-licensing)
6. [Insurance Requirements](#insurance-requirements)
7. [Payment & Financial Compliance](#payment--financial-compliance)
8. [Employment & Labor](#employment--labor)
9. [Advertising & Marketing](#advertising--marketing)
10. [Compliance Governance](#compliance-governance)
11. [Expansion Compliance (GCC)](#expansion-compliance-gcc)
12. [Business Examples](#business-examples)
13. [Business Decisions](#business-decisions)
14. [Risks](#risks)
15. [Assumptions](#assumptions)
16. [Open Questions](#open-questions)
17. [Next Steps](#next-steps)

---

## Compliance Framework

Salik Assist compliance program structured around:

| Pillar | Focus |
|--------|-------|
| **Licensing & registration** | Entity setup, trade licenses, activity codes |
| **Marketplace regulation** | Intermediary classification, provider independence |
| **Consumer protection** | Fair pricing, dispute resolution, advertising |
| **Data privacy** | PDPL compliance, DPO, data subject rights |
| **Sector-specific** | RTA recovery permits, commercial insurance |
| **Financial** | VAT, payment regulations, anti-money laundering |
| **Governance** | Policies, training, audit, incident response |

**Compliance owner:** General Counsel / Head of Legal (to be hired); interim: CEO + external counsel.

---

## Marketplace & Platform Regulation

### Entity & Licensing

| Requirement | Status | Notes |
|-------------|--------|-------|
| UAE mainland or free zone entity | Required pre-launch | Activity: IT platform / marketplace services |
| Trade license with correct activity codes | Required | Counsel to confirm codes (e.g., online marketplace, IT services) |
| VAT registration (TRN) | Required if turnover > AED 375K | Voluntary registration acceptable at launch |
| E-commerce compliance (TDRA/NMC guidelines) | Required | Terms, privacy, contact details on platform |

### Marketplace Classification

**Target classification:** Technology marketplace / intermediary — NOT transport operator, NOT recovery service provider.

| Factor | Salik Assist Position |
|--------|----------------------|
| Owns fleet? | No |
| Employs drivers? | No |
| Sets service prices unilaterally? | No (guardrails only; providers set rates) |
| Performs roadside service? | No |
| Controls provider work methods? | Standards only; providers independent |

**Risk:** Regulator or insurer classifies platform as de facto transport operator. **Mitigation:** Legal opinion; clear terms; provider independence in [Provider Agreement](./Provider-Agreement.md).

---

## Consumer Protection

### UAE Consumer Protection Law (Federal Law No. 15 of 2020)

| Requirement | Salik Assist Implementation |
|-------------|----------------------------|
| Clear pricing before purchase | Price estimate pre-request; firm offer pre-acceptance |
| Right to cancel | [Cancellation Policy](../06-Operations/Cancellation-Policy.md) |
| Refund for non-delivery | [Refund Policy](../06-Operations/Refund-Policy.md) |
| Accurate advertising | Marketing review process; no false ETA/price claims |
| Complaint mechanism | 24/7 support; escalation policy |
| Arabic language access | Arabic app, terms, and support |

### Specific Consumer Protections

| Area | Compliance Action |
|------|-------------------|
| Surge pricing | Disclosed before acceptance; cap on surge multiplier (2.5× base) |
| Hidden fees | Itemized receipt; no post-hoc charges without approval |
| Provider credentials | Verification badge; accurate representation |
| Dispute resolution | 72-hour resolution SLA; documented process |

---

## Data Protection & Privacy

See [Privacy Summary](./Privacy-Summary.md) for detail.

| Requirement | PDPL (Federal Decree-Law 45/2021) |
|-------------|-------------------------------------|
| Lawful basis for processing | Documented per data category |
| Data Protection Officer | Appoint before or at launch |
| Privacy notice | Arabic + English Privacy Policy |
| Data subject rights | Access, correction, deletion process |
| Breach notification | 72-hour regulator notification (if applicable) |
| Cross-border transfers | Safeguards for non-adequate jurisdictions |
| Privacy Impact Assessment | For high-risk processing (location, payment) |

---

## Transport & Recovery Licensing

**Key principle:** Salik Assist does not perform transport/recovery; providers must hold required licenses.

| Requirement | Applies To | Salik Assist Role |
|-------------|------------|-------------------|
| RTA recovery permit | Tow providers (Dubai) | Verify at onboarding; monitor expiry |
| Commercial vehicle registration | All provider fleet | Verify |
| ADTA/ITC permits | Tow providers (Abu Dhabi/Sharjah) | Verify when expanding |
| Driver licensing | Provider drivers | Verify appropriate class |

**Platform obligation:** Verify provider licenses; do not permit unlicensed tow/recovery operators to accept tow jobs. Category gating in matching.

---

## Insurance Requirements

| Insurance Type | Applies To | Minimum Coverage |
|----------------|------------|------------------|
| Commercial vehicle / liability | All providers | AED 1M third-party liability |
| Enhanced liability | Premium verified providers | AED 2M |
| Professional indemnity | Salik Assist entity | Counsel to advise amount |
| Cyber insurance | Salik Assist entity | Recommended at launch |
| Workers compensation | Provider employees | Provider responsibility (not Salik) |

**Claims process:** Customer vehicle damage → provider commercial insurance primary → Salik Assist facilitates documentation → platform not insurer of record.

---

## Payment & Financial Compliance

| Requirement | Implementation |
|-------------|----------------|
| **VAT (5%)** | Applied to platform commission and applicable service fees; TRN on invoices |
| **PCI-DSS** | Payment processing via licensed PCI-compliant processor; no card storage |
| **AML/CFT** | KYC on providers (business verification); monitor for suspicious transaction patterns |
| **Central Bank regulations** | Use licensed payment acquirer; no unauthorized payment aggregation |
| **Record keeping** | 7-year financial record retention |

**Provider payouts:** Bank transfer to verified UAE business account; payout records maintained for audit.

---

## Employment & Labor

| Topic | Salik Assist Position |
|-------|----------------------|
| Provider employment status | Independent contractors / business owners — NOT Salik employees |
| Provider drivers | Employed by provider; provider responsible for visas, labor cards, wages |
| Misclassification risk | Providers control schedule, equipment, pricing; multi-platform allowed |
| Salik employees | UAE labor law compliance for platform staff |

**Compliance action:** Provider Agreement explicitly states independent contractor relationship; providers represent compliance with UAE labor law for their employees.

---

## Advertising & Marketing

| Requirement | Implementation |
|-------------|----------------|
| Accurate claims | No guaranteed ETAs in marketing (SLA commitments ≠ ads) |
| Influencer disclosure | Paid partnerships disclosed per UAE NMC guidelines |
| Arabic advertising | Key campaigns in Arabic for UAE market |
| Comparison advertising | Factual only; no disparagement of competitors |
| Emergency services implication | Do not imply Salik is emergency services (police/ambulance) |

---

## Compliance Governance

### Compliance Calendar

| Activity | Frequency | Owner |
|----------|-----------|-------|
| Provider license expiry audit | Weekly (automated) + quarterly manual | Verification team |
| Privacy compliance review | Quarterly | DPO |
| Terms and policy review | Semi-annual | Legal |
| Compliance training (staff) | Annual + onboarding | HR/Legal |
| Regulatory monitoring | Ongoing | Legal counsel |
| Internal compliance audit | Annual | External auditor (Year 2) |

### Incident & Reporting

| Incident Type | Report To | Timeline |
|---------------|-----------|----------|
| Data breach | UAE Data Office + affected individuals | Per PDPL |
| Serious safety incident | Internal + potentially RTA/police | Immediate |
| Provider license fraud | Internal + potentially authorities | 24 hours |
| Consumer protection complaint (official) | Legal + respond to authority | Per request |
| AML suspicious activity | Compliance officer + FIU if required | Per AML policy |

---

## Expansion Compliance (GCC)

| Market | Key Additional Requirements | Timeline |
|--------|----------------------------|----------|
| **KSA** | SDAIA data law; MCI e-commerce; local entity; Arabic mandatory | Phase 3 |
| **Qatar** | MCIT regulations; local partnership may be required | Phase 3+ |
| **Bahrain** | PDPL (Bahrain); CBB payment rules if applicable | Phase 3+ |
| **Oman** | Local entity; Arabic; transport authority permits | Phase 3+ |
| **Kuwait** | Local agent/entity requirements | Phase 3+ |

Each expansion requires legal feasibility study before market entry decision.

---

## Business Examples

**Example 1 — RTA permit verification:** Tow provider applies with valid trade license but expired RTA recovery permit. Verification team rejects tow category; approves battery category only. Provider renews permit; tow category activated. Compliance maintained.

**Example 2 — Consumer protection complaint:** Customer files complaint with UAE Consumer Protection department alleging hidden fees. Legal team responds within required timeline with job record showing itemized receipt and in-app price approval. Complaint resolved; no violation found.

**Example 3 — VAT compliance:** Salik Assist exceeds AED 375K turnover in Month 8. TRN registered retroactively per advisor guidance. All subsequent invoices include 5% VAT on platform fees. Provider payouts documented for audit.

---

## Business Decisions

| Decision | Rationale |
|----------|-----------|
| Marketplace intermediary classification | Avoids transport operator licensing; scalable model |
| Provider-side licensing verification | Platform liability mitigation; customer trust |
| PDPL compliance from launch | Regulatory trend; customer trust; avoids retrofit cost |
| PCI via third-party processor | Avoid direct PCI compliance burden |
| Independent contractor provider model | Labor law alignment; provider flexibility |
| Compliance calendar from Month 1 | Prevents drift; supports Series A diligence |

---

## Risks

| Risk | Impact | Mitigation |
|------|--------|------------|
| Reclassification as transport operator | High | Legal opinion; marketplace terms; regulatory engagement |
| PDPL enforcement action | High | DPO; PIA; privacy program |
| Provider operates without valid license | High | Verification; continuous monitoring; auto-suspension |
| Consumer protection violation | Medium | Clear policies; support SLAs; Arabic access |
| AML/KYC failure on provider side | Medium | Business verification; monitoring |
| Expansion compliance gaps | Medium | Market-specific legal study before entry |

---

## Assumptions

- UAE marketplace intermediary model is legally viable with proper structure
- Provider licensing verification satisfies platform due diligence obligation
- PDPL compliance achievable at launch scale with DPO and policies
- Salik Assist entity registered in UAE mainland or appropriate free zone before launch
- VAT registration manageable within first year of operations

---

## Open Questions

- Optimal entity structure: mainland Dubai vs. DIFC vs. ADGM?
- Professional indemnity insurance — required or recommended at launch?
- Direct engagement with RTA on marketplace model (proactive vs. reactive)?
- SAMA/CBU involvement if insurance partnerships expand to payment flows?

---

## Next Steps

1. Engage UAE regulatory/commercial legal counsel for entity setup and classification opinion
2. Appoint DPO and initiate Privacy Impact Assessment
3. Confirm trade license activity codes with licensing authority
4. Register for VAT when threshold approached (or voluntarily at launch)
5. Build compliance calendar and assign owners
6. Conduct provider licensing requirements audit by emirate for expansion planning
