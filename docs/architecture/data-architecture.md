# VidyaVerse — Data Architecture

## 1. Data Ownership

Each business service shall own its persistent data.

A shared PostgreSQL instance may initially host
multiple logically isolated service databases.

Each database-owning service shall use
service-specific database credentials.

## 2. Proposed Databases

- identity_db
- curriculum_db
- learning_db
- assessment_db
- championship_db
- subscription_db
- notification_db
- ai_platform_db

Databases shall be created when their corresponding
services require persistence.

## 3. TypeScript Database Access

NestJS services shall use Prisma 7 where appropriate.

Each database-owning service shall maintain:

- Its own Prisma schema.
- Its own prisma.config.ts.
- Its own generated Prisma client.
- Its own database migrations.
- Its own database connection configuration.

Shared Prisma clients across business services
are prohibited.

## 4. Python Database Access

Python services shall use SQLAlchemy and Alembic
where relational persistence is required.

AI services shall not directly modify databases
owned by NestJS services.

## 5. Cross-Service References

Cross-service entities shall be referenced
using stable identifiers.

Cross-service database joins and foreign keys
shall not be required for business workflows.

Data required across service boundaries shall
be obtained through APIs or event-driven projections.

## 6. Transactional Consistency

Local business transactions shall use
database transactions.

Distributed workflows shall use appropriate
consistency patterns when required:

- Transactional outbox.
- Idempotent consumers.
- Compensating actions.
- Saga orchestration.

## 7. Redis

Redis may be used for:

- Cache entries.
- Rate limiting.
- Temporary coordination.
- Short-lived session-related state.
- Non-authoritative progress information.

Redis shall not be the sole persistent storage
for examination answers or final results.

## 8. Object Storage

Object storage shall support:

- Uploaded examination papers.
- Uploaded answer sheets.
- Textbook images.
- Educational assets.
- Generated reports.

Student documents shall use private storage.

Access shall require authorization and
short-lived signed URLs where appropriate.

## 9. Vector Storage

PostgreSQL with pgvector may be used for:

- Curriculum retrieval.
- Semantic question search.
- Duplicate detection.
- Educational knowledge retrieval.

Vector retrieval shall not replace
authoritative transactional records.

## 10. Versioning

The platform shall maintain versions for:

- Curriculum.
- Learning content.
- Questions.
- Answer keys.
- Examination definitions.
- Scoring policies.
- AI prompts.
- AI model configurations.

Published examination versions shall remain immutable.

## 11. Data Protection

- Encryption in transit.
- Encryption at rest.
- Least-privilege database access.
- Retention policies.
- Authorized deletion workflows.
- Backup and recovery testing.
- Sensitive-data logging restrictions.

## 12. Scaling

Scaling shall be driven by measured workloads.

Possible strategies include:

- Query optimization.
- Appropriate indexing.
- Connection pooling.
- Vertical scaling.
- Read replicas.
- Partitioning.
- Independent database instances.

Database sharding shall be considered only
when simpler scaling strategies are insufficient.
