# VidyaVerse — Authentication and Authorization

## 1. Objectives

- Secure user authentication.
- Secure session management.
- Least-privilege authorization.
- Parent and child account isolation.
- Independent adult learner accounts.
- Secure administrative access.

## 2. Account Types

- Student.
- Parent or authorized guardian.
- Administrative user.
- Future teacher.
- Future institution administrator.

Adult learners shall be able to manage
their own accounts independently.

## 3. Authentication

The Identity Service shall own:

- User credentials.
- Authentication.
- Sessions.
- Refresh tokens.
- Account verification.
- Password recovery.
- Multi-factor authentication.

Passwords shall be hashed using Argon2id
with appropriately configured parameters.

## 4. Access Tokens

Access tokens shall use asymmetric JWT signing.

Initial signing algorithm: RS256.

Initial access token lifetime: five minutes.

Tokens shall include minimal identity claims.

Services shall validate:

- Signature.
- Allowed signing algorithm.
- Issuer.
- Audience.
- Expiration.
- Applicable session status.

Signing keys shall support controlled rotation.

## 5. Refresh Tokens

Refresh tokens shall be opaque,
cryptographically random credentials.

Refresh token values shall not be stored
in plaintext.

Refresh token rotation shall be atomic.

Consumed token reuse shall trigger
appropriate session protection.

Concurrent legitimate refresh requests
shall be handled safely.

## 6. Sessions

Sessions shall support:

- Session creation.
- Session expiration.
- Session revocation.
- Logout.
- Logout from all devices.
- Token family tracking.
- Security event auditing.

Initial maximum session lifetime: 30 days.

Initial inactivity expiration: seven days.

## 7. Browser Security

Refresh tokens shall use secure HttpOnly cookies.

Cookie scope and SameSite settings shall
match the deployment architecture.

Cookie-authenticated operations shall
implement appropriate CSRF protection.

Authentication tokens shall not be
persisted in browser local storage.

## 8. Authorization

Authorization shall combine:

- Role-based access control.
- Explicit permissions.
- Resource ownership verification.
- Guardian relationship verification.
- Account and consent status.
- Applicable subscription entitlements.

Frontend authorization shall not replace
backend authorization.

## 9. Administrative Security

Administrative accounts shall use MFA.

Administrative permissions shall follow
least-privilege principles.

Sensitive operations shall require
appropriate authorization and audit records.

## 10. Account Recovery

Account recovery shall use short-lived,
single-use recovery credentials.

Recovery responses shall avoid unnecessary
account existence disclosure.

Successful password recovery shall trigger
appropriate session revocation.

## 11. Abuse Prevention

- Login rate limiting.
- Registration abuse detection.
- Password reset rate limiting.
- Credential stuffing protection.
- Suspicious session detection.

## 12. Service Authentication

Internal services shall authenticate callers.

Services shall not trust arbitrary identity
headers supplied by external clients.

Service identities shall have scoped permissions.

## 13. Security Testing

Test:

- Expired tokens.
- Invalid signatures.
- Invalid issuer and audience.
- Revoked sessions.
- Refresh token reuse.
- Concurrent token refresh.
- Unauthorized resource access.
- Privilege escalation.
- CSRF protection.
- Account recovery abuse.
