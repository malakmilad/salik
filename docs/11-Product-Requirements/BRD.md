# Business Requirements Document (BRD) — Delivery View

| Field | Value |
|-------|-------|
| **Version** | 1.0 |
| **Status** | Draft |
| **Author** | Product & Strategy / Engineering |
| **Last Updated** | November 5, 2026 |

## Purpose

Translate [Business Requirements](../04-Business/Business-Requirements.md) into an execution-ready delivery view for MVP: which requirements are in the first build, which are deferred, and how they trace to PRD epics and launch gates.

## Scope

MVP Dubai launch only. B2B and multi-category expansion remain documented but **out of build** until Phase 1 go/no-go.

## Related Documents

- [PRD](./PRD.md)
- [Business Requirements](../04-Business/Business-Requirements.md)
- [Business Rules](../04-Business/Business-Rules.md)
- [Constraints](../04-Business/Constraints.md)
- [MVP](../09-Roadmap/MVP.md)
- [Launch Readiness Checklist](../14-Launch/Launch-Readiness-Checklist.md)

---

## Priority Definitions

| Priority | Meaning for delivery |
|----------|----------------------|
| **P0** | Must ship before public consumer launch |
| **P1** | Within ~6 months post-launch (Phase 1) |
| **P2** | Year 2 / later roadmap |

---

## MVP In-Scope Requirements (P0)

### Customer (Demand)

| ID | Requirement | PRD epic | Acceptance hook |
|----|-------------|----------|-----------------|
| BR-C01 | Request help &lt;60s with location, vehicle, issue | E2 | US-C03 |
| BR-C02 | Up to 3 offers within 5 minutes | E3 | US-C06, SLA-C1 |
| BR-C03 | Compare ETA, price, rating, credentials | E3 | US-C06 |
| BR-C04 | Track provider en route | E4 | US-C08 |
| BR-C05 | Digital pay on completion | E5 | US-C10 |
| BR-C06 | Rate provider after completion | E6 | US-C11 |
| BR-C07 | Support / disputes within policy windows | E6 | US-C12 |
| BR-C08 | Arabic + English parity | E9 | US-SYS03 |

### Provider (Supply)

| ID | Requirement | PRD epic | Acceptance hook |
|----|-------------|----------|-----------------|
| BR-P01 | Verification before offers | E7 | US-P06, US-O02 |
| BR-P02 | Explicit accept/decline of offers | E3 | US-P02 |
| BR-P03 | Payout within 48 hours | E5 | US-P04 |
| BR-P04 | Availability + service zone controls | E1/E7 | US-P01 |
| BR-P05 | Job history + earnings | E5 | US-P04 |
| BR-P06 | Public rating profile | E6 | US-C11 |
| BR-P07 | Non-exclusive independence | Legal + product copy | Rule 9–10 |
| BR-P08 | Bilingual provider support | E6/E9 | Support model |

### Marketplace Operations

| ID | Requirement | PRD epic | Acceptance hook |
|----|-------------|----------|-----------------|
| BR-M01 | Match nearest qualified available | E3 | US-SYS01 |
| BR-M02 | Top-3 offer round before expiry | E3 | US-C06 |
| BR-M03 | Full lifecycle audit trail | E4 | Job State Machine |
| BR-M04 | Dispute mediation process | E6 | US-C12 + Ops |
| BR-M05 | Min provider density launch zone | Launch ops | ≥150 providers |
| BR-M08 | Geo-gate service by zone | E9 | US-SYS04 |
| BR-M09 | Cancellation fee rules enforced | E4 | US-C09 |

**Note:** BR-M07 (ops dashboard) is P1 in master BR list but **elevated to P0 for MVP** per MVP scope (operations dashboard + manual dispatch). Tracked as BR-M07-MVP under E8.

### Financial

| ID | Requirement | PRD epic |
|----|-------------|----------|
| BR-F01 | Auto commission on completed jobs | E5 |
| BR-F02 | AED primary currency | E5 |
| BR-F03 | Dispute / guarantee fund process | Ops + Finance (process may be manual at MVP) |

### Trust & Compliance

| ID | Requirement | PRD epic |
|----|-------------|----------|
| BR-T01 | License, insurance, identity verified | E7 |
| BR-T02 | Intermediary positioning in terms | Legal |
| BR-T03 | UAE PDPL-aligned data handling | E1 + Security |
| BR-T04 | Insurance expiry monitoring / suspend | E7 |
| BR-T06 | Driver background checks before activation | E7 |

---

## Explicitly Deferred (Not in MVP Build)

| ID | Requirement | Target phase |
|----|-------------|--------------|
| BR-C09 | Additional categories (tire, fuel, mechanic…) | Phase 1 |
| BR-C10 | Share live trip with contact | Phase 1 |
| BR-C11 | Coverage map pre-request (nice-to-have; basic waitlist OK at MVP) | Phase 1 polish |
| BR-C12 | 12-month history UX | Phase 2 |
| BR-P09 | Surge incentive bonuses (auto) | Phase 1 |
| BR-P10 | Provider premium subscription | Phase 2 |
| BR-P11 | Large multi-vehicle fleets beyond 5 | Phase 2 |
| BR-M06 | Automated surge pricing | Phase 1 |
| BR-M10 | Automated monthly health report | Phase 1 |
| BR-B01–B06 | All B2B partner requirements | Phase 1 |
| BR-F04–F06 | Tax packs, promo engine scale, long-term unit econ | Phase 1+ |
| BR-T05 | Regulatory audit export automation | Phase 1 |

---

## Business Constraints (Hard)

From [Constraints](../04-Business/Constraints.md) and strategy docs — must not be violated in delivery:

1. **Marketplace only** — no owned fleet features or fleet-ops UX implying employment
2. **No cash payments** on-platform
3. **No B2C auto-assign** without customer offer choice
4. **Commission default 18%** unless promo flag
5. **Intermediary liability posture** — product copy and flows must not imply Salik performs the roadside service

---

## Traceability Summary

| Layer | Artifact |
|-------|----------|
| Strategy | Vision, Mission, Objectives, Success Metrics |
| Business | Business Requirements, Business Rules, BMC |
| Delivery BRD | This document |
| Product | [PRD](./PRD.md) |
| Software | [SRS](../12-Engineering/SRS.md) |
| Launch | [Launch Readiness Checklist](../14-Launch/Launch-Readiness-Checklist.md) |

Every P0 row above must map to at least one PRD story with testable acceptance criteria before sprint planning closes.

---

## Sign-off Checklist

| Role | Signs for | Status |
|------|-----------|--------|
| Product | Scope freeze MVP | Pending |
| Operations | Manual dispatch + support model | Pending (O2/O3 open) |
| Legal | Terms intermediary + PDPL | Pending (L1/L5/L6 open) |
| Finance | Take rate + payout T+2 | Pending |
| Engineering | Feasibility of P0 NFRs | Pending |

---

## Next Steps

1. Product + Eng review PRD/BRD in kickoff workshop
2. Close Block Launch decisions in [Block-Launch Decisions](../14-Launch/Block-Launch-Decisions.md)
3. Slice Jira/Linear epics E1–E10 from PRD
4. Begin SRS and API contract freeze
