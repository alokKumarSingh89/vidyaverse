# VidyaVerse — Communication Patterns

## 1. Communication Strategy

VidyaVerse shall support:

- Synchronous REST communication.
- Asynchronous job processing.
- Event-driven communication.
- In-process module interfaces during initial deployment.

Communication mechanisms shall be selected
according to business and reliability requirements.

## 2. Synchronous Communication

Use synchronous communication when an
immediate response is required.

Requirements:

- Explicit request and response contracts.
- Request timeouts.
- Error normalization.
- Authentication and authorization.
- Correlation identifiers.
- Bounded retries for safe operations.

## 3. Asynchronous Communication

Use asynchronous communication for:

- AI question generation.
- Document processing.
- Translation.
- Report generation.
- Notifications.
- Background evaluation.
- Learning analytics.

AWS SQS shall be the initial production
queue technology where queues are required.

## 4. Domain Events

Proposed domain events:

- identity.user.registered.v1
- identity.consent.granted.v1
- curriculum.version.published.v1
- learning.lesson.completed.v1
- assessment.attempt.submitted.v1
- assessment.completed.v1
- assessment.result.corrected.v1
- championship.result.finalized.v1
- subscription.activated.v1
- ai.generation.completed.v1
- ai.generation.failed.v1

Event names and payloads shall be versioned.

## 5. Event Envelope

Every domain event shall contain:

- Event identifier.
- Event type.
- Event version.
- Producer identifier.
- Occurrence timestamp.
- Correlation identifier.
- Event payload.

Sensitive personal information shall not be
included unless explicitly required and protected.

## 6. Delivery Semantics

Consumers shall assume at-least-once delivery
where applicable.

Consumers shall handle duplicate messages safely.

Message ordering shall not be assumed unless
explicitly guaranteed by the selected mechanism.

## 7. Event Publication

Transactional outbox shall be used where
business data and event publication must
remain consistent.

Consumers shall use idempotent processing.

## 8. Event Fan-Out

Independent consumers shall receive their own
event deliveries.

SNS or EventBridge may route events to
service-specific SQS queues.

A shared queue shall not be treated as
a broadcast mechanism.

## 9. Failure Handling

- Bounded retry policies.
- Exponential backoff with jitter.
- Dead-letter queues.
- Operational alerts.
- Idempotent replay.
- Circuit breakers where appropriate.

## 10. Examination Reliability

Live examination operations shall not depend
on synchronous AI provider calls.

Examination answer persistence shall complete
before successful acknowledgement.

Non-critical notifications and analytics
shall be processed asynchronously.

## 11. Observability

Communication shall propagate:

- Request identifiers.
- Correlation identifiers.
- Distributed trace context.

Logs shall not expose examination answer keys
or unnecessary student information.
