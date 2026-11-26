# VidyaVerse — Engineering Instructions

## 1. Project Mission

Build a production-grade AI-powered interactive
and multilingual education platform.

## 2. Sources of Truth

Read the relevant documentation before implementation:

- docs/product/vision.md
- docs/product/prd.md
- docs/product/mvp-scope.md
- docs/product/business-rules.md
- docs/product/backlog.md

Report conflicting requirements instead of silently
selecting one interpretation.

## 3. Repository Rules

- Preserve the established monorepo structure.
- Do not rename or relocate existing applications
  without explicit approval.
- Do not introduce unnecessary applications or services.
- Use pnpm for JavaScript and TypeScript packages.
- Use uv for Python services.
- Commit dependency lockfiles.
- Do not commit credentials or personal information.

## 4. Engineering Rules

- Use production-oriented folder structures.
- Maintain explicit module boundaries.
- Prefer dependency injection.
- Separate domain logic from infrastructure.
- Validate external inputs.
- Use structured error handling.
- Avoid unnecessary dependencies.
- Do not change unrelated functionality.
- Document significant architectural decisions.

## 5. TypeScript Rules

- Enable strict TypeScript settings.
- Avoid unsafe any types.
- Validate external data at runtime.
- Prefer explicit contracts at service boundaries.
- Maintain backward compatibility where required.

## 6. Python Rules

- Use project-specific Python environments.
- Use type annotations.
- Validate external data.
- Keep AI providers behind abstractions.
- Separate prompts, orchestration and domain logic.
- Maintain automated tests.

## 7. Database Rules

- Database-owning services own their schemas.
- Database-owning services own their migrations.
- Services shall not directly modify another
  service's database.
- Database changes require migration review.
- Preserve data integrity and transactional boundaries.

## 8. AI Rules

- Treat AI output as untrusted data.
- Validate structured AI output.
- Do not execute arbitrary AI-generated code.
- Track model and prompt versions.
- Track token usage and generation costs.
- Store reusable generated content.
- Prefer deterministic validation where available.
- Do not use student data for model training by default.

## 9. Examination Rules

- Server-side time is authoritative.
- Published examination versions are immutable.
- Objective scoring must be deterministic.
- Submission operations must support idempotency.
- AI must not be required during live examinations.
- Scoring changes must be auditable.

## 10. Security and Privacy

- Enforce authentication and authorization server-side.
- Apply least-privilege access.
- Protect uploaded student documents.
- Do not log sensitive student information.
- Apply child safety and privacy requirements.
- Use secure secret management.
- Include security tests for sensitive workflows.

## 11. Testing Rules

- Add unit tests for domain logic.
- Add integration tests for infrastructure boundaries.
- Add E2E tests for critical user journeys.
- Test failure scenarios.
- Test authorization boundaries.
- Do not claim tests passed unless they were executed.

## 12. Development Workflow

For each feature:

1. Identify applicable requirements.
2. Review existing architecture.
3. Define acceptance criteria.
4. Implement the smallest complete change.
5. Add automated tests.
6. Run relevant quality checks.
7. Update documentation.
8. Report changes and unresolved issues.

## 13. Completion Criteria

A feature is complete when:

- Acceptance criteria are satisfied.
- Required tests pass.
- Relevant documentation is updated.
- Security implications are reviewed.
- Known limitations are reported.
- No unrelated changes are introduced.

## 14. Prohibited Actions

- Publishing unvalidated educational content.
- Exposing correct answers during active examinations.
- Introducing paid advantages in prize competitions.
- Committing credentials.
- Silently modifying product requirements.
- Destructive database changes without approval.
- Claiming unexecuted tests have passed.
