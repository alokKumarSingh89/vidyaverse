# VidyaVerse — Service Boundaries

## 1. API Gateway

Responsibilities:

- Request routing.
- Authentication integration.
- Request context propagation.
- Rate limiting.
- API versioning.
- Response normalization.

The gateway shall not own core business data.

## 2. Identity Service

Responsibilities:

- User accounts.
- Authentication.
- Authorization.
- Sessions.
- Parent profiles.
- Child profiles.
- Parent-child relationships.
- Consent management.
- Account lifecycle.

Owned entities:

- User
- Credential
- Session
- Role
- Permission
- ParentProfile
- StudentProfile
- GuardianRelationship
- ConsentRecord

## 3. Curriculum Service

Responsibilities:

- Education boards.
- Academic years.
- Classes.
- Subjects.
- Chapters.
- Topics.
- Learning objectives.
- Curriculum versioning.

Owned entities:

- Board
- AcademicYear
- Grade
- Subject
- Chapter
- Topic
- LearningObjective
- CurriculumVersion

## 4. Learning Service

Responsibilities:

- Interactive lessons.
- Educational explanations.
- Visualization configurations.
- Learning content translations.
- Learning progress.
- Concept mastery.
- Learning recommendations.

Owned entities:

- Lesson
- LessonVersion
- LearningContent
- Visualization
- ContentTranslation
- LearningProgress
- ConceptMastery

## 5. Assessment Service

Responsibilities:

- Question bank.
- Question versioning.
- Practice sessions.
- Examination definitions.
- Examination attempts.
- Answer submission.
- Objective scoring.
- Answer disclosure.
- Result corrections.

Owned entities:

- Question
- QuestionVersion
- QuestionOption
- AnswerKey
- Assessment
- AssessmentVersion
- AssessmentQuestion
- Attempt
- AttemptAnswer
- AssessmentResult
- ScoringCorrection

## 6. Championship Service

Responsibilities:

- Competition scheduling.
- Competition registration.
- Eligibility verification.
- Class-wise rankings.
- Result challenges.
- Winner verification.
- Prize management.

Owned entities:

- Championship
- ChampionshipGroup
- Registration
- Ranking
- ResultChallenge
- Winner
- Prize
- PrizeDistribution

The Championship Service shall consume assessment
results instead of implementing examination scoring.

## 7. Subscription Service

Responsibilities:

- Subscription plans.
- Payment integration.
- Subscription lifecycle.
- Feature entitlements.
- Usage limits.
- Usage accounting.

Owned entities:

- Plan
- PlanEntitlement
- Subscription
- Payment
- Invoice
- UsageRecord

## 8. Notification Service

Responsibilities:

- Email notifications.
- SMS notifications.
- Future push notifications.
- Notification templates.
- Delivery tracking.

Owned entities:

- Notification
- NotificationTemplate
- DeliveryAttempt
- NotificationPreference

## 9. AI Platform

Responsibilities:

- AI provider abstraction.
- Prompt management.
- Question generation.
- Educational content generation.
- Answer verification.
- Translation.
- Document processing.
- Mathematical computation.
- Visualization configuration generation.
- Model evaluation.
- AI usage tracking.

Owned entities:

- GenerationJob
- PromptVersion
- ModelConfiguration
- ValidationResult
- DocumentProcessingJob
- AIUsageRecord
- EvaluationDataset

AI-generated artifacts shall be submitted to
the appropriate business service for publication.

## 10. Boundary Rules

- Every business entity shall have one authoritative owner.
- Services shall not directly modify another service's data.
- Cross-service references shall use stable identifiers.
- Service contracts shall be explicitly versioned.
- Shared packages shall not contain shared database entities.
- Cross-service operations shall handle partial failures.
- Services shall not bypass authorization boundaries.
- Database migrations shall be owned by the responsible service.

## 11. Implementation Strategy

Service boundaries define the target architecture.

Services shall be introduced incrementally.

The initial release does not require every service
to run as an independently deployed process.
