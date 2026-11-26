# VidyaVerse — Payment Architecture

## 1. Objective

Provide secure, reliable and auditable
subscription payments.

## 2. Provider Abstraction

Payment functionality shall use
provider-independent interfaces.

Razorpay is the proposed initial provider,
subject to onboarding and capability verification.

## 3. Payment Capabilities

Provider adapters may support:

- Payment order creation.
- Recurring subscription creation.
- Payment status verification.
- Subscription cancellation.
- Refund initiation.
- Webhook signature verification.
- Payment reconciliation.

## 4. Payment Creation

The backend shall determine:

- Plan version.
- Payment amount.
- Currency.
- Applicable charges.
- Customer authorization.

Client-supplied payment amounts shall
not be trusted.

Use integer minor currency units
for monetary amounts.

## 5. Checkout

Use provider-hosted payment functionality
where appropriate.

Do not store raw card details.

Payment credentials shall remain server-side.

## 6. Webhook Security

Webhook processing shall:

- Verify signatures using the required raw body.
- Validate the provider event.
- Deduplicate provider event identifiers.
- Validate payment amount and currency.
- Validate provider order references.
- Enforce valid state transitions.
- Persist events durably.

Frontend success callbacks shall not
independently activate subscriptions.

## 7. Idempotency

Repeated payment events shall not cause:

- Duplicate subscription activation.
- Duplicate invoices.
- Duplicate refunds.
- Duplicate entitlement grants.

## 8. Event Ordering

Webhook events may arrive out of order.

Payment state transitions shall prevent
invalid state regression.

Uncertain payment states shall be
reconciled with the provider.

## 9. Subscription Activation

Verified payment processing shall persist
payment and subscription changes atomically.

Use an outbox for reliable downstream events.

## 10. Refunds

Refund workflows shall support:

- Authorization.
- Refund reason.
- Amount validation.
- Provider request tracking.
- Provider confirmation.
- Auditing.
- Applicable entitlement adjustments.

## 11. Reconciliation

Reconcile internal records with provider
payments, refunds and settlements.

Unresolved differences shall generate
operational alerts.

## 12. Compliance

Review applicable requirements for:

- Payment processing.
- Recurring mandates.
- GST and invoicing.
- Refunds.
- Consumer protection.
- Financial record retention.

## 13. Monitoring

Track:

- Payment success rate.
- Payment failure rate.
- Webhook processing latency.
- Invalid webhook signatures.
- Duplicate events.
- Reconciliation discrepancies.
- Refund processing failures.
