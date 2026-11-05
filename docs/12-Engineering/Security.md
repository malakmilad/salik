# Security — Salik Assist MVP

| Field | Value |
|-------|-------|
| **Version** | 1.0 |
| **Status** | Draft |
| **Author** | Engineering |
| **Last Updated** | November 5, 2026 |

## Purpose

Minimum security and privacy controls for MVP launch aligned with UAE PDPL posture and marketplace trust requirements.

## Controls

| Area | MVP requirement |
|------|-----------------|
| Transport | TLS 1.2+ only |
| Auth | OTP rate limits; lockout; secure session tokens |
| Secrets | Vault / cloud secret manager; no secrets in repo |
| Payments | PSP tokenization; never store PAN/CVV |
| PII | Encrypt sensitive fields at rest where practical; minimize logs |
| Documents | Private object storage; signed short-lived URLs |
| RBAC | Ops roles enforced server-side |
| Audit | Immutable logs for dispatch, refunds, suspensions, state changes |
| Mobile | Certificate pinning optional post-MVP; jailbreak detection not required for MVP |
| Abuse | Rate-limit job create, OTP, offer submit |

## Privacy

- Consent for location while job active
- Privacy policy + in-app consent flows before tracking
- Data subject request process (manual ops runbook OK at MVP)
- DPO appointment is a **Block Launch** legal item (L5) — engineering supports export/delete tooling stubs

## Threat Focus (MVP)

1. Fake Arrived / Complete to force payment → geofence + confirm rules
2. Offer collusion / off-platform bypass → monitoring + Rule 11 enforcement ops
3. Document fraud → human verification + expiry automation
4. Account takeover via OTP → rate limits + device signals

## Related

- [Privacy Summary](../07-Legal/Privacy-Summary.md)
- [Compliance](../07-Legal/Compliance.md)
- [SRS](./SRS.md)
