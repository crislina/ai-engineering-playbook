# Spring Boot

## Purpose

Guide Spring Boot backend implementation.

## Beans

- Prefer constructor injection.
- Avoid field injection.
- Keep bean creation explicit when configuration matters.
- Do not create beans with hidden side effects during startup.

## Configuration

- Prefer typed configuration properties.
- Keep environment-specific values outside source control.
- Document required environment variables in the consuming project.
- Use `@Configuration` for framework wiring, not business logic.

## Transactions

- Use `@Transactional` at service or use-case boundaries.
- Prefer read-only transactions for query use cases.
- Avoid long-running transactions around external network calls.
- Be explicit about rollback behavior when it differs from defaults.

## Testing

- Use unit tests for service logic.
- Use slice tests for controllers and repositories when useful.
- Use integration tests for important application flows.
