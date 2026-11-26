# ADR-0003: AI Platform Isolation

## Status

Accepted

## Context

AI workloads have different latency, resource,
reliability and cost characteristics compared
with transactional application workloads.

External AI providers may become unavailable
or produce incorrect responses.

## Decision

Implement the AI platform as an independent
Python and FastAPI service.

Use asynchronous processing for expensive
or long-running AI workloads.

Persist validated reusable educational content.

Live examinations shall not require real-time
AI provider availability.

## Alternatives

- Implement all AI functionality inside NestJS.
- Call external AI providers directly from clients.

## Consequences

Positive:

- Independent AI scaling.
- Access to Python AI and scientific libraries.
- Better failure isolation.
- Centralized AI cost tracking.
- Replaceable AI providers.

Negative:

- Additional service communication.
- Background job management.
- Distributed observability requirements.

## Constraints

- AI outputs shall be treated as untrusted.
- Generated content shall pass validation.
- Student browsers shall not execute AI-generated code.
- Student data shall not be used for training by default.
- AI services shall not bypass business service ownership.

## Review Triggers

- AI processing latency.
- Model provider costs.
- GPU requirements.
- Specialized model deployment.
- Educational quality evaluation results.
