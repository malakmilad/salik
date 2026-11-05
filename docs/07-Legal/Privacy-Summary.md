# Privacy Summary — Salik Assist

| Field | Value |
|-------|-------|
| **Version** | 1.0 |
| **Status** | Draft |
| **Author** | Product & Strategy Team |
| **Last Updated** | July 4, 2026 |

## Purpose

Summarize Salik Assist's approach to collecting, using, storing, and protecting personal data for customers, providers, and partners—supporting compliance planning and operational training. Full Privacy Policy requires legal counsel and DPO review.

## Scope

Covers business and operational privacy practices for UAE/GCC operations. Excludes technical security architecture and data engineering specifications.

## Related Documents

- [Terms Summary](./Terms-Summary.md)
- [Compliance](./Compliance.md)
- [Provider Agreement](./Provider-Agreement.md)
- [Customer Onboarding](../06-Operations/Customer-Onboarding.md)
- [Provider Verification](../06-Operations/Provider-Verification.md)

## Table of Contents

1. [Privacy Principles](#privacy-principles)
2. [Data We Collect](#data-we-collect)
3. [How We Use Data](#how-we-use-data)
4. [Data Sharing & Third Parties](#data-sharing--third-parties)
5. [Location Data](#location-data)
6. [Data Retention](#data-retention)
7. [User Rights](#user-rights)
8. [Security & Breach Response](#security--breach-response)
9. [Children & Vulnerable Users](#children--vulnerable-users)
10. [Cross-Border Transfers](#cross-border-transfers)
11. [Business Examples](#business-examples)
12. [Business Decisions](#business-decisions)
13. [Risks](#risks)
14. [Assumptions](#assumptions)
15. [Open Questions](#open-questions)
16. [Next Steps](#next-steps)

---

## Privacy Principles

Salik Assist privacy practices align with five principles:

1. **Purpose limitation** — Collect only data needed for marketplace operations
2. **Transparency** — Clear notice of what is collected and why
3. **Minimization** — No unnecessary personal data; guest checkout minimizes collection
4. **Security** — Appropriate safeguards for sensitive data (location, payment)
5. **User control** — Access, correction, and deletion rights per applicable law

**Regulatory context:** UAE Federal Decree-Law No. 45 of 2021 on Personal Data Protection (PDPL); potential DIFC/ADGM requirements for specific entities.

---

## Data We Collect

### Customer Data

| Category | Data Elements | Required? |
|----------|---------------|-----------|
| **Identity** | Name, mobile number, email | Mobile required; name/email optional initially |
| **Location** | GPS coordinates, address pin, service location history | Required during active request |
| **Vehicle** | Make, model, year, plate number, color | Optional pre-job; improves matching |
| **Payment** | Card token (not full PAN stored), billing history | Required for B2C payment |
| **Usage** | App interactions, request history, ratings, support tickets | Automatic |
| **Communications** | In-app messages with provider, support chat/call recordings | During active job/support |
| **Device** | Device type, OS, app version, push token | Automatic |

### Provider Data

| Category | Data Elements | Required? |
|----------|---------------|-----------|
| **Business identity** | Trade license, business name, TRN, bank IBAN | Required |
| **Personal identity** | Owner Emirates ID, driver Emirates IDs, photos | Required |
| **Credentials** | Insurance certificates, permits, vehicle registrations | Required |
| **Operational** | GPS location (during active jobs), job history, earnings | Required during service |
| **Performance** | Ratings, SPS, quality audits, training records | Automatic |

### B2B Partner Data

| Category | Data Elements |
|----------|---------------|
| **Organization** | Company name, TRN, contract details, billing contacts |
| **End users** | Policy numbers, fleet vehicle IDs (as shared by partner) |
| **Operational** | Dispatch records, SLA reports, invoice data |

---

## How We Use Data

| Purpose | Data Used | Legal Basis (PDPL Framework) |
|---------|-----------|------------------------------|
| Service delivery & matching | Location, vehicle, provider availability | Contract performance |
| Payment processing | Payment tokens, job amounts | Contract performance |
| Provider verification | Business documents, ID, insurance | Legitimate interest / legal obligation |
| Customer support | Contact info, job history, communications | Contract performance |
| Quality & safety | Ratings, GPS, incident reports | Legitimate interest |
| Fraud prevention | Payment patterns, device info, identity | Legitimate interest |
| Platform improvement | Anonymized usage analytics | Legitimate interest |
| Marketing (opt-in) | Email, push token | Consent |
| Legal compliance | All categories as required | Legal obligation |
| B2B reporting | Partner job data | Contract performance |

**What we do NOT do:**
- Sell personal data to third parties
- Use customer location for advertising when no active request
- Share customer phone number with provider until offer accepted
- Publish customer full name in provider-facing interface (first name + initial)

---

## Data Sharing & Third Parties

| Recipient | Data Shared | Purpose |
|-----------|-------------|---------|
| **Matched provider** | Customer first name, location, vehicle info, issue description, phone (after acceptance) | Service delivery |
| **Matched customer** | Provider business name, rating, photo, vehicle plate, ETA, phone (after acceptance) | Service delivery |
| **Payment processor** | Payment tokens, transaction amounts | Payment processing |
| **Background check provider** | Provider owner ID details | Verification |
| **Insurance partners (B2B)** | Job records, policy numbers, service outcomes | Partner billing and SLA |
| **Cloud infrastructure provider** | Encrypted stored data | Hosting (UAE/GCC region preferred) |
| **Legal/regulatory** | As required by law or court order | Compliance |
| **Analytics (anonymized)** | Aggregated usage patterns | Platform improvement |

**Data Processing Agreements (DPAs):** Required with all third-party processors handling personal data. Vendor assessment before engagement.

---

## Location Data

Location is the most sensitive operational data category for Salik Assist.

| Context | Collection | Retention |
|---------|------------|-----------|
| **Active request** | Continuous customer GPS until job complete | Job record + 90 days |
| **Provider en route** | Provider GPS during active job | Job record + 90 days |
| **Background (customer)** | NOT collected when no active request | — |
| **Background (provider)** | Only when provider marks "Available" | Session only; not stored long-term |
| **Historical** | Service location (not continuous track) | 24 months for dispute/legal |

**Customer controls:** Location permission required for service; can manually pin drop if GPS denied (reduced matching accuracy disclosed).

---

## Data Retention

| Data Category | Retention Period | Deletion Trigger |
|---------------|------------------|------------------|
| Active job records (full) | 24 months | Auto-archive |
| Payment/transaction records | 7 years | Legal/tax requirement |
| Provider verification documents | Duration of relationship + 3 years | Offboarding + 3 years |
| Support tickets | 3 years | Auto-archive |
| Marketing consent records | Until consent withdrawn + 1 year | Opt-out |
| Anonymized analytics | Indefinite | N/A (not personal data) |
| Account data (deleted account) | 30-day grace; then delete | User deletion request |
| GPS tracks (continuous) | 90 days post-job | Auto-delete |

---

## User Rights

Under UAE PDPL and operational policy, users may:

| Right | Customer | Provider | Timeline |
|-------|----------|----------|----------|
| **Access** | Request copy of personal data | Request copy of business/personal data | 30 days |
| **Correction** | Update profile; request correction of errors | Update business profile | Immediate (self-serve) or 15 days |
| **Deletion** | Request account deletion | Request offboarding + data deletion | 30 days (subject to legal holds) |
| **Objection** | Object to marketing | Object to non-essential processing | Immediate for marketing |
| **Portability** | Request data export (JSON/CSV) | Request job/earnings export | 30 days |
| **Withdraw consent** | Marketing opt-out | N/A | Immediate |

**Exceptions:** Deletion may be refused where data required for legal obligation, active dispute, or fraud investigation.

**Request channel:** privacy@salikassist.ae (to be established); in-app privacy settings (Phase 1).

---

## Security & Breach Response

### Security Measures (Business Summary)
- Encryption in transit and at rest for sensitive data
- Access controls: role-based; least privilege
- Payment data handled by PCI-compliant processor (no full card storage)
- Employee privacy training annually
- Vendor security assessment for data processors

### Breach Response Plan

| Stage | Timeline | Action |
|-------|----------|--------|
| Detection | Immediate | Security team alerted |
| Containment | ≤4 hours | Limit exposure; preserve evidence |
| Assessment | ≤24 hours | Scope, data types, individuals affected |
| Notification (regulator) | Per PDPL requirements (72 hours if applicable) | UAE Data Office notification |
| Notification (individuals) | Per PDPL requirements | Affected customers/providers |
| Remediation | ≤30 days | Fix root cause; prevent recurrence |
| Documentation | Ongoing | Breach register maintained |

---

## Children & Vulnerable Users

- Salik Assist is not directed at users under 18
- No knowing collection of data from minors
- Accounts found to be under 18 will be terminated
- Vulnerable users (elderly, disability) receive standard support; no differential data collection

---

## Cross-Border Transfers

| Scenario | Approach |
|----------|----------|
| Data stored in UAE/GCC region | Preferred default |
| Transfer to non-adequate jurisdiction | PDPL-compliant safeguards (SCCs, adequacy decision, or consent) |
| KSA expansion | Local data residency assessment required |
| Analytics tools (US-based) | Anonymized/aggregated only; DPA required |

---

## Business Examples

**Example 1 — Location during job:** Customer submits request; GPS shared with 3 matched providers. Customer accepts Provider A. Provider B and C location access to customer end. Provider A sees customer location until job complete. GPS track deleted 90 days later; service address retained 24 months.

**Example 2 — Deletion request:** Customer deletes account. 30-day grace period (pending jobs resolved). Personal data deleted; transaction records anonymized and retained 7 years for tax. Provider ratings from deleted customer remain (anonymized as "former customer").

**Example 3 — B2B data sharing:** Insurer partner sends policyholder phone and policy number via secure channel. Salik creates linked request. After job, outcome data (service type, cost, completion) returned to insurer. Data shared per DPA; not used for insurer marketing without separate consent.

---

## Business Decisions

| Decision | Rationale |
|----------|-----------|
| No background customer location tracking | Privacy best practice; location only during active request |
| Phone shared only after offer acceptance | Prevents harassment; providers can't cold-call customers |
| 24-month job record retention | Balances dispute resolution with data minimization |
| 7-year financial record retention | UAE tax and commercial law compliance |
| UAE/GCC data residency preferred | PDPL alignment; customer trust in region |
| Guest checkout with minimal data | Emergency use case; full registration encouraged post-job |

---

## Risks

| Risk | Impact | Mitigation |
|------|--------|------------|
| PDPL non-compliance | High | DPO appointment; legal review; privacy impact assessments |
| Data breach | High | Security measures; breach response plan; insurance |
| Provider misuses customer phone number | Medium | Terms prohibition; reporting mechanism; provider penalties |
| Over-collection of data | Medium | Privacy by design reviews; minimization audits |
| Cross-border transfer violations | Medium | GCC hosting; DPAs; anonymization for analytics |

---

## Assumptions

- UAE PDPL enforcement timeline and guidance sufficient for launch compliance
- PCI-compliant payment processor handles card data; Salik avoids PCI scope for storage
- Customers accept location sharing during active requests as necessary for service
- DPO appointment required before launch (or within PDPL timeline)
- Anonymized analytics fall outside PDPL personal data definition

---

## Open Questions

- Appoint DPO internally or outsource?
- Privacy impact assessment required before launch?
- Customer location history visible to customer in app (transparency feature)?
- Provider access to customer data post-job (should be cut off immediately)?

---

## Next Steps

1. Engage legal counsel for full Privacy Policy drafting (Arabic + English)
2. Appoint or designate Data Protection Officer
3. Conduct Privacy Impact Assessment for core data flows
4. Execute DPAs with payment processor, cloud host, background check vendor
5. Establish privacy@salikassist.ae and data subject request process
6. Train support and ops teams on privacy principles and breach escalation
