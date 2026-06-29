# Spring Boot

## Purpose

Guide Spring Boot backend implementation.

## Package

- Use a consistent package structure by feature or layer.
- Keep controllers, services, repositories, DTOs, config, exceptions, and clients easy to locate.
- Avoid placing unrelated shared code into broad `common` packages.

## Bean

- Prefer constructor injection.
- Avoid field injection.
- Keep bean creation explicit when configuration matters.
- Do not create beans with hidden side effects during startup.

## Configuration

- Prefer typed configuration properties.
- Keep environment-specific values outside source control.
- Document required environment variables.
- Use `@Configuration` for framework wiring, not business logic.
- Keep configuration classes small and focused.

## Transaction

- Use `@Transactional` at service or use-case boundaries.
- Prefer read-only transactions for query use cases.
- Avoid long-running transactions around external network calls.
- Be explicit about rollback behavior when it differs from defaults.

## Validation

- Validate request DTOs at controller boundaries.
- Use Bean Validation for structural validation.
- Put business validation in services.
- Return consistent validation errors.

## Controller

- Keep controllers thin.
- Map HTTP request and response only.
- Delegate business behavior to services.

## Service

- Keep business rules and orchestration in services.
- Keep services testable without starting the full application.

## Repository

- Use repositories for persistence access only.
- Keep custom queries named and tested when complex.

## Testing

- Use unit tests for service logic.
- Use slice tests for controllers and repositories when useful.
- Use integration tests for important application flows.
