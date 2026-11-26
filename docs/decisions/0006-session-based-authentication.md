# ADR-0006: Session-Based Authentication

## Status

Accepted

## Context

VidyaVerse requires secure authentication,
device management and session revocation.

Purely stateless long-lived JWT authentication
does not provide sufficient session control.

## Decision

Use short-lived JWT access tokens with
server-managed sessions.

Use opaque rotating refresh tokens.

Maintain session and token family records
in the Identity Service.

Use asymmetric JWT signing.

## Alternatives

- Long-lived stateless JWT tokens.
- Traditional cookie-only sessions.
- Fully managed external identity provider.

## Consequences

Positive:

- Session revocation.
- Device-level session management.
- Refresh token reuse detection.
- Short access token exposure window.

Negative:

- Session persistence requirements.
- Additional refresh token complexity.
- Session status verification overhead.

## Constraints

- Refresh token rotation shall be atomic.
- Refresh tokens shall not be stored in plaintext.
- Revoked sessions shall not be renewed.
- Sensitive operations shall enforce
  the required session validity policy.

## Review Triggers

- Authentication performance bottlenecks.
- Session scaling requirements.
- Enterprise identity integration.
- Security incident findings.
