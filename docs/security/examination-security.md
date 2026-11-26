# VidyaVerse — Examination Security

## 1. Objective

Provide reliable, fair and secure
online examinations.

## 2. Examination Publication

Published examinations shall reference
immutable versions of:

- Questions.
- Answer keys.
- Marks.
- Scoring rules.
- Examination duration.
- Eligibility rules.

## 3. Eligibility

The Assessment Service shall verify:

- Student account status.
- Required consent.
- Examination registration.
- Applicable eligibility requirements.
- Attempt restrictions.

Prize examination eligibility shall not
depend on purchasing a subscription.

## 4. Server-Authoritative Timing

The server shall determine:

- Examination start time.
- Examination end time.
- Attempt start time.
- Attempt expiration.
- Submission eligibility.

Client-side timers shall be informational.

## 5. Answer Security

Correct answers shall not be included
in active examination response payloads.

Answer keys shall have restricted access.

Examination answers shall be persisted
before successful acknowledgement.

## 6. Submission Integrity

Answer submissions shall support:

- Ownership validation.
- Schema validation.
- Idempotency.
- Concurrent update handling.
- Durable persistence.

Final submission shall prevent unauthorized
subsequent answer modification.

## 7. Scoring

Objective scoring shall be deterministic.

Scoring shall use the published
examination and scoring versions.

Real-time AI provider availability shall
not be required for live examinations.

Subjective AI evaluation shall remain
provisional where appropriate.

## 8. Anti-Abuse Controls

- Request rate limiting.
- Duplicate registration detection.
- Attempt restrictions.
- Suspicious activity detection.
- Appropriate question randomization.
- Winner verification.

Automated suspicion indicators shall not
alone establish cheating.

## 9. Examination Availability

The platform shall support:

- Autosave.
- Controlled reconnection.
- Service health monitoring.
- Load testing.
- Incident recovery procedures.

Examination disruption policies shall
be communicated before participation.

## 10. Result Corrections

Confirmed scoring defects shall trigger:

- Audited correction.
- Identification of affected attempts.
- Consistent rescoring.
- Updated rankings.
- Appropriate participant communication.

## 11. Prize Competitions

Valuable prizes shall remain disabled until:

- Legal approval is obtained.
- Funding is approved.
- Question quality is independently verified.
- Winner verification procedures are available.
- Challenge and correction rules are published.

## 12. Privacy

Avoid invasive monitoring by default.

Biometric or camera-based proctoring shall
require separate necessity, privacy and
legal assessment.

## 13. Security Testing

Test:

- Unauthorized attempt access.
- Expired examination submissions.
- Duplicate submissions.
- Concurrent answer updates.
- Answer key disclosure.
- Scoring manipulation.
- Interrupted connections.
- Ranking correction.
