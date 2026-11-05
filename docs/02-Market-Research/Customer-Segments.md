# Customer Segments — Salik Assist

| Field | Value |
|-------|-------|
| **Version** | 1.0 |
| **Status** | Draft |
| **Author** | Product & Strategy Team |
| **Last Updated** | July 4, 2026 |

## Purpose

Define and prioritize customer segments for Salik Assist's roadside assistance marketplace, distinguishing demand-side (motorists and institutional buyers) and supply-side (service providers) segments with sizing, needs, and acquisition strategies.

## Scope

Covers B2C motorists, B2B institutional buyers (insurers, fleets, rental, dealerships), and B2B supply-side providers. Excludes technical user roles, API consumers, and system administration personas.

## Related Documents

- [Personas](./Personas.md)
- [Customer Journey](./Customer-Journey.md)
- [Pain Points](./Pain-Points.md)
- [Market Size](./Market-Size.md)
- [Market Research](./Market-Research.md)
- [Go-To-Market](../05-Product-Strategy/Go-To-Market.md)
- [Pricing Strategy](../04-Business/Pricing-Strategy.md)
- [Executive Summary](../01-Executive/Executive-Summary.md)

## Table of Contents

1. [Segmentation Framework](#segmentation-framework)
2. [Demand-Side Segments (B2C)](#demand-side-segments-b2c)
3. [Demand-Side Segments (B2B)](#demand-side-segments-b2b)
4. [Supply-Side Segments (Providers)](#supply-side-segments-providers)
5. [Segment Prioritization Matrix](#segment-prioritization-matrix)
6. [Segment Sizing](#segment-sizing)
7. [Acquisition Channels by Segment](#acquisition-channels-by-segment)
8. [Segment-Specific Value Propositions](#segment-specific-value-propositions)
9. [Business Examples](#business-examples)
10. [Business Decisions](#business-decisions)
11. [Risks](#risks)
12. [Assumptions](#assumptions)
13. [Open Questions](#open-questions)
14. [Next Steps](#next-steps)

---

## Segmentation Framework

Salik Assist serves a two-sided marketplace. Customer segmentation applies separately to **demand** (who requests assistance) and **supply** (who delivers service).

### Segmentation Dimensions

| Dimension | Application |
|-----------|-------------|
| Geography | UAE emirate, highway corridor, urban vs. suburban |
| Service need | Tow, battery, tire, fuel, mobile mechanic, emergency |
| Coverage type | Insurance-covered, out-of-pocket, fleet-covered |
| Urgency | Critical (highway), urgent, moderate |
| Demographics | Expat vs. national, tourist, fleet driver |
| Vehicle type | Sedan, SUV, luxury, commercial, EV |
| Digital behavior | App-native, app-willing, phone-preferring |

---

## Demand-Side Segments (B2C)

### Segment 1: Urban Commuters

**Profile:** Daily drivers in Dubai/Abu Dhabi metro; sedan and SUV; mix of expat and national; smartphone-native.

| Attribute | Detail |
|-----------|--------|
| Est. UAE size | 1.8M motorists |
| Event frequency | 0.7–1.0/year |
| Avg. transaction | AED 150–250 |
| Coverage | 55% insured, 45% out-of-pocket |
| Price sensitivity | Medium |
| Key need | Speed, transparency, trust |

**Salik Assist fit:** High. Core launch segment. Responds to top-3 offer model and real-time tracking.

---

### Segment 2: Highway / Inter-Emirate Travelers

**Profile:** Motorists on E11, E311, E611; higher urgency; includes commuters and travelers; safety-critical context.

| Attribute | Detail |
|-----------|--------|
| Est. UAE size | 900K active highway users (daily) |
| Event frequency | 0.3–0.5/year (per user) but high severity |
| Avg. transaction | AED 250–450 (long-distance tow) |
| Coverage | 65% insured |
| Price sensitivity | Low in critical moments |
| Key need | Fastest ETA, verified provider, location sharing |

**Salik Assist fit:** Very high. Premium pricing opportunity. Highway corridor coverage is MVP priority.

---

### Segment 3: Expat Residents (No Local Network)

**Profile:** Western, South Asian, and other expat communities; 2–10 years in UAE; limited Arabic; no established garage relationships.

| Attribute | Detail |
|-----------|--------|
| Est. UAE size | 2.2M motorists |
| Event frequency | 0.8–1.1/year |
| Avg. transaction | AED 160–280 |
| Coverage | 50% insured |
| Price sensitivity | Medium-high |
| Key need | English interface, clear pricing, no negotiation |

**Salik Assist fit:** High. Digital-first; frustrated by informal tow negotiations. Strong referral potential in community networks.

---

### Segment 4: Tourists and Visitors

**Profile:** Rental car users, hotel guests, business travelers; unfamiliar roads and providers; episodic usage.

| Attribute | Detail |
|-----------|--------|
| Est. UAE size | 15M+ annual visitors; ~30% drive |
| Event frequency | 0.2–0.4/year (per visitor driver) |
| Avg. transaction | AED 200–400 |
| Coverage | 70% via rental insurance |
| Price sensitivity | Low (expense account / insurance) |
| Key need | Immediate help, language support, rental company coordination |

**Salik Assist fit:** Medium-high. Requires rental/fleet B2B integration. High visibility for brand building.

---

### Segment 5: Luxury and Premium Vehicle Owners

**Profile:** High-value vehicles (AED 250K+); concerned about damage during tow; expect white-glove service.

| Attribute | Detail |
|-----------|--------|
| Est. UAE size | 350K vehicles |
| Event frequency | 0.5–0.8/year |
| Avg. transaction | AED 350–600 |
| Coverage | 75% insured (comprehensive) |
| Price sensitivity | Very low |
| Key need | Flatbed-only, verified handling, provider credentials |

**Salik Assist fit:** Medium. Requires premium provider tier and flatbed verification. High LTV and NPS potential.

---

### Segment 6: Budget-Conscious Motorists

**Profile:** Older vehicles; price-first decision making; may delay service or use informal providers.

| Attribute | Detail |
|-----------|--------|
| Est. UAE size | 600K motorists |
| Event frequency | 1.0–1.4/year (older vehicles) |
| Avg. transaction | AED 80–150 |
| Coverage | 35% insured |
| Price sensitivity | Very high |
| Key need | Lowest price, payment flexibility |

**Salik Assist fit:** Medium. Top-3 offer model serves price comparison. Risk of churn to informal if platform fees inflate price.

---

## Demand-Side Segments (B2B)

### Segment B1: Motor Insurers

**Profile:** UAE insurance carriers with roadside assistance as policy benefit or optional add-on.

| Attribute | Detail |
|-----------|--------|
| Est. UAE size | 25–30 active motor insurers |
| Volume potential | 120K–180K events/year (UAE) |
| Revenue model | Per-dispatch fee + platform subscription |
| Key need | Cost per event reduction, CSAT improvement, fraud reduction |

**Strategic priority:** P1. See [Executive Summary](../01-Executive/Executive-Summary.md)—25%+ volume at maturity.

---

### Segment B2: Rental Car Companies

**Profile:** Airport and metro rental fleets; breakdown = fleet downtime cost.

| Attribute | Detail |
|-----------|--------|
| Est. UAE size | 50+ operators; top 10 hold 70% fleet |
| Volume potential | 25K–40K events/year |
| Revenue model | Enterprise contract + per-event fee |
| Key need | SLA-backed response, fleet dashboard, billing integration |

**Strategic priority:** P1 for B2B. High contract value; tourist segment conduit.

---

### Segment B3: Corporate Fleets and Logistics

**Profile:** Delivery vans, corporate cars, ride-hail fleets; high daily vehicle-kilometers.

| Attribute | Detail |
|-----------|--------|
| Est. UAE size | 200K+ commercial fleet vehicles |
| Volume potential | 40K–60K events/year |
| Revenue model | Subscription + volume discount |
| Key need | Uptime, reporting, multi-vehicle dispatch |

**Strategic priority:** P2. Requires fleet management features (business roadmap).

---

### Segment B4: Car Dealerships and OEM Programs

**Profile:** Dealership service departments; OEM roadside program administration.

| Attribute | Detail |
|-----------|--------|
| Est. UAE size | 200+ dealerships |
| Volume potential | 15K–25K events/year |
| Revenue model | Referral fee or white-label |
| Key need | Brand-safe providers, customer satisfaction |

**Strategic priority:** P2. Co-marketing opportunity at point of vehicle purchase.

---

## Supply-Side Segments (Providers)

### Segment S1: Independent Tow Operators

**Profile:** 1–10 truck operations; owner-operators; Al Quoz, industrial zone based.

| Attribute | Detail |
|-----------|--------|
| Est. UAE size | 800–1,200 entities |
| Capacity utilization | 50–60% |
| Key need | Demand volume, payment guarantee, reduced idle time |
| Commission tolerance | 15–20% |

**Strategic priority:** P1. Anchor supply for MVP.

---

### Segment S2: Battery Retailers with Mobile Units

**Profile:** Battery Plus, Solite, independents; retail + mobile service.

| Attribute | Detail |
|-----------|--------|
| Est. UAE size | 200+ locations |
| Key need | Customer acquisition, inventory turnover |
| Commission tolerance | 12–18% |

**Strategic priority:** P1. Second anchor category.

---

### Segment S3: Mobile Mechanics

**Profile:** Independent technicians; semi-formal; variable quality.

| Attribute | Detail |
|-----------|--------|
| Est. UAE size | 500+ individuals/small shops |
| Key need | Job routing, reputation building |
| Commission tolerance | 15–22% |

**Strategic priority:** P2. Requires stronger verification.

---

### Segment S4: Tire Service Providers

**Profile:** Pitstop, TyrePlus, independents; mobile and shop-based.

| Attribute | Detail |
|-----------|--------|
| Est. UAE size | 150+ service points |
| Key need | Off-peak demand, mobile call-outs |
| Commission tolerance | 12–18% |

**Strategic priority:** P2. Category expansion Month 4–6.

---

### Segment S5: Fuel Delivery Services

**Profile:** Niche operators; app-based and informal.

| Attribute | Detail |
|-----------|--------|
| Est. UAE size | 30–50 operators |
| Key need | Demand aggregation |
| Commission tolerance | 18–25% |

**Strategic priority:** P3. Low volume; high urgency for retention.

---

## Segment Prioritization Matrix

| Segment | Market Size | Salik Fit | Acquisition Cost | Priority |
|---------|-------------|-----------|------------------|----------|
| Urban commuters | Large | High | Medium | **P1** |
| Highway travelers | Medium | Very High | Low (corridor QR) | **P1** |
| Expat residents | Large | High | Medium | **P1** |
| Insurers (B2B) | Medium | Very High | High (sales cycle) | **P1** |
| Tow operators (supply) | Large | High | Medium (field sales) | **P1** |
| Battery providers (supply) | Medium | High | Medium | **P1** |
| Rental companies | Small-Med | High | Medium | **P2** |
| Tourists | Medium | Medium | High (B2B dependent) | **P2** |
| Luxury owners | Small | Medium | Low | **P2** |
| Corporate fleets | Medium | Medium | High | **P2** |
| Budget motorists | Medium | Medium | Low | **P3** |
| Mobile mechanics | Medium | Medium | Medium | **P3** |

---

## Segment Sizing

| Segment | Est. Annual Events (UAE) | % of Total | Year 3 Salik Target Share |
|---------|--------------------------|------------|---------------------------|
| Urban commuters | 1,100,000 | 38% | 12% |
| Highway travelers | 420,000 | 15% | 15% |
| Expat residents | 850,000 | 30% | 10% |
| Tourists/visitors | 180,000 | 6% | 8% |
| Luxury | 120,000 | 4% | 10% |
| Budget | 210,000 | 7% | 5% |
| **B2B (insurer/fleet)** | **350,000** | **12%** | **30%** |

*B2B events overlap B2C segments; shown separately for channel planning.*

---

## Acquisition Channels by Segment

| Segment | Primary Channels | CAC Estimate |
|---------|------------------|--------------|
| Urban commuters | App store, performance marketing, referrals | $8–$14 |
| Highway travelers | Highway QR signage, Waze/Google ads | $5–$10 |
| Expat residents | Facebook/Instagram, community groups, SEO | $10–$16 |
| Insurers | Enterprise sales, industry events | $500–$2K per contract |
| Tow operators | Field sales, tow yard visits, WhatsApp outreach | $80–$150 per provider |
| Rental companies | B2B sales, airport partnerships | $1K–$5K per contract |

---

## Segment-Specific Value Propositions

| Segment | Core Message |
|---------|--------------|
| Urban commuters | "Three verified offers in minutes—pick your price and ETA" |
| Highway travelers | "Help is on the way. Share your location. Track arrival live." |
| Expat residents | "No haggling. No surprises. Roadside help in English and Arabic." |
| Insurers | "Reduce dispatch time 50%+ and improve policyholder NPS" |
| Tow operators | "More jobs. Guaranteed payment. Build your reputation." |
| Rental companies | "Get your fleet back on the road in half the time" |

---

## Business Examples

**Example 1 — Segment crossover:** An expat urban commuter (Segment 3) breaks down on Sheikh Zayed Road (Segment 2 context). Salik Assist serves both segment needs: English UI with highway-priority matching. Single product, multiple segment triggers.

**Example 2 — B2B2C flow:** An insurer (B1) policyholder (Segment 1) taps "Roadside Help" in the insurer app. Salik Assist fulfills behind the scenes. Customer segment = urban commuter; acquisition channel = B2B partnership.

**Example 3 — Supply segmentation:** A 3-truck tow operator (S1) in Al Quoz joins for tow jobs; a battery retailer (S2) joins for mobile battery calls. Marketplace aggregates heterogeneous supply to serve unified demand.

---

## Business Decisions

| Decision | Rationale |
|----------|-----------|
| Launch marketing targets Segments 1, 2, 3 simultaneously | Combined 83% of B2C events; shared product experience |
| Prioritize insurer B2B (B1) over fleet (B3) for first partnership | Higher volume; faster trust transfer to consumers |
| Recruit S1 + S2 supply first | Tow + battery = 66% of events |
| Defer luxury-specific tier to Phase 2 | Small segment; requires flatbed verification investment |
| Highway QR signage as primary Segment 2 channel | Captures high-urgency users at point of need |

---

## Risks

| Risk | Affected Segments | Mitigation |
|------|-------------------|------------|
| Insurer partnership delays | B1, all B2C (trust) | Consumer launch proceeds; insurer pitch continues |
| Provider shortage in luxury tier | Segment 5 | Phase 2; don't market premium until supply ready |
| Tourist segment requires rental B2B | Segment 4 | Defer tourist marketing until rental contract signed |
| Budget segment churns on price | Segment 6 | Top-3 model shows cheapest option; avoid hidden fees |
| Mobile mechanic quality variance | S3 | Stricter verification; phased onboarding |

---

## Assumptions

- B2C segments are not mutually exclusive; a single motorist may belong to 2–3 segments
- Insurer-covered events represent 45–55% of UAE roadside volume
- Expat residents are over-indexed on digital app adoption vs. nationals
- Provider segments S1 and S2 have sufficient capacity to serve 85K Year 1 jobs
- Tourist segment volume recovers to pre-2020 levels by 2026

---

## Open Questions

- Should nationals be targeted with Arabic-first campaigns distinct from expat messaging?
- Which insurer segment (tier 1 vs. tier 2 carriers) offers faster partnership closure?
- Is there a distinct "female motorist alone at night" sub-segment requiring safety features?
- Do corporate fleets prefer subscription or per-event pricing?
- What is the minimum viable provider count per segment (S1–S5) for category launch?

---

## Next Steps

1. Map detailed personas for P1 segments in [Personas](./Personas.md)
2. Align acquisition budget to segment CAC estimates in [Go-To-Market](../05-Product-Strategy/Go-To-Market.md)
3. Begin insurer outreach for B1 segment validation
4. Field sales campaign targeting 150 S1 + 50 S2 providers in launch corridors
5. Design segment-specific messaging for launch marketing assets
