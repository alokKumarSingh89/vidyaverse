# ADR-0004: AI Provider Abstraction

## Status

Accepted

## Context

VidyaVerse requires multiple AI capabilities.

AI providers differ in quality, cost,
availability and supported features.

Direct provider coupling would increase
migration complexity.

## Decision

Introduce provider-independent interfaces
for supported AI capabilities.

Use provider-specific adapters behind
these interfaces.

Introduce additional providers only when
business requirements justify them.

## Alternatives

- Direct provider SDK usage in business logic.
- One permanent AI provider.
- Self-host all models initially.

## Consequences

Positive:

- Reduced provider dependency.
- Centralized usage accounting.
- Task-specific model selection.
- Easier provider migration.

Negative:

- Additional abstraction complexity.
- Provider capability differences.
- Adapter maintenance requirements.

## Constraints

Provider abstraction shall not hide
important capability differences.

Fallback providers shall satisfy required
quality, privacy and security policies.

## Review Triggers

- Provider pricing changes.
- Quality regressions.
- Availability issues.
- New language requirements.
- Specialized model requirements.
