# API Overview — Salik Assist MVP

| Field | Value |
|-------|-------|
| **Version** | 1.0 |
| **Status** | Draft |
| **Author** | Engineering |
| **Last Updated** | November 5, 2026 |

## Purpose

Define the MVP HTTP API surface. Detailed OpenAPI spec to follow; this overview freezes resource boundaries and critical endpoints for mobile/ops parallel development.

## Conventions

- Base: `/v1`
- Auth: Bearer access token (customer / provider / ops)
- Errors: `{ "code", "message", "details?" }`
- Idempotency-Key header on payment and state transitions
- Times in ISO-8601 UTC
- Money in fils or decimal AED — **pick one in OpenAPI** (recommend minor units integer)

---

## Auth

| Method | Path | Notes |
|--------|------|-------|
| POST | `/auth/otp/request` | mobile |
| POST | `/auth/otp/verify` | returns tokens; may create guest |
| POST | `/auth/register` | upgrade guest / full register |
| POST | `/auth/refresh` | |
| POST | `/auth/logout` | |

---

## Customer

| Method | Path | Notes |
|--------|------|-------|
| GET | `/me` | profile |
| PATCH | `/me` | name, locale |
| GET/POST | `/me/vehicles` | max 1 emphasized at MVP |
| GET/POST/DELETE | `/me/payment-methods` | PSP setup intent pattern |
| POST | `/coverage/check` | `{lat,lng}` → in_zone / waitlist |
| POST | `/waitlist` | out-of-zone capture |
| POST | `/jobs` | create request |
| GET | `/jobs` | history |
| GET | `/jobs/{id}` | detail + state |
| GET | `/jobs/{id}/offers` | up to 3 |
| POST | `/jobs/{id}/offers/{offerId}/accept` | |
| POST | `/jobs/{id}/cancel` | |
| POST | `/jobs/{id}/completion/confirm` | |
| POST | `/jobs/{id}/price-approval` | if over estimate band |
| GET | `/jobs/{id}/tracking` | or websocket topic |
| POST | `/jobs/{id}/ratings` | |
| POST | `/jobs/{id}/disputes` | |
| GET | `/support/channels` | phone + chat deep links |

---

## Provider

| Method | Path | Notes |
|--------|------|-------|
| GET/PATCH | `/provider/me` | availability, categories |
| POST | `/provider/onboarding/documents` | upload metadata |
| GET/POST | `/provider/vehicles` | max 5 |
| GET | `/provider/offers/inbox` | pending invites |
| POST | `/provider/offers/{id}/submit` | eta + price |
| POST | `/provider/offers/{id}/decline` | |
| GET | `/provider/jobs/{id}` | |
| POST | `/provider/jobs/{id}/ack` | after assign |
| POST | `/provider/jobs/{id}/transition` | `{to_state}` |
| POST | `/provider/jobs/{id}/location` | lat/lng |
| POST | `/provider/jobs/{id}/photos` | |
| POST | `/provider/jobs/{id}/completion/request` | |
| GET | `/provider/earnings` | |
| GET | `/provider/payouts` | |
| POST | `/provider/jobs/{id}/ratings` | internal customer rating |

---

## Ops

| Method | Path | Notes |
|--------|------|-------|
| GET | `/ops/jobs` | filters: state, sla_risk |
| GET | `/ops/jobs/{id}` | full audit |
| POST | `/ops/jobs/{id}/manual-invite` | provider_id |
| POST | `/ops/jobs/{id}/credits` | service credit |
| GET/POST | `/ops/providers/{id}/verification` | approve/reject/suspend |
| GET | `/ops/disputes` | |
| POST | `/ops/disputes/{id}/resolve` | |
| GET | `/ops/audit` | |

---

## Webhooks (inbound)

| Source | Events |
|--------|--------|
| PSP | payment succeeded/failed/refunded |
| SMS (optional) | delivery receipts |

---

## Realtime Topics

- `job.{id}.state`
- `job.{id}.location`
- `provider.{id}.offers`
- `ops.jobs.sla`

---

## Critical Sequences

1. **Create → Match → Offers → Accept → En Route → … → Paid → Rated**
2. **Zero offer → expand → manual dispatch → customer accept**
3. **Cancel at stage → fee compute → optional credit**

All sequences must respect [Job State Machine](./Job-State-Machine.md).
