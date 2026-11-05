# MVP — Salik Assist

| Field | Value |
|-------|-------|
| **Version** | 1.0 |
| **Status** | Draft |
| **Author** | Product & Strategy Team |
| **Last Updated** | July 4, 2026 |

## Purpose

Define the Minimum Viable Product (MVP) scope for Salik Assist—the smallest market-ready version that validates the core marketplace hypothesis: customers will choose transparent, verified roadside assistance over informal alternatives.

## Scope

Business features, geographic scope, service categories, provider/customer requirements, and success criteria for MVP launch. Excludes technical specifications, post-MVP features, and expansion markets.

## Related Documents

- [Phase 1](./Phase-1.md)
- [Product Roadmap](./Product-Roadmap.md)
- [Operations Workflow](../06-Operations/Operations-Workflow.md)
- [Provider Onboarding](../06-Operations/Provider-Onboarding.md)
- [Revenue Forecast](../08-Finance/Revenue-Forecast.md)
- [Executive Summary](../01-Executive/Executive-Summary.md)

## Table of Contents

1. [MVP Vision](#mvp-vision)
2. [Core Hypothesis](#core-hypothesis)
3. [MVP Scope: In / Out](#mvp-scope-in--out)
4. [Geographic Scope](#geographic-scope)
5. [Service Categories](#service-categories)
6. [Customer Experience (MVP)](#customer-experience-mvp)
7. [Provider Experience (MVP)](#provider-experience-mvp)
8. [Operations Readiness](#operations-readiness)
9. [Launch Criteria](#launch-criteria)
10. [MVP Success Metrics](#mvp-success-metrics)
11. [Timeline & Milestones](#timeline--milestones)
12. [Business Examples](#business-examples)
13. [Business Decisions](#business-decisions)
14. [Risks](#risks)
15. [Assumptions](#assumptions)
16. [Open Questions](#open-questions)
17. [Next Steps](#next-steps)

---

## MVP Vision

Launch a working two-sided marketplace in Dubai where a stranded motorist can receive three verified provider offers within 5 minutes, track arrival, pay securely, and rate the experience—proving the model before scaling categories, geography, or B2B channels.

**MVP tagline:** *Help on the road, on demand — Dubai.*

---

## Core Hypothesis

| Hypothesis | Validation Criteria |
|------------|---------------------|
| Customers prefer top-3 offers over calling unknown tow numbers | ≥70% offer acceptance rate when 2+ offers received |
| Verified providers attract customer trust | ≥80% customers select verified badge provider when priced within 10% |
| Providers accept 18% commission for qualified demand | ≥70% of onboarded providers remain active after promo period |
| 150 providers sufficient for Dubai launch density | ≤5 min P90 time-to-first-offer in launch zone |
| Emergency guest checkout converts to registered users | ≥40% guest-to-registered conversion |

---

## MVP Scope: In / Out

### In Scope (MVP)

| Area | Included |
|------|----------|
| Customer app (iOS + Android) | Request, offers, tracking, payment, rating |
| Provider app (iOS + Android) | Offers, navigation, status updates, earnings |
| Service categories | Tow, battery jump/replacement |
| Top-3 offer model | Competitive offers with ETA and price |
| Guest checkout | Mobile OTP; 2 jobs before registration required |
| Payment | Card, Apple Pay; charge on completion |
| Provider verification | Tier 1 standard verification |
| Customer support | Phone + chat (peak hours) |
| Operations dashboard | Job monitoring, manual dispatch fallback |
| Arabic + English | Full bilingual support |
| Basic ops policies | Cancellation, refund, SLA, escalation |

### Out of Scope (Post-MVP → Phase 1)

| Area | Deferred To |
|------|-------------|
| Tire, fuel, mobile mechanic, lockout | Phase 1 |
| B2B / insurance integration | Phase 1 |
| Provider subscriptions (Pro/Premium) | Phase 1 |
| Abu Dhabi, Sharjah | Phase 1 |
| Subscription product for customers | Phase 2 |
| Surge pricing (manual only at MVP if needed) | Phase 1 |
| WhatsApp request channel | Phase 1 |
| Web app (desktop) | Phase 1 |
| Tipping | Phase 1 |
| Scheduled (non-emergency) requests | Phase 2 |
| KSA expansion | Phase 3 |

---

## Geographic Scope

### Launch Zone (MVP)

| Zone | Coverage | Rationale |
|------|----------|-----------|
| Dubai Metro | Business Bay, DIFC, Marina, JLT, Deira, Bur Dubai, Al Quoz | High vehicle density |
| E11 (Sheikh Zayed Road) | Full corridor Dubai segment | Highest breakdown frequency |
| E311 (Mohammed bin Zayed Road) | Dubai segment | Commuter/highway demand |
| E611 (Emirates Road) | Dubai segment | Logistics/tow demand |
| Dubai International Airport vicinity | 5 km radius | Tourist/rental car demand |

**Out of zone at MVP:** Abu Dhabi, Sharjah, desert interior, Hatta, Al Ain.

**Fallback:** Out-of-zone requests receive "Coming soon to your area" with option to join waitlist.

---

## Service Categories

### Tow / Recovery (Primary — 55% of MVP volume target)

- Flatbed and wheel-lift tow
- Short-distance (≤30 km) and medium-distance (≤80 km)
- Highway and urban pickup
- Drop-off at customer-specified garage or nearest safe location

### Battery (Secondary — 45% of MVP volume target)

- Jump-start
- Battery replacement (provider-supplied battery)
- 30-day warranty on replacements (provider responsibility)

**Rationale:** Tow and battery represent ~70% of roadside assistance demand in UAE climate (heat → battery failure; highway → tow demand).

---

## Customer Experience (MVP)

| Step | MVP Feature |
|------|-------------|
| 1. Open app | iOS/Android; optional guest mode |
| 2. Location | Auto-GPS or pin drop |
| 3. Select service | Tow or Battery |
| 4. Vehicle info | Type (sedan/SUV/commercial); optional plate |
| 5. Submit request | See price estimate range |
| 6. Receive offers | Up to 3; ETA, price, rating, verified badge |
| 7. Accept offer | 3-minute grace cancel (free) |
| 8. Track provider | Map tracking en route |
| 9. Service delivery | Provider updates status |
| 10. Payment | Auto-charge saved card on completion |
| 11. Rate | 1–5 stars + optional comment |
| 12. Support | In-app chat + phone hotline |

**Not in MVP customer experience:** Schedule ahead, multiple vehicles saved (limited to 1), subscription, insurance link, tipping, WhatsApp.

---

## Provider Experience (MVP)

| Feature | MVP |
|---------|-----|
| Receive offer invitations | ✓ (90-second response window) |
| Submit offer (ETA + price) | ✓ |
| Accept assigned job | ✓ |
| Status updates (en route, arrived, complete) | ✓ |
| Navigation to customer | ✓ (external maps link) |
| Earnings dashboard | ✓ (basic: daily/weekly) |
| Payout tracking | ✓ (T+2) |
| Performance score | ✓ (basic SPS) |
| Training completion | ✓ (required before activation) |
| Multi-vehicle management | ✓ (up to 5 vehicles) |
| B2B job pool | ✗ (Phase 1) |
| Subscription tier | ✗ (Phase 1) |

---

## Operations Readiness

| Requirement | MVP Target |
|-------------|------------|
| Verified providers activated | 150 minimum |
| Onboarding team trained | 3 specialists |
| Support team trained | 4 agents + 1 supervisor |
| Ops shift coverage | 6 AM – 11 PM (peak); on-call overnight |
| Policies documented | Cancellation, refund, SLA, escalation |
| Manual dispatch SOP | Tested via tabletop exercise |
| Provider field sales | 300 leads contacted; 150 converted |
| Legal | Terms, privacy, provider agreement signed template |
| Mystery shop program | 10 jobs pre-launch |

---

## Launch Criteria

All criteria must be met before public launch:

| # | Criterion | Threshold |
|---|-----------|-----------|
| 1 | Verified active providers | ≥150 |
| 2 | Provider geographic coverage | 90% of launch zone with ≥3 providers within 15 km |
| 3 | End-to-end test jobs completed | ≥50 (internal + mystery shop) |
| 4 | Support team trained and staffed | 100% |
| 5 | Policies published | 100% |
| 6 | Legal terms approved by counsel | Sign-off |
| 7 | Payment processing live | Test + live transactions |
| 8 | SLA monitoring dashboard operational | Live |
| 9 | App store approval | iOS + Android approved |
| 10 | Escalation drill completed | Pass |

---

## MVP Success Metrics

### 90-Day Post-Launch Targets

| Metric | Target |
|--------|--------|
| Completed jobs | 8,500 (Q1 equivalent) |
| Job completion rate | ≥88% |
| Time to first offer (P90) | ≤5 minutes |
| Customer rating (avg) | ≥4.2 |
| Provider retention (active Month 3) | ≥65% of launch cohort |
| Guest-to-registered conversion | ≥40% |
| Support contact rate | ≤15% |
| No-show rate | <2% |
| NPS | ≥35 |

### Go/No-Go for Phase 1 (Day 90)

| Signal | Go | No-Go |
|--------|-----|-------|
| Monthly jobs | ≥3,000/month by Day 90 | <1,500/month |
| Completion rate | ≥85% | <80% |
| Provider retention | ≥60% | <45% |
| Unit economics | Contribution margin ≥8% | <3% |

---

## Timeline & Milestones

| Milestone | Target Week | Owner |
|-----------|-------------|-------|
| Provider pipeline 50 verified | W-8 | Field sales |
| Provider pipeline 150 verified | W-4 | Field sales |
| Internal alpha (50 test jobs) | W-3 | Ops + Product |
| App store submission | W-2 | Product |
| Soft launch (invite-only, 500 users) | W-1 | Growth |
| Public launch | W0 | GM |
| Day 30 review | W+4 | Leadership |
| Day 90 Phase 1 go/no-go | W+12 | Leadership |

*W0 = launch week (specific date TBD)*

---

## Business Examples

**Example 1 — MVP happy path:** Customer on SZR blows tire (tow needed). Opens app, guest checkout, selects tow. Three offers in 4 minutes: AED 250/22min, AED 230/28min, AED 270/18min. Selects AED 230 offer. Tracks provider. Tow completed. Pays AED 245 (highway surcharge approved). Rates 5 stars. Creates account post-job.

**Example 2 — MVP manual dispatch:** Customer in Al Barsha, 11 PM. Zero offers at 5 minutes. Ops expands radius, manually contacts backup provider. Offer secured at 7 minutes. Customer accepts. Job completes. AED 50 credit issued for delay. Root cause: provider availability gap in zone — recruitment priority.

**Example 3 — MVP provider promo:** New provider completes 20 zero-commission jobs in first 45 days. Earns AED 4,200 in job value. Commission kicks in at job 21. Provider accepts 18% — demand volume justifies cost. Remains active.

---

## Business Decisions

| Decision | Rationale |
|----------|-----------|
| Tow + battery only at MVP | Covers majority demand; limits operational complexity |
| Dubai only | Achievable provider density; focused marketing |
| Guest checkout enabled | Emergency context requires minimum friction |
| Top-3 offers (not auto-assign) | Core differentiator; must validate at MVP |
| 150 provider minimum | Modeled for ≤5 min offer SLA |
| 90-day Phase 1 gate | Sufficient data for go/no-go without over-extending |
| Manual surge (not automated) | Ops-controlled during MVP learning period |

---

## Risks

| Risk | Impact | Mitigation |
|------|--------|------------|
| Provider supply below 150 | High | Field sales blitz; zero-commission promo |
| App store rejection/delay | Medium | Submit W-4; contingency web MVP |
| Low customer awareness at launch | High | Soft launch PR; QR signage; referral program |
| SLA misses damage early reviews | High | Over-supply providers in launch zone; ops monitoring |
| Scope creep into Phase 1 features | Medium | Strict MVP scope gate; change control |

---

## Assumptions

- 8-week runway from "150 providers signed" to public launch
- Tow + battery sufficient to generate 1,800+ jobs in launch month
- Guest checkout achieves 60%+ of first-time user conversions
- iOS and Android apps pass store review within 2 weeks
- No competing marketplace launches identical model in same window

---

## Open Questions

- Soft launch invite-only or immediate public?
- Co-brand with Salik toll entity or independent brand at MVP?
- Launch marketing budget for MVP month (AED 150K vs. 300K)?
- Minimum viable provider app — native or hybrid?

---

## Next Steps

1. Confirm W0 launch date and work backward to milestone schedule
2. Accelerate provider pipeline to 150 verified (current: pre-launch)
3. Complete 50 internal test jobs by W-3
4. Submit apps to stores by W-2
5. Conduct escalation tabletop exercise by W-2
6. Execute soft launch W-1; public launch W0
