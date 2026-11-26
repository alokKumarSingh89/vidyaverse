# VidyaVerse — Infrastructure Security

## 1. Production Environment

AWS infrastructure shall be provisioned
using version-controlled Terraform.

Production and non-production environments
shall have appropriate isolation.

## 2. Network Security

- Use a dedicated VPC.
- Restrict public entry points.
- Place application workloads in private subnets
  where appropriate.
- Keep databases inaccessible from the public internet.
- Restrict traffic using security groups.
- Control outbound connectivity.

## 3. Identity and Access Management

AWS permissions shall follow least privilege.

ECS workloads shall use task-specific IAM roles.

Avoid long-lived AWS credentials.

CI/CD shall use short-lived federated credentials
where supported.

## 4. Secret Management

Production secrets shall use AWS Secrets Manager
or another approved secret management service.

Secrets include:

- Database credentials.
- JWT signing keys.
- AI provider API keys.
- Payment provider credentials.
- Notification provider credentials.

Secrets shall not be committed to Git
or included in frontend bundles.

## 5. Encryption

Use HTTPS for external communication.

Protect sensitive internal communication
according to the threat model.

Enable encryption at rest for applicable
databases, object storage and backups.

## 6. Container Security

- Use trusted base images.
- Run containers as non-root where possible.
- Scan container images.
- Limit container permissions.
- Avoid unnecessary packages.
- Pin and update dependencies.
- Restrict filesystem write access.

## 7. Application Protection

- Request validation.
- API rate limiting.
- Appropriate CORS configuration.
- Content Security Policy.
- Secure HTTP headers.
- WAF where justified.
- Request size limits.

## 8. AI Provider Security

AI provider credentials shall remain
server-side.

Provider access shall be restricted
to authorized AI workloads.

Enforce:

- Request budgets.
- Usage quotas.
- Execution timeouts.
- Retry limits.
- Data minimization.

## 9. Monitoring

Monitor:

- Authentication failures.
- Authorization failures.
- Application error rates.
- API latency.
- ECS task health.
- CPU and memory utilization.
- Database connections.
- Queue depth and age.
- AI usage and cost anomalies.

## 10. Auditing

Audit important operations involving:

- Administrative permissions.
- Account security.
- Consent changes.
- Examination publication.
- Result corrections.
- Prize approval.
- Sensitive resource access.

Protect audit records against
unauthorized modification.

## 11. Backup and Recovery

Define recovery objectives for
critical data and services.

Automate appropriate backups.

Regularly test restoration procedures.

## 12. Incident Response

Maintain procedures for:

- Detection.
- Investigation.
- Containment.
- Credential revocation.
- Service recovery.
- Required notifications.
- Post-incident review.

## 13. Cost-Aware Security

Introduce infrastructure controls
according to measured requirements.

Cost optimization shall not remove
essential security protections.
