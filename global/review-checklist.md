# Review Checklist

Use this checklist during code review, AI review, and pre-merge self-review.

## Architecture

- [ ] Responsibility is in the correct layer.
- [ ] No circular dependency exists.
- [ ] Architecture changes are documented.
- [ ] Shared concepts and technology-specific implementation details are separated.

## Code Quality

- [ ] Naming is clear and matches domain vocabulary.
- [ ] Methods are small and focused.
- [ ] Classes and modules have clear responsibility.
- [ ] Abstractions are useful and not over-engineered.
- [ ] Existing project style and patterns are followed.

## API

- [ ] Resource naming is consistent.
- [ ] HTTP status codes are correct.
- [ ] Request validation exists.
- [ ] Error response format is consistent.
- [ ] DTOs are used for request and response boundaries.
- [ ] Entities are not exposed directly.

## Database

- [ ] Migration exists when schema changes are made.
- [ ] Migration strategy is additive or documented.
- [ ] Indexes are considered for filters, joins, and sorting.
- [ ] Nullable fields are intentional.
- [ ] No obvious N+1 query exists.

## Security

- [ ] Input is validated.
- [ ] Injection risks are controlled through safe APIs.
- [ ] Internal errors are not exposed to clients.
- [ ] Sensitive information is not logged.
- [ ] Secrets are not committed.

## Testing

- [ ] Unit tests are added or updated when behavior changes.
- [ ] Important success and failure paths are covered.
- [ ] Regression tests are added for bug fixes.
- [ ] Existing tests pass.
- [ ] Skipped tests are explained with residual risk.
