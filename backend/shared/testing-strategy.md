# Testing Strategy

## Purpose

Set backend validation expectations independent of framework.

## Strategy

- Test business rules directly at the service or domain level.
- Use integration tests for cross-module contracts and critical workflows.
- Verify request validation, status codes, response shape, and error responses at API boundaries.
- Add regression tests when fixing defects.

## Coverage

- Coverage should protect important behavior, not chase a number blindly.
- Critical business rules require regression coverage.
- If tests cannot be added or run, document the reason and residual risk.
