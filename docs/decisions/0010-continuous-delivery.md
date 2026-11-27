# ADR-0010: Controlled Continuous Delivery

## Status

Accepted

## Context

VidyaVerse requires reliable software
delivery across TypeScript, Python,
infrastructure and educational AI workloads.

The platform will handle student information,
payments and live examinations.

## Decision

Use GitHub Actions for continuous integration
and controlled continuous delivery.

Maintain verified, versioned application artifacts.

Deploy to staging where appropriate.

Require controlled production approval initially.

Use AWS OIDC authentication for deployment.

## Alternatives

- Manual deployment.
- Unrestricted continuous deployment.
- Self-hosted CI/CD infrastructure.

## Consequences

Positive:

- Repeatable builds.
- Automated verification.
- Traceable releases.
- Reduced credential exposure.
- Controlled production changes.

Negative:

- Pipeline maintenance requirements.
- CI execution costs.
- Additional deployment configuration.

## Constraints

- Do not expose production secrets to
  untrusted workflows.
- Do not deploy unverified artifacts.
- Preserve database compatibility.
- Maintain appropriate rollback procedures.
- Avoid unnecessary deployment disruption
  during live examinations.

## Review Triggers

- Increased deployment frequency.
- Larger engineering team.
- Higher availability requirements.
- CI performance bottlenecks.
- Significant infrastructure growth.
