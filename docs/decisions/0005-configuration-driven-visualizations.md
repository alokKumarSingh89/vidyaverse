# ADR-0005: Configuration-Driven Visualizations

## Status

Accepted

## Context

VidyaVerse requires thousands of interactive
educational explanations.

Generating custom executable code for every
question would increase security, maintenance
and quality risks.

## Decision

Build reusable interactive learning engines.

AI shall generate structured configurations
for registered visualization components.

Configurations shall pass schema validation
before rendering.

## Alternatives

- Generate React code dynamically using AI.
- Create a custom component for every question.
- Use only static educational images.

## Consequences

Positive:

- Reusable educational components.
- Lower content generation costs.
- Consistent user experience.
- Improved security.
- Deterministic evaluation support.

Negative:

- Initial learning engine development effort.
- Limited visualization capabilities until
  additional components are implemented.
- Schema version management.

## Constraints

Arbitrary AI-generated executable code
shall not be executed in student browsers.

Examination evaluation shall remain
server-authoritative.

## Review Triggers

- Unsupported educational concepts.
- Visualization performance limitations.
- Accessibility requirements.
- Advanced simulation requirements.
