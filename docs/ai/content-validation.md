# VidyaVerse — Content Validation

## 1. Objective

Prevent incorrect, misleading, ambiguous or
inappropriate AI-generated educational content
from being published.

## 2. Content Lifecycle

Supported states:

- DRAFT
- VALIDATING
- VALIDATION_FAILED
- VALIDATED
- APPROVED
- PUBLISHED
- QUARANTINED
- ARCHIVED

State transitions shall be explicitly controlled.

## 3. Validation Categories

### Schema Validation

Verify required fields, types, identifiers
and supported content formats.

### Curriculum Validation

Verify board, grade, subject, topic
and learning objective alignment.

### Mathematical Validation

Use deterministic mathematical verification
where supported.

### Answer Validation

Verify answer correctness, option uniqueness
and scoring compatibility.

### Explanation Validation

Verify consistency between the answer,
explanation and question.

### Language Validation

Verify translated content preserves
the original educational meaning.

### Duplicate Validation

Detect exact and semantically similar questions.

### Safety Validation

Detect inappropriate, unsafe or age-incompatible
educational content.

### Visualization Validation

Verify component identifiers, parameters,
interaction rules and schema versions.

## 4. Independent Solving

Independent question solvers should not receive
the proposed answer before solving.

The generated solution shall be compared
with the proposed answer.

Agreement between AI models shall not be
treated as proof of correctness.

## 5. Validation Results

Each validation result shall include:

- Validator identifier.
- Validator version.
- Validation status.
- Reason codes.
- Supporting evidence.
- Execution timestamp.
- Relevant model metadata.

Supported validation outcomes:

- PASS
- FAIL
- INCONCLUSIVE
- NOT_APPLICABLE

## 6. Publication Rules

Mandatory validation failures shall block publication.

Inconclusive mandatory validation shall require
additional verification or review.

Automated validation shall not be represented
as independent expert approval.

## 7. Risk-Based Approval

Low-risk, objectively verifiable practice content
may use an approved automated publication policy.

Subjective or difficult-to-verify content shall
require additional review.

Valuable prize examinations shall require
independent content-quality approval.

## 8. Regeneration

Failed content may be regenerated using
validation feedback.

Regeneration shall enforce bounded attempts
and execution budgets.

Repeated failures shall result in quarantine
or review.

## 9. Correction Workflow

Reported content errors shall be investigated.

Confirmed errors shall result in:

- Content quarantine where necessary.
- Audited correction.
- New content version.
- Identification of affected assessments.
- Consistent rescoring when required.

Published examination snapshots shall not
be silently modified.

## 10. Quality Monitoring

Track:

- Validation acceptance rate.
- Validation failure reasons.
- Published content error rate.
- Translation error rate.
- Duplicate detection rate.
- User-reported content defects.
- Correction resolution time.
