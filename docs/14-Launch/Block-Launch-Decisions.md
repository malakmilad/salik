# Block-Launch Decisions — Salik Assist MVP

| Field | Value |
|-------|-------|
| **Version** | 1.0 |
| **Status** | Open |
| **Author** | Leadership / Product |
| **Last Updated** | November 5, 2026 |

## Purpose

Track the 8 Block Launch questions from [Open Questions](../10-Appendix/Open-Questions.md) with decision slots so engineering and ops are not blocked by ambiguity at W0.

**Rule:** Engineering may proceed on scaffolding now; production public launch cannot proceed while any row below remains `Open` without an explicit waiver.

---

## Decision Log

| ID | Question | Owner | Decision | Date | Status |
|----|----------|-------|----------|------|--------|
| S1 | Final brand: "Salik Assist" vs independent name? | CEO | _TBD_ | | Open |
| O2 | Dedicated ops shift 11 PM–6 AM? | Ops | _TBD_ | | Open |
| O3 | 24/7 full support from launch or phased on-call? | Ops | _TBD_ | | Open |
| L1 | Entity: mainland Dubai vs DIFC vs ADGM? | Legal | _TBD_ | | Open |
| L5 | DPO internal vs outsourced? | Legal | _TBD_ | | Open |
| L6 | Privacy Impact Assessment before launch? | Legal | _TBD_ | | Open |
| — | _(From register: ensure remaining Block Launch IDs synced)_ | | | | |

### Additional high-impact (treat as Soft-launch blockers if unresolved)

| ID | Question | Owner | Decision | Status |
|----|----------|-------|----------|--------|
| S2 | Co-brand with Salik toll entity? | CEO/Marketing | _TBD_ | Open |
| P1 | Soft launch invite-only or immediate public? | Growth | **Recommend: invite-only** | Proposed |
| PR2 | Exclusive vs non-exclusive at launch? | Legal/Ops | **Recommend: non-exclusive (Rule 10)** | Proposed |

---

## Recommended Defaults (until leadership overrides)

Use these so build is not idle:

1. **Brand:** Continue shipping as **Salik Assist** in code/bundle ids pending S1
2. **Soft launch:** Invite-only (`soft_launch_invite_only=true`)
3. **Support:** Phased — 6 AM–11 PM staffed; overnight on-call (matches MVP ops table)
4. **Providers:** Non-exclusive
5. **Cancellation fees:** [Cancellation Policy](../06-Operations/Cancellation-Policy.md) table (not older Rule 41–43 variants)

---

## Next Steps

1. Schedule leadership session for S1 + L1 within 2 weeks
2. Ops write overnight roster proposal for O2/O3
3. Legal kick off L5/L6 with counsel
4. Update this table and mark [Launch Readiness Checklist](./Launch-Readiness-Checklist.md) section A
