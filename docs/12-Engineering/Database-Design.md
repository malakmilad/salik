# Database Design — Salik Assist MVP

| Field | Value |
|-------|-------|
| **Version** | 1.0 |
| **Status** | Draft |
| **Author** | Engineering |
| **Last Updated** | November 5, 2026 |

## Purpose

Define core relational entities for MVP. Physical schema (types, indexes) to be finalized in migration PRs; this document freezes the conceptual model.

## Related Documents

- [SRS](./SRS.md)
- [Job State Machine](./Job-State-Machine.md)
- [API Overview](./API-Overview.md)

---

## Entity Overview

```text
customers ──< jobs >── providers
               │
          offers, events, payments, ratings, disputes

providers ──< vehicles, documents, drivers
coverage_zones (polygons)
ops_users, audit_logs
```

---

## Core Tables (Logical)

### `customers`
- `id`, `mobile_e164`, `name`, `email`, `locale` (`ar`|`en`)
- `is_guest`, `guest_jobs_completed`, `status`
- `created_at`, `updated_at`

### `payment_methods`
- `id`, `customer_id`, `psp_token_ref`, `brand`, `last4`, `is_default`

### `customer_vehicles`
- `id`, `customer_id`, `type` (sedan|suv|commercial), `plate`, `nickname`

### `providers`
- `id`, `business_name`, `mobile`, `email`, `status` (pending|active|suspended|rejected)
- `rating_avg`, `rating_count`, `locale`
- `available` bool, `service_categories[]`
- `commission_override` nullable (promo 0%)
- `training_completed_at`

### `provider_vehicles`
- `id`, `provider_id`, `plate`, `type`, `registration_doc_id`, `active` (max 5 active)

### `provider_drivers`
- `id`, `provider_id`, `name`, `id_doc_ref`, `background_check_status`, `active`

### `provider_documents`
- `id`, `provider_id`, `type` (trade_license|insurance|id|other)
- `storage_key`, `expires_on`, `review_status`, `reviewed_by`, `reviewed_at`

### `coverage_zones`
- `id`, `name`, `polygon` (GeoJSON), `active`, `sla_enabled`

### `jobs`
- `id`, `customer_id`, `provider_id` nullable
- `category` (TOW|BATTERY_JUMP|BATTERY_REPLACE)
- `state` (see state machine)
- `pickup_lat`, `pickup_lng`, `pickup_geohash`
- `dropoff_lat/lng` nullable (tow)
- `vehicle_snapshot` JSON
- `estimate_min_aed`, `estimate_max_aed`
- `final_price_aed` nullable
- `accepted_offer_id` nullable
- `high_risk_location` bool
- `created_at`, `updated_at`, state timestamps as needed

### `offers`
- `id`, `job_id`, `provider_id`
- `eta_minutes`, `price_aed`
- `status` (invited|submitted|withdrawn|accepted|expired|declined)
- `invited_at`, `respond_by`, `submitted_at`

### `job_events`
- `id`, `job_id`, `from_state`, `to_state`, `actor_type`, `actor_id`
- `reason_code`, `metadata` JSON, `created_at`
- Append-only

### `job_location_points` (or time-series store)
- `job_id`, `lat`, `lng`, `recorded_at` (provider trail while active)

### `payments`
- `id`, `job_id`, `customer_id`, `amount_aed`, `commission_aed`, `provider_net_aed`
- `psp_charge_id`, `status` (pending|succeeded|failed|refunded)
- `created_at`

### `payouts`
- `id`, `provider_id`, `payment_id`, `amount_aed`, `status` (scheduled|paid|held|failed)
- `scheduled_for`, `paid_at`, `hold_reason`

### `ratings`
- `id`, `job_id`, `from_role` (customer|provider), `score`, `comment`, `visibility` (public|internal)

### `disputes`
- `id`, `job_id`, `opened_by`, `reason`, `status`, `resolution`, `created_at`, `resolved_at`

### `service_credits`
- `id`, `customer_id`, `amount_aed`, `reason`, `job_id`, `issued_by_ops_id`

### `waitlist_entries`
- `id`, `mobile`, `lat`, `lng`, `created_at`

### `ops_users`
- `id`, `email`, `role` (agent|supervisor|verifier|admin), `mfa_enabled`

### `audit_logs`
- `id`, `actor_id`, `action`, `entity_type`, `entity_id`, `payload`, `created_at`

---

## Indexing Priorities

- `jobs(state, created_at)`, `jobs(pickup_geohash)`, `offers(job_id, status)`
- `providers(status, available)`, documents `expires_on`
- `job_events(job_id, created_at)`

---

## Integrity Rules

- Only one `accepted` offer per job
- `final_price` cannot exceed estimate max × 1.15 without approval event
- Provider `available=true` requires `status=active` and valid docs
- Guest customers blocked at 3rd job create if still guest
