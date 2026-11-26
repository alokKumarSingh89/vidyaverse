# ADR-0002: Database Ownership

## Status

Accepted

## Context

VidyaVerse contains multiple business domains
with different persistence requirements.

Independent database infrastructure for every
service would increase initial operating costs.

## Decision

Use service-owned logical databases with
service-specific credentials.

Initially, multiple databases may share
one PostgreSQL instance.

Each service owns its schema and migrations.

## Alternatives

- One shared application database.
- Independent database instance per service.

## Consequences

Positive:

- Clear data ownership.
- Lower initial infrastructure cost.
- Easier future database isolation.
- Independent migration ownership.

Negative:

- Shared infrastructure failure domain.
- Shared resource contention.
- Cross-service query complexity.
- Distributed consistency requirements.

## Constraints

- No direct cross-service database writes.
- No shared Prisma clients.
- No cross-service foreign key dependencies.
- Independent database access credentials.

## Review Triggers

- Database resource contention.
- Connection pool exhaustion.
- Different backup or recovery requirements.
- Security isolation requirements.
- Independent scaling requirements.
