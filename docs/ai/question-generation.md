# VidyaVerse — Question Generation

## 1. Objective

Generate original, curriculum-aligned and
validated educational questions.

## 2. Generation Request

A generation request shall support:

- Education board.
- Curriculum version.
- Grade.
- Subject.
- Chapter.
- Topic.
- Learning objectives.
- Difficulty.
- Question type.
- Question count.
- Marks.
- Language.
- Optional visualization requirements.

## 3. Supported Question Types

Initial types:

- SINGLE_CHOICE
- MULTIPLE_CHOICE
- NUMERICAL
- INTERACTIVE

Future types:

- SHORT_ANSWER
- LONG_ANSWER
- MATCHING
- ORDERING
- DIAGRAM_LABELING

Subjective evaluation shall remain provisional
unless appropriate review requirements are met.

## 4. Generated Question Contract

A generated question shall include:

- Question text.
- Question type.
- Options where applicable.
- Proposed answer.
- Explanation.
- Difficulty estimate.
- Marks.
- Learning objectives.
- Curriculum references.
- Language.
- Optional visualization configuration.

## 5. Generation Workflow

1. Validate the generation request.
2. Retrieve relevant curriculum context.
3. Generate candidate questions.
4. Validate structured output.
5. Independently solve supported questions.
6. Verify mathematical answers.
7. Validate curriculum alignment.
8. Detect ambiguity.
9. Detect duplicate questions.
10. Validate explanations.
11. Validate visualization configurations.
12. Persist validation results.
13. Submit eligible content for approval.

## 6. Examination Paper Assembly

Question generation and examination assembly
shall remain separate operations.

Examination assembly shall select eligible
questions from the approved question bank.

A paper blueprint shall define:

- Question count.
- Total marks.
- Duration.
- Difficulty distribution.
- Question type distribution.
- Chapter coverage.
- Learning objective coverage.
- Language requirements.
- Question reuse restrictions.

Deterministic logic shall enforce blueprint
constraints.

Unsatisfied constraints shall be reported
instead of silently changing the blueprint.

## 7. Examination Versions

Published examinations shall reference immutable
question versions and scoring policies.

Correct answers and explanations shall remain
separate from student-facing examination payloads.

## 8. Translation

Translated questions shall reference the original
question version.

Translations shall preserve:

- Numerical values.
- Mathematical expressions.
- Correct answer meaning.
- Marks.
- Difficulty intent.

## 9. Difficulty Calibration

AI-generated difficulty shall be treated
as an initial estimate.

Difficulty may later be calibrated using
appropriate assessment statistics.

## 10. Failure Handling

Generation jobs shall support:

- Bounded retries.
- Idempotent processing.
- Cancellation.
- Failure reason tracking.
- Partial generation results.
- Execution budgets.
