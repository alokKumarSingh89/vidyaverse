# VidyaVerse — Frontend Architecture

## 1. Objectives

- Provide a professional and accessible learning experience.
- Support affordable mobile devices.
- Support multiple languages.
- Reuse interactive learning components.
- Support independent frontend evolution.
- Minimize initial deployment complexity.

## 2. Applications

### Web Shell

Responsibilities:

- Application composition.
- Shared navigation.
- Authentication integration.
- Route management.
- Global error handling.
- Language initialization.

### Student Web

Responsibilities:

- Student dashboard.
- Curriculum navigation.
- Interactive lessons.
- Practice sessions.
- Document uploads.
- AI tutoring.
- Live examinations.
- Learning progress.

### Parent Web

Responsibilities:

- Child profile management.
- Independent language preferences.
- Translated educational content.
- Progress reports.
- Learning recommendations.
- Subscription management.

### Admin Web

Responsibilities:

- Curriculum management.
- AI generation workflows.
- Content validation.
- Question bank management.
- Examination scheduling.
- Championship management.
- Operational dashboards.

## 3. Shared Packages

### UI

- Design tokens.
- Typography.
- Accessible components.
- Forms.
- Navigation.
- Feedback components.

### Contracts

- API request and response schemas.
- Shared identifiers.
- Runtime validation schemas.
- Event contracts.

### Localization

- Translation resources.
- Locale configuration.
- Number and date formatting.
- Language fallback rules.

### Authentication

- Authentication client interfaces.
- Session handling.
- Authorization helpers.

### Learning Engine

- Geometry.
- Arithmetic.
- Fractions.
- Algebra.
- Graphs.
- Physics.
- Chemistry.
- Biology.
- Simulations.

## 4. Micro-Frontend Strategy

Static package composition shall be used for
shared components and learning engines.

Runtime federation may be introduced for
independently deployed frontend modules.

Framework and federation compatibility shall
be validated before implementation.

The architecture shall not depend on runtime
federation for the initial learning release.

## 5. State Management

- Local component state for UI interactions.
- Server-state caching for API resources.
- Shared application state only when necessary.
- Server-authoritative examination state.

## 6. Interactive Learning Rules

- Visualizations shall use approved component schemas.
- AI shall generate configuration rather than executable code.
- Interactive components shall be reusable.
- Visualizations shall provide accessible alternatives.
- Examination visualizations shall not expose answer keys.
- Visualizations shall support localization.

## 7. Performance

- Route-based code splitting.
- Lazy loading of expensive visualizations.
- Optimized image and asset delivery.
- Minimal initial JavaScript payloads.
- Appropriate client-side caching.
- Support for low-bandwidth connections.

## 8. Security

- Do not expose secrets in frontend bundles.
- Do not trust client-side authorization decisions.
- Do not expose examination answer keys.
- Sanitize untrusted rendered content.
- Apply appropriate content security policies.
- Avoid storing sensitive credentials in local storage.

## 9. Testing

- Unit tests for reusable components.
- Interaction tests for learning engines.
- Integration tests for API interactions.
- End-to-end tests for critical user journeys.
- Accessibility testing.
- Performance testing.
