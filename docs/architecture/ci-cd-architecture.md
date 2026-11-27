# VidyaVerse — CI/CD Architecture

## 1. Objective

Provide repeatable, secure and reliable
software delivery across the monorepo.

## 2. Source Control

Use Git and GitHub.

Maintain a protected main branch.

Use short-lived feature, fix, documentation
and refactoring branches.

Changes shall be reviewed through pull requests
where practical.

## 3. Continuous Integration

CI shall progressively verify:

- Dependency installation.
- Formatting.
- Linting.
- Type checking.
- Unit tests.
- Integration tests.
- End-to-end tests.
- Application builds.
- Secret scanning.
- Dependency vulnerabilities.
- Container vulnerabilities.

Checks shall be introduced alongside
the corresponding application capabilities.

## 4. TypeScript Pipeline

Use pnpm and Turborepo.

Install dependencies using the committed lockfile.

Respect workspace dependency ordering.

Use task caching where appropriate.

## 5. Python Pipeline

Use uv and the committed uv lockfile.

Verify:

- Formatting.
- Linting.
- Type checking.
- Unit tests.
- Integration tests.
- AI evaluation where applicable.

## 6. AI Testing

Ordinary CI tests shall not depend on
live external AI provider availability.

Use deterministic fixtures and mocked providers.

Real provider evaluation shall use
controlled execution and approved budgets.

## 7. Build Artifacts

Production application artifacts shall
be versioned and traceable to source commits.

Container images shall use immutable
release identifiers and recorded digests.

## 8. Artifact Registry

Amazon ECR is the proposed production
container registry.

Container images shall be scanned
before production deployment.

## 9. AWS Authentication

GitHub Actions shall use OIDC and
temporary AWS credentials where supported.

Deployment IAM roles shall follow
least-privilege principles.

Avoid long-lived AWS access keys.

## 10. Environments

Support:

- Local development.
- Continuous integration.
- Staging.
- Production.

Environment credentials and data
shall remain appropriately isolated.

## 11. Deployment

Use verified application artifacts.

Deploy to staging before production
where appropriate.

Production deployments shall require
controlled approval initially.

## 12. Workflow Security

- Restrict workflow permissions.
- Review third-party actions.
- Pin production actions to verified commit SHAs.
- Prevent untrusted code from accessing secrets.
- Protect deployment environments.
- Scan for committed credentials.

## 13. Observability

Record:

- Build results.
- Test results.
- Deployment versions.
- Deployment status.
- Health check results.
- Rollback events.

## 14. Cost Management

Use concurrency controls and caching.

Introduce affected-package execution
when repository growth justifies it.

Avoid unnecessary AI provider calls
during automated testing.
