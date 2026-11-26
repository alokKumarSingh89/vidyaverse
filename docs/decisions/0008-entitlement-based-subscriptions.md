# ADR-0008: Entitlement-Based Subscriptions

## Status

Accepted

## Context

VidyaVerse requires configurable subscriptions
and predictable AI processing costs.

Hardcoded plan-based feature checks would
increase coupling between business services
and pricing decisions.

## Decision

Use versioned subscription plans with
explicit feature entitlements.

Enforce usage limits on the backend.

Use atomic reservations for costly operations.

## Alternatives

- Hardcoded subscription checks.
- Unlimited AI usage.
- Client-side feature enforcement.

## Consequences

Positive:

- Flexible pricing.
- Controlled operating costs.
- Reusable authorization logic.
- Support for family subscriptions.

Negative:

- Additional usage accounting complexity.
- Concurrent reservation management.
- Reconciliation requirements.

## Constraints

- Usage limits shall be server-enforced.
- Duplicate operations shall be idempotent.
- AI costs shall be recorded.
- Paid entitlements shall not influence
  championship rankings.

## Review Triggers

- New pricing models.
- Increased AI operating costs.
- Institutional subscriptions.
- Usage accounting performance issues.
