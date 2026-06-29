# Review Checklist

Use this checklist during code review, AI review, and pre-merge self-review. Each item should be checked against the approved scope of the task.

## 1. Architecture

- [ ] Responsibility is in the correct layer.
- [ ] Controller contains no business logic.
- [ ] Service owns business rules.
- [ ] Repository only accesses persistence.
- [ ] DTOs, entities, services, and repositories are clearly separated.
- [ ] No circular dependency exists.
- [ ] Design follows project architecture.
- [ ] Architecture changes are documented and approved.

## 2. Code Quality

- [ ] Naming is clear and matches domain vocabulary.
- [ ] Methods are small and focused.
- [ ] Classes have a clear responsibility.
- [ ] No unnecessary duplicated code exists.
- [ ] Code is easy to understand.
- [ ] Abstraction is useful and not over-engineered.
- [ ] Comments are used only when necessary.
- [ ] Existing project style and patterns are followed.

## 3. API

- [ ] REST naming is consistent.
- [ ] HTTP status codes are correct.
- [ ] Request validation exists.
- [ ] Error response format is consistent.
- [ ] DTOs are used for request and response boundaries.
- [ ] Entities are not exposed directly.
- [ ] API behavior is backward compatible or the breaking change is approved.
- [ ] Pagination, filtering, sorting, and versioning are handled when relevant.

## 4. Database

- [ ] Flyway migration exists when schema changes are made.
- [ ] Migration is additive or rollback/forward-fix strategy is documented.
- [ ] JSONB structure is consistent and validated when JSONB is used.
- [ ] Indexes are considered for filters, joins, and sorting.
- [ ] Nullable fields are intentional.
- [ ] No unnecessary query exists.
- [ ] No obvious N+1 query exists.
- [ ] Data constraints are enforced where appropriate.

## 5. Security

- [ ] Input is validated.
- [ ] SQL injection is prevented through parameterized queries or safe ORM usage.
- [ ] Internal errors are not exposed to clients.
- [ ] Sensitive information is not logged.
- [ ] Secrets are not committed.
- [ ] Permissions and data access are appropriately limited when applicable.
- [ ] Error messages are useful but do not leak implementation details.

## 6. Testing

- [ ] Unit tests are added or updated.
- [ ] Happy path is tested.
- [ ] Invalid input is tested.
- [ ] Edge cases are considered.
- [ ] Regression tests are added for bug fixes.
- [ ] Existing tests pass.
- [ ] Skipped tests are explained with residual risk.

## 7. Performance

- [ ] No unnecessary database query exists.
- [ ] No obvious N+1 query exists.
- [ ] No repeated JSON parsing exists in hot paths.
- [ ] Algorithm is efficient enough for expected data size.
- [ ] Expensive frontend renders or backend operations are controlled.
- [ ] Pagination or limits are used for large data sets.

## 8. Maintainability

- [ ] Code is easy to extend.
- [ ] Coupling is low.
- [ ] Cohesion is high.
- [ ] Configuration is preferred over hardcoding.
- [ ] Behavior is easy to understand.
- [ ] Logging levels are appropriate.
- [ ] Correlation ID or request context is preserved when relevant.
- [ ] Future enhancements are documented instead of half-implemented.
