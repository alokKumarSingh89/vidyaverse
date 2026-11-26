# ADR-0007: Resource-Level Authorization

## Status

Accepted

## Context

VidyaVerse supports students, parents,
administrators and future institutions.

Role-based authorization alone cannot
prevent unauthorized access to individual
student resources.

## Decision

Combine RBAC with resource-level
authorization policies.

Verify ownership, guardian relationships,
resource scope and applicable permissions.

Enforce authorization within the responsible
business service.

## Alternatives

- Role-based authorization only.
- Frontend authorization only.
- Unrestricted administrative access.

## Consequences

Positive:

- Stronger student privacy.
- Explicit authorization boundaries.
- Reduced cross-account data exposure.
- Support for future institutions.

Negative:

- Additional authorization logic.
- More comprehensive testing requirements.
- Potential cross-service policy dependencies.

## Constraints

- Deny access by default.
- Never trust client-supplied ownership claims.
- Do not bypass resource authorization
  because a request originates internally.
- Audit sensitive administrative operations.

## Review Triggers

- Institution onboarding.
- Complex delegated permissions.
- Authorization performance bottlenecks.
- New guardian access requirements.
