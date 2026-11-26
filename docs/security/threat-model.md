# VidyaVerse — Threat Model

## 1. Methodology

Use STRIDE to identify and evaluate
application and infrastructure threats.

Threat models shall evolve with
the platform architecture.

## 2. Protected Assets

- User credentials.
- Authentication sessions.
- Child personal information.
- Guardian relationships.
- Consent records.
- Examination questions.
- Examination answer keys.
- Student answers and results.
- Uploaded documents.
- Subscription records.
- AI provider credentials.
- Proprietary educational datasets.

## 3. Trust Boundaries

- Browser to API Gateway.
- Gateway to business services.
- Business services to databases.
- Business services to AI platform.
- AI platform to external AI providers.
- User uploads to processing workers.
- Administrative users to management APIs.
- CI/CD to AWS infrastructure.

## 4. Threat Register

### THR-001: Account Takeover

Category: Spoofing.

Controls:

- Secure password hashing.
- Rate limiting.
- Session revocation.
- Administrative MFA.

### THR-002: Unauthorized Student Access

Category: Information disclosure.

Controls:

- Resource-level authorization.
- Guardian relationship validation.
- Authorization regression tests.

### THR-003: Examination Answer Tampering

Category: Tampering.

Controls:

- Server-authoritative validation.
- Immutable examination versions.
- Deterministic scoring.
- Idempotent persistence.

### THR-004: Unauthorized Result Modification

Category: Tampering and repudiation.

Controls:

- Scoped administrative permissions.
- Audited correction workflows.
- Consistent rescoring.

### THR-005: Examination Answer Leakage

Category: Information disclosure.

Controls:

- Separate answer-key contracts.
- Restricted database access.
- Controlled publication.
- Response contract testing.

### THR-006: Examination Traffic Overload

Category: Denial of service.

Controls:

- Rate limiting.
- Load testing.
- Horizontal scaling.
- Database capacity monitoring.
- Incident response procedures.

### THR-007: Malicious Document Upload

Category: Tampering and denial of service.

Controls:

- Quarantine.
- Malware scanning.
- File validation.
- Parser isolation.
- Resource limits.

### THR-008: AI Prompt Injection

Category: Elevation of privilege.

Controls:

- Untrusted document handling.
- Restricted AI tools.
- Structured output validation.
- Least-privilege execution.

### THR-009: AI Cost Abuse

Category: Denial of service.

Controls:

- Usage quotas.
- Atomic budget enforcement.
- Execution limits.
- Cost anomaly alerts.

### THR-010: Secret Exposure

Category: Information disclosure.

Controls:

- Secret management.
- Repository secret scanning.
- Scoped IAM roles.
- Credential rotation.

### THR-011: Administrative Privilege Abuse

Category: Elevation of privilege.

Controls:

- Least privilege.
- Administrative MFA.
- Permission checks.
- Audit records.

### THR-012: Unauthorized Model Training

Category: Information disclosure.

Controls:

- Dataset provenance.
- Data minimization.
- Training data approval.
- Student data exclusion by default.

## 5. Risk Assessment

Each threat shall be evaluated using:

- Likelihood.
- Business impact.
- Educational impact.
- Privacy impact.
- Existing controls.
- Residual risk.
- Responsible owner.

## 6. Review Triggers

Review the threat model when introducing:

- New authentication methods.
- New services.
- New AI providers.
- Payment integrations.
- Live examinations.
- Public competitions.
- New upload formats.
- New educational age groups.
- Model training capabilities.

## 7. Release Requirements

Unresolved critical security defects
shall block public release.

Residual risks shall be documented
and appropriately reviewed.
