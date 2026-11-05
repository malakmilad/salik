# Launch Readiness Checklist — Salik Assist MVP

| Field | Value |
|-------|-------|
| **Version** | 1.0 |
| **Status** | Draft |
| **Author** | Product, Ops, Engineering |
| **Last Updated** | November 5, 2026 |

## Purpose

Single go-live checklist combining MVP launch criteria, technical gates, and block-launch decisions.

## How to use

Mark each item `☐` → `☑` with owner and date. Soft launch requires all **Soft** items. Public W0 requires **Soft + Public**.

---

## A. Decisions (Block Launch)

See [Block-Launch Decisions](./Block-Launch-Decisions.md).

| ID | Item | Soft | Public |
|----|------|------|--------|
| S1 | Final brand naming | ☑ required | ☑ |
| L1 | Legal entity structure | ☑ | ☑ |
| L5 | DPO appointed | ☐ preferred | ☑ |
| L6 | Privacy Impact Assessment | ☐ preferred | ☑ |
| O2 | Overnight ops coverage model | ☑ | ☑ |
| O3 | Support 24/7 vs phased on-call | ☑ | ☑ |

---

## B. Supply & Ops (from MVP)

| # | Criterion | Threshold | Soft | Public |
|---|-----------|-----------|------|--------|
| 1 | Verified active providers | ≥150 (soft may start ≥80 with capped geo) | ☐ | ☑ ≥150 |
| 2 | Zone coverage | 90% launch zone ≥3 providers / 15 km | ☐ | ☑ |
| 3 | E2E test jobs | ≥50 | ☑ | ☑ |
| 4 | Support staffed & trained | Per O3 decision | ☑ | ☑ |
| 5 | Policies published in-app | Cancel, refund, SLA summary | ☑ | ☑ |
| 6 | Legal templates approved | ToS, Privacy, Provider Agreement | ☑ | ☑ |
| 7 | Mystery shop | ≥10 | ☐ | ☑ |
| 8 | Escalation drill | Pass | ☑ | ☑ |
| 9 | Manual dispatch SOP | Tabletop + staging drill | ☑ | ☑ |

---

## C. Product & Engineering

| # | Item | Soft | Public |
|---|------|------|--------|
| 1 | PRD P0 stories accepted | ☑ | ☑ |
| 2 | State machine + fees tested | ☑ | ☑ |
| 3 | Payment sandbox → live switch runbook | ☑ sandbox | ☑ live |
| 4 | Test Plan must-pass scenarios green | ☑ | ☑ |
| 5 | Observability dashboards live | ☑ | ☑ |
| 6 | Feature flags configured | ☑ | ☑ |
| 7 | iOS + Android store builds | Internal | ☑ Approved |
| 8 | Bilingual AR/EN core flows | ☑ | ☑ |
| 9 | Geo fence production data loaded | ☑ | ☑ |
| 10 | Backup / restore verified on staging | ☐ | ☑ |

---

## D. Commercial

| # | Item | Soft | Public |
|---|------|------|--------|
| 1 | Take rate 18% configured | ☑ | ☑ |
| 2 | Zero-commission promo rules (if used) | ☑ | ☑ |
| 3 | Payout T+2 pathway tested | ☑ | ☑ |
| 4 | Service credit issuance path | ☑ | ☑ |

---

## E. Go / No-Go Meeting

| Checkpoint | Timing | Decision |
|------------|--------|----------|
| Soft launch | W-1 | Invite-only live? |
| Public launch | W0 | Open stores + marketing? |
| Day 30 | W+4 | Ops/product review |
| Day 90 | W+12 | Phase 1 go/no-go per MVP metrics |

**Public launch requires:** all Public columns ☑, no open P0 bugs, on-call roster named.
