# VidyaVerse — Architecture Overview

## 1. Status

- Version: 0.1.0
- Status: Proposed architecture
- Product: VidyaVerse

## 2. Architecture Objectives

- Support incremental product development.
- Minimize initial infrastructure expenses.
- Maintain explicit business domain boundaries.
- Support independent service scaling.
- Support multilingual educational content.
- Support reusable interactive learning engines.
- Isolate AI workloads from transactional operations.
- Maintain security and privacy for children.
- Support reliable live examinations.

## 3. Architecture Style

VidyaVerse shall use a modular, microservice-ready
architecture within a monorepo.

Logical service boundaries shall be established before
introducing independent distributed deployments.

Services shall be independently deployable when
business, scaling or reliability requirements justify it.

## 4. Application Layer

- Web shell.
- Student web application.
- Parent web application.
- Administration web application.
- Future mobile application.

Frontend applications shall reuse shared packages
for UI, contracts, localization and learning engines.

## 5. Backend Layer

- API Gateway.
- Identity Service.
- Curriculum Service.
- Learning Service.
- Assessment Service.
- Championship Service.
- Subscription Service.
- Notification Service.

Future analytics functionality may be extracted
into an independent service.

## 6. AI Platform

The AI platform shall use Python and FastAPI.

Responsibilities include:

- AI provider abstraction.
- Curriculum-grounded content generation.
- Question generation.
- Answer verification.
- Document intelligence.
- Translation.
- Interactive visualization configuration.
- AI tutoring.
- Model evaluation.
- AI cost tracking.

AI operations shall be isolated from critical
transactional workflows.

## 7. Data Layer

- PostgreSQL for transactional persistence.
- pgvector for supported vector retrieval.
- Redis for caching and temporary state.
- Object storage for uploaded documents and assets.
- Message queues for asynchronous workloads.

PostgreSQL remains the authoritative data source
for examination attempts and final results.

## 8. Infrastructure

Local development:

- Docker Compose.
- Local PostgreSQL.
- Local Redis.
- Local or compatible object storage when required.

Production target:

- AWS ECS and Fargate.
- Application Load Balancer.
- Amazon RDS.
- Amazon S3.
- Amazon SQS.
- Amazon CloudFront.
- AWS Secrets Manager.
- Amazon CloudWatch.

Infrastructure shall be introduced incrementally.

## 9. Reliability

- Published content shall remain available during AI failures.
- Live examinations shall not require real-time AI.
- Critical operations shall support idempotency.
- Asynchronous jobs shall support bounded retries.
- Failed jobs shall support dead-letter handling.
- Database backups and recovery shall be tested.
- Examination availability shall be load-tested.

## 10. Security

- Authentication and authorization.
- Least-privilege access.
- Encryption in transit and at rest.
- Private student document storage.
- Secure secret management.
- Audit logging.
- Child privacy and consent management.

## 11. Observability

- Structured application logs.
- Distributed tracing.
- Application and infrastructure metrics.
- AI usage and cost metrics.
- Examination health metrics.
- Operational alerts.

## 12. Architecture Evolution

Architecture decisions shall be documented using ADRs.

Service extraction shall be driven by measured
scaling, reliability, deployment or ownership needs.
