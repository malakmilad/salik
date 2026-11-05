# Customer Journey — Salik Assist

| Field | Value |
|-------|-------|
| **Version** | 1.0 |
| **Status** | Draft |
| **Author** | Product & Strategy Team |
| **Last Updated** | July 4, 2026 |

## Purpose

Map the end-to-end customer journey for Salik Assist—from pre-need awareness through post-service loyalty—identifying touchpoints, emotions, moments of truth, and business opportunities at each stage for both B2C motorists and B2B institutional customers.

## Scope

Covers demand-side journey (motorists and institutional buyers). Provider journey is referenced where it intersects customer experience. Excludes technical workflows, API sequences, and system state diagrams.

## Related Documents

- [Personas](./Personas.md)
- [Customer Segments](./Customer-Segments.md)
- [Pain Points](./Pain-Points.md)
- [Market Research](./Market-Research.md)
- [Go-To-Market](../05-Product-Strategy/Go-To-Market.md)
- [User Flows](../09-UX/User-Flows.md)
- [Success Metrics](../01-Executive/Success-Metrics.md)

## Table of Contents

1. [Journey Overview](#journey-overview)
2. [Journey Stages Framework](#journey-stages-framework)
3. [B2C Motorist Journey](#b2c-motorist-journey)
4. [B2B Institutional Journey](#b2b-institutional-journey)
5. [Emergency Journey (High-Urgency)](#emergency-journey-high-urgency)
6. [Provider Intersection Points](#provider-intersection-points)
7. [Emotional Journey Map](#emotional-journey-map)
8. [Moments of Truth](#moments-of-truth)
9. [Channel Touchpoints](#channel-touchpoints)
10. [Metrics by Stage](#metrics-by-stage)
11. [Business Examples](#business-examples)
12. [Business Decisions](#business-decisions)
13. [Risks](#risks)
14. [Assumptions](#assumptions)
15. [Open Questions](#open-questions)
16. [Next Steps](#next-steps)

---

## Journey Overview

The Salik Assist customer journey is non-linear for most of the year (latent) and intensely linear during a breakdown event (active). The platform must win at two distinct moments: **pre-need brand registration** (so the app is on the phone before crisis) and **in-need execution** (so the first request succeeds flawlessly).

### Journey Types

| Journey | Trigger | Frequency | Duration |
|---------|---------|-----------|----------|
| B2C first-time emergency | Breakdown | Once (then repeat potential) | 30–90 minutes |
| B2C repeat user | Breakdown | 0.8–1.2×/year | 20–60 minutes |
| B2B2C insurer flow | Policyholder breakdown | Per policy event | 25–75 minutes |
| B2B fleet dispatch | Driver reports issue | Per fleet event | 20–60 minutes |
| B2B partnership sales | Salik sales outreach | One-time (annual renewal) | 3–9 months |

---

## Journey Stages Framework

```
AWARENESS → CONSIDERATION → REGISTRATION → PRE-NEED → TRIGGER → REQUEST → OFFERS → SELECTION →
TRACKING → SERVICE → PAYMENT → RATING → RETENTION → ADVOCACY
```

| Stage | Customer State | Business Goal |
|-------|----------------|---------------|
| Awareness | Knows roadside help exists | Brand recall in emergency context |
| Consideration | Evaluates Salik vs. alternatives | Differentiate on transparency |
| Registration | Downloads app / creates account | Minimize friction; optional deferral |
| Pre-need | App installed; no active request | Maintain top-of-mind; push referrals |
| Trigger | Breakdown occurs | Be the default action |
| Request | Submits service need | < 60 seconds to submit |
| Offers | Receives top-3 provider offers | < 5 minutes to receive offers |
| Selection | Chooses provider | Clear comparison; confident decision |
| Tracking | Waits for arrival | Anxiety reduction via live ETA |
| Service | Provider delivers | Quality execution |
| Payment | Completes transaction | Frictionless; dispute-free |
| Rating | Feedback submitted | Capture quality signal |
| Retention | Returns for next event | Loyalty; insurance of app |
| Advocacy | Refers others | Organic growth |

---

## B2C Motorist Journey

### Stage 1: Awareness

**Context:** Motorist has not experienced a breakdown recently. May have seen roadside signage, insurer materials, or social ads.

| Element | Detail |
|---------|--------|
| Touchpoints | Highway QR signage, Instagram ads, insurer co-marketing, app store search, word of mouth |
| Customer thought | "I should have something for emergencies" |
| Emotion | Low engagement; latent anxiety |
| Pain points | Doesn't think about roadside until needed; ad blindness |
| Opportunity | Highway signage at rest stops; "download before you need it" messaging |
| KPI | Brand awareness in launch corridors: 15% Year 1 |

**Persona fit:** Sarah sees Instagram ad; Raj hears colleague recommendation; Fatima sees QR on E11 rest stop.

---

### Stage 2: Consideration

**Context:** Motorist researches options after near-miss, friend’s bad experience, or ad click.

| Element | Detail |
|---------|--------|
| Touchpoints | App store listing, website, reviews, comparison with insurer hotline |
| Customer thought | "Is this better than calling my insurance?" |
| Emotion | Mild urgency; skepticism |
| Pain points | Unknown brand trust; "another app?" fatigue |
| Opportunity | Reviews, insurer endorsement, "top-3 offers" differentiation |
| KPI | App store conversion rate: 25%+ |

---

### Stage 3: Registration

**Context:** Motorist downloads app. Account creation may be deferred until first request.

| Element | Detail |
|---------|--------|
| Touchpoints | App install, onboarding screens, vehicle profile (optional) |
| Customer thought | "Let me set this up so I'm ready" |
| Emotion | Preparedness; mild friction tolerance |
| Pain points | Too many fields; payment setup before needed |
| Opportunity | Minimal onboarding; register vehicle optionally; guest request path |
| KPI | Install-to-registration: 60%+ |

---

### Stage 4: Pre-Need (Idle)

**Context:** App installed; no breakdown. Days to months pass.

| Element | Detail |
|---------|--------|
| Touchpoints | Push notifications (sparingly), seasonal reminders, referral prompts |
| Customer thought | "Hope I don't need this" |
| Emotion | Neutral; app forgotten in folder |
| Pain points | Notification fatigue; app deletion risk |
| Opportunity | Summer battery reminder; referral incentive; insurance linking |
| KPI | 90-day retention (app installed): 40%+ |

---

### Stage 5: Trigger (Breakdown Event)

**Context:** Vehicle won't start, flat tire, accident, empty fuel, overheating. Stress peaks.

| Element | Detail |
|---------|--------|
| Touchpoints | Memory of app; home screen; Siri/voice search; highway QR scan |
| Customer thought | "I need help NOW" |
| Emotion | Anxiety, fear (highway), frustration |
| Pain points | Panic reduces rational choice; may revert to calling someone |
| Opportunity | One-tap emergency button; auto-location; calm UX copy |
| KPI | Salik Assist as first action (vs. call insurer/friend): 35%+ by Year 2 |

**Moment of Truth #1:** Customer opens Salik Assist instead of calling insurer or random tow number.

---

### Stage 6: Request Submission

**Context:** Customer describes need and location.

| Element | Detail |
|---------|--------|
| Touchpoints | Service category selection, GPS location, vehicle info, issue description |
| Customer thought | "Did I explain it right? Will someone come?" |
| Emotion | Impatience; hope |
| Pain points | Complex forms in stress; wrong category selection |
| Opportunity | Auto-detect location; smart category suggestion; photo upload |
| KPI | Request completion time: < 60 seconds (median) |

---

### Stage 7: Offers Received (Top-3 Model)

**Context:** Platform matches nearby verified providers; up to 3 submit offers.

| Element | Detail |
|---------|--------|
| Touchpoints | Offer cards showing ETA, price estimate, rating, provider name |
| Customer thought | "Which one should I pick?" |
| Emotion | Relief (offers arrived); decision pressure |
| Pain points | No offers (supply gap); too-slow offers; confusing pricing |
| Opportunity | Highlight recommended option; show "fastest" and "best value" tags |
| KPI | Top-3 offers within 5 minutes: 85%+; median time: 3 minutes |

**Moment of Truth #2:** Customer receives 3 credible offers faster than insurer hotline would assign one provider.

---

### Stage 8: Selection

**Context:** Customer compares and accepts one offer.

| Element | Detail |
|---------|--------|
| Touchpoints | Offer comparison, accept button, confirmation screen |
| Customer thought | "Good choice? What if they don't show?" |
| Emotion | Cautious commitment |
| Pain points | Price changes on arrival; provider cancels |
| Opportunity | Locked price guarantee; provider commitment penalty |
| KPI | Offer acceptance rate: 90%+ (of those who receive offers) |

---

### Stage 9: Tracking

**Context:** Provider en route. Customer waits—often in unsafe or uncomfortable location.

| Element | Detail |
|---------|--------|
| Touchpoints | Live map, ETA updates, provider photo/vehicle, in-app chat/call |
| Customer thought | "Where are they? How much longer?" |
| Emotion | Anxiety decreasing with visibility |
| Pain points | ETA drift; no communication; can't share status with family |
| Opportunity | Share-my-ride link for family; proactive delay notifications |
| KPI | Customer anxiety score (post-job survey): ≤ 3/10 |

**Moment of Truth #3:** Provider arrives within promised ETA window (±5 minutes).

---

### Stage 10: Service Delivery

**Context:** Provider arrives and performs tow, battery, tire, or other service.

| Element | Detail |
|---------|--------|
| Touchpoints | Provider arrival notification, in-person interaction, service execution |
| Customer thought | "Are they professional? Will they damage my car?" |
| Emotion | Relief (arrival); evaluation (service quality) |
| Pain points | Unprofessional behavior; upselling; damage |
| Opportunity | Verified badge visible; service scope confirmation; photo documentation |
| KPI | Service completion rate: 97%+ |

---

### Stage 11: Payment

**Context:** Service complete. Customer pays.

| Element | Detail |
|---------|--------|
| Touchpoints | In-app payment, receipt, insurance coverage application |
| Customer thought | "Is this the price I was quoted?" |
| Emotion | Relief or anger (if price differs) |
| Pain points | Price dispute; cash demand from provider; receipt delay |
| Opportunity | Pre-authorized estimate; instant digital receipt; insurance direct billing |
| KPI | Payment dispute rate: < 2% |

---

### Stage 12: Rating & Feedback

**Context:** Customer rates provider and overall experience.

| Element | Detail |
|---------|--------|
| Touchpoints | Star rating, optional comment, issue report |
| Customer thought | "That went well—I should rate them" |
| Emotion | Gratitude (good) or frustration (bad) |
| Pain points | Lengthy survey; no response to complaints |
| Opportunity | Two-tap rating; immediate dispute escalation path |
| KPI | Rating completion rate: 70%+ |

---

### Stage 13: Retention

**Context:** Customer retains app for future events.

| Element | Detail |
|---------|--------|
| Touchpoints | Thank-you message, referral offer, insurance link reminder |
| Customer thought | "I'll keep this app for next time" |
| Emotion | Satisfaction; preparedness |
| Pain points | App deleted after single use |
| Opportunity | Referral credit; annual "you're covered" reminder |
| KPI | Repeat user rate (2+ jobs in 24 months): 25%+ |

---

### Stage 14: Advocacy

**Context:** Customer recommends Salik Assist to others.

| Element | Detail |
|---------|--------|
| Touchpoints | Referral link, social share, word of mouth |
| Customer thought | "My friend should have this" |
| Emotion | Enthusiasm |
| Pain points | No incentive to refer |
| Opportunity | Referral bonus (AED 25 credit both sides) |
| KPI | NPS: 45+; referral rate: 15% of completed jobs |

---

## B2B Institutional Journey

### Insurer Partnership Journey (Noura Persona)

| Stage | Activity | Duration | Salik Assist Role |
|-------|----------|----------|-------------------|
| Discovery | Insurer identifies assistance gap | Ongoing | Industry content, referrals |
| Evaluation | RFP or pilot proposal | 4–8 weeks | ROI model, network demo |
| Pilot | Limited policyholder rollout | 8–12 weeks | White-label dispatch, reporting |
| Contract | Annual agreement | 2–4 weeks | SLA, pricing, compliance |
| Integration | App/embed launch | 4–8 weeks | Co-branded experience |
| Operations | Ongoing dispatch | Continuous | Quality monitoring, QBRs |
| Renewal | Annual review | 2–4 weeks | Performance report, upsell |

**B2B Moment of Truth:** Pilot achieves < 15-minute dispatch time vs. 45-minute baseline.

---

### Fleet Partnership Journey (Khalid Persona)

| Stage | Activity | Duration |
|-------|----------|----------|
| Pain recognition | Fleet downtime costs escalate | — |
| Vendor search | Google, referral, Salik sales outreach | 2–4 weeks |
| Pilot | 30-day trial with 10–20 vehicles | 4 weeks |
| Contract | Annual SLA agreement | 2–4 weeks |
| Driver rollout | Training, app distribution | 2 weeks |
| Operations | Ongoing dispatch + reporting | Continuous |

---

## Emergency Journey (High-Urgency)

For highway and safety-critical events (Fatima persona), the journey compresses:

| Standard Stage | Emergency Compression |
|----------------|----------------------|
| Awareness/Registration | Pre-installed app assumed |
| Request | One-tap emergency with auto-location |
| Offers | Fastest ETA highlighted; auto-sort by speed |
| Selection | "Recommended fastest" pre-highlighted |
| Tracking | Share location with emergency contact auto-prompt |
| Payment | Deferred if insurer-covered; speed priority |

**Target emergency journey time:** Request to provider arrival < 25 minutes (highway, Dubai corridor).

---

## Provider Intersection Points

Customer journey quality depends on provider journey execution at these intersection points:

| Customer Stage | Provider Action | Failure Impact |
|----------------|-----------------|----------------|
| Offers | Provider submits competitive offer quickly | Customer receives < 3 offers |
| Selection | Provider commits without cancel | Customer stranded |
| Tracking | Provider shares live location | Customer anxiety spikes |
| Service | Professional execution | Bad rating; churn |
| Payment | Accepts platform payment | Dispute; trust damage |

---

## Emotional Journey Map

```
Emotion
  ^
  |     Anxiety ████████████
  |          ╲        ╱ Relief ████████
  |           ╲      ╱           ╲ Satisfaction
  |            ╲    ╱             ╲████
  |  Neutral    ╲██/  Anticipation  ╲
  |  ────────────╱╲──────────────────────────► Time
  |           Trigger  Offers  Service  Rating
```

**Design principle:** Reduce anxiety fastest at Trigger → Offers → Tracking stages. These three stages determine NPS more than payment or rating.

---

## Moments of Truth

| # | Moment | Success Criteria | Failure Consequence |
|---|--------|------------------|---------------------|
| 1 | App opened in emergency | Customer chooses Salik over alternatives | Revert to informal/insurer; brand lost |
| 2 | Top-3 offers received < 5 min | 3 credible offers with clear pricing | Customer abandons; calls tow directly |
| 3 | Provider arrives on time | Within ETA ± 5 min | 1-star rating; social media complaint |
| 4 | Price matches estimate | Final ≤ 110% of quoted estimate | Dispute; chargeback; trust destroyed |
| 5 | First job completed successfully | 4+ star rating | Customer deletes app; negative word of mouth |

---

## Channel Touchpoints

| Stage | Digital | Physical | Human |
|-------|---------|----------|-------|
| Awareness | Social ads, SEO | Highway QR, signage | Word of mouth |
| Consideration | App store, website | — | Friend recommendation |
| Registration | App onboarding | — | — |
| Trigger | App push, home screen | Highway QR scan | Call from passenger |
| Request–Payment | In-app full flow | Provider in-person | Provider phone call |
| Retention | Push, email | — | — |
| Advocacy | Referral link | — | Social sharing |

---

## Metrics by Stage

| Stage | Primary Metric | Year 1 Target |
|-------|----------------|---------------|
| Awareness | Aided recall (launch corridors) | 15% |
| Registration | Monthly app installs | 25,000 |
| Trigger → Request | Conversion rate | 70% |
| Request → Offers | Offer fulfillment rate | 85% |
| Offers → Selection | Acceptance rate | 90% |
| Selection → Service | Completion rate | 97% |
| Service → Payment | Dispute-free rate | 98% |
| Payment → Rating | Rating completion | 70% |
| Rating → Retention | 90-day app retention | 40% |
| Retention → Advocacy | NPS | 45+ |

---

## Business Examples

**Example 1 — Sarah's journey:** Sarah's battery dies in DIFC parking. Opens Salik Assist (pre-installed from Instagram ad). Submits request in 40 seconds. Receives 3 offers in 2.5 minutes. Selects fastest (18 min ETA, AED 165). Tracks arrival. Pays in-app. Rates 5 stars. Refers colleague.

**Example 2 — Raj's failed journey (risk case):** Raj's car breaks down. Opens Salik Assist. Only 1 offer received (supply gap in zone). Waits 8 minutes; no additional offers. Calls informal tow. **Lesson:** Supply density is journey-critical at Offers stage.

**Example 3 — Noura B2B2C journey:** Insurer policyholder taps "Roadside Help." Request routes to Salik network. Policyholder sees co-branded experience. Provider assigned in 12 minutes. Insurer billed per dispatch. Noura reviews monthly SLA dashboard.

---

## Business Decisions

| Decision | Journey Impact |
|----------|----------------|
| Allow guest request (no pre-registration) | Reduces Trigger → Request friction |
| Top-3 offers (not auto-assign) | Strengthens Offers → Selection confidence |
| Pre-install marketing ("download before you need it") | Improves Trigger conversion |
| Highway QR signage | Captures Trigger at point of need |
| Locked price estimate | Protects Payment moment of truth |
| Referral incentive post-rating | Drives Advocacy stage |

---

## Risks

| Risk | Journey Stage | Mitigation |
|------|---------------|------------|
| Supply gap → < 3 offers | Offers | Zone gating; surge provider incentives |
| Customer reverts to insurer hotline | Trigger | Insurer co-marketing; speed superiority |
| Provider no-show | Tracking → Service | Backup provider auto-offer; penalty |
| Price dispute | Payment | Locked estimate; photo documentation |
| App not installed at trigger | Trigger | Highway QR → mobile web fallback |
| B2B pilot failure | B2B Evaluation | Conservative SLA promises; white-glove pilot |

---

## Assumptions

- 30% of Year 1 users pre-install app before first breakdown (vs. 70% install at trigger)
- Median request-to-offer time achievable at 3 minutes with 150+ providers in corridor
- Customers compare up to 3 offers; more than 3 creates choice paralysis
- B2B2C journey removes Payment friction for insured events
- Provider behavior at intersection points is trainable via incentives and penalties

---

## Open Questions

- Should emergency journey auto-select fastest provider (override top-3 choice) for highway critical events?
- Is guest request (no account) sufficient or does it reduce retention?
- What is acceptable offer wait time before customer abandons (5 min? 8 min?)?
- Should family location-sharing be automatic or opt-in for privacy?
- How does B2B fleet journey differ when driver doesn't speak English?

---

## Next Steps

1. Validate journey timing assumptions with provider simulation exercises
2. Map journey stages to success metrics in [Success Metrics](../01-Executive/Success-Metrics.md)
3. Design highway QR → app install → pre-registration funnel
4. Define provider SLAs at each intersection point
5. Conduct journey walkthroughs with 5 personas in usability sessions (Q3 2026)
