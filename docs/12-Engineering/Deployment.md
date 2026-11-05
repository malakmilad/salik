# Deployment — Salik Assist MVP

| Field | Value |
|-------|-------|
| **Version** | 1.0 |
| **Status** | Draft |
| **Author** | Engineering |
| **Last Updated** | November 5, 2026 |

## Purpose

Define environments, release process, and operational basics for MVP.

## Environments

| Env | URL pattern | Data | Who |
|-----|-------------|------|-----|
| dev | `*-dev` | Synthetic | Engineers |
| staging | `*-staging` | Anonymized / test | QA, Ops training |
| production | `api.salikassist…` (TBD) | Live | Restricted |

## Release Process

1. PR → CI (lint, unit, integration)
2. Deploy staging
3. QA sign-off on must-pass scenarios
4. Production deploy (blue/green or rolling)
5. Smoke: auth OTP (test), create job dry-run health, payment webhook health
6. Mobile: staged rollout (TestFlight / Play internal → production %)

## Feature Flags

| Flag | Use |
|------|-----|
| `soft_launch_invite_only` | Restrict customer signup to allowlist |
| `category_tow` / `category_battery` | Kill switch per category |
| `manual_surge` | Ops-only pricing note (no auto surge) |
| `matching_enabled` | Emergency pause matching |

## Observability

- API latency/error dashboards
- Offer SLA (time to first offer) realtime
- Payment success rate
- Job state funnel
- On-call rotation for production (align with Ops O2/O3 decision)

## Rollback

- Server: previous container/image within 15 minutes
- Mobile: remote config / flag to force “maintenance” screen if critical
- PSP: no schema-breaking payment changes without dual-run

## Related

- [Test Plan](./Test-Plan.md)
- [Security](./Security.md)
- [Launch Readiness Checklist](../14-Launch/Launch-Readiness-Checklist.md)
