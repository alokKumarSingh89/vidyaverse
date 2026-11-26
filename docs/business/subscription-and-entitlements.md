# VidyaVerse — Subscription and Entitlements

## 1. Objective

Provide configurable educational subscriptions
with predictable usage and operating costs.

## 2. Plan Versioning

Subscription plans shall support:

- Stable plan identifiers.
- Versioned pricing.
- Billing intervals.
- Currency.
- Effective dates.
- Feature entitlements.
- Usage allowances.

Existing subscription terms shall not be
silently modified.

## 3. Entitlement Types

Supported entitlement types may include:

- Boolean feature access.
- Quantity limits.
- Token limits.
- Monetary budgets.
- Time-based allowances.
- Student profile limits.

## 4. Entitlement Identifiers

Initial identifiers:

- learning.interactive.access
- practice.questions.daily
- documents.uploads.monthly
- documents.pages.monthly
- ai.tutor.requests.monthly
- ai.tokens.monthly
- ai.budget.monthly
- evaluation.answers.monthly
- parent.analytics.advanced
- family.students.maximum

## 5. Authorization

Business services shall enforce entitlements
on the backend.

Business functionality shall not depend
directly on subscription plan names.

## 6. Usage Reservation

Costly operations shall support:

1. Entitlement verification.
2. Estimated usage calculation.
3. Atomic quota reservation.
4. Operation execution.
5. Actual usage recording.
6. Reservation reconciliation.

Concurrent requests shall not bypass
usage or budget restrictions.

## 7. Usage Accounting

Usage records shall preserve:

- Operation identifier.
- Account identifier.
- Entitlement identifier.
- Billing period.
- Reserved quantity.
- Actual quantity.
- Estimated cost.
- Actual or provider-reported cost.
- Processing status.
- Idempotency identifier.

## 8. Reservation Recovery

Reservations shall support expiration
and reconciliation.

Failed operations shall release unused
allowances.

Provider charges incurred during failed
operations shall still be recorded.

Unknown provider outcomes shall be reconciled
before unsafe duplicate execution.

## 9. Family Subscriptions

Family subscriptions may authorize multiple
student profiles.

Student academic histories shall remain isolated.

Shared allowances shall enforce concurrent
usage restrictions.

## 10. Subscription Lifecycle

Supported states may include:

- PENDING
- ACTIVE
- PAST_DUE
- CANCELLED
- EXPIRED

Cancellation shall preserve paid access
according to the applicable subscription terms.

## 11. Free Tier

Free users shall have configurable usage limits.

Free championship eligibility shall not depend
on purchasing paid entitlements.

## 12. Reliability

Entitlement enforcement shall support:

- Atomic transactions.
- Idempotent usage accounting.
- Audited adjustments.
- Usage reconciliation.
- Operational monitoring.
