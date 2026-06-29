# Testing

## Purpose

Set expectations for validation and confidence.

## Testing Strategy

- Add or update tests when behavior changes.
- Prefer focused tests near the changed code.
- Use integration tests for cross-module contracts and critical workflows.
- Keep test fixtures readable and representative.

## Backend Testing

### JUnit

- Use JUnit for service, domain, and utility tests.
- Test business rules directly at the service or domain level.
- Cover success, validation failure, not-found, conflict, and error paths where relevant.

### MockMvc

- Use MockMvc for Spring MVC controller behavior.
- Verify status codes, request validation, response shape, and error responses.
- Do not duplicate all service tests at controller level.

## Frontend Testing

### Vitest

- Use Vitest for frontend unit tests and pure logic.
- Keep tests fast and deterministic.

### React Testing Library

- Test user-visible behavior.
- Prefer queries by role, label, and accessible name.
- Cover loading, empty, error, and success states.

## Coverage

- Coverage should protect important behavior, not chase a number blindly.
- Critical business rules require regression coverage.
- New bugs should usually add a regression test.

## Regression Tests

- Add a regression test when fixing a defect.
- Name the test around the behavior that must not break again.
- Keep the test focused on the failing scenario.

## Validation Checklist

- Unit tests pass.
- Integration or end-to-end tests pass when relevant.
- Build and lint pass when available.
- Manual verification is documented when automated coverage is not enough.

## Test Gaps

If tests cannot be added or run, document the reason and the residual risk.
