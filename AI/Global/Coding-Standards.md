# Coding Standards

## Purpose

Capture shared engineering expectations across languages and frameworks.

## General Principles

- Optimize for readability, maintainability, and correctness.
- Keep functions and modules focused on one responsibility.
- Use descriptive names that reflect domain intent.
- Prefer explicit behavior over clever shortcuts.
- Handle errors close to the boundary where they can be understood.

## Naming

- Class names use nouns and reflect responsibility.
- Method names use verbs and describe behavior.
- Boolean names should read like predicates, such as `isActive`, `hasPermission`, or `shouldRetry`.
- Avoid vague names such as `data`, `info`, `manager`, `helper`, or `util` unless the meaning is obvious.
- Domain names should match `AI/Project/Domain.md`.

## Java Style

- Follow the project's formatter.
- Prefer constructor injection.
- Prefer immutable values where practical.
- Avoid static mutable state.
- Keep null handling explicit.
- Use meaningful exceptions instead of swallowing errors.

## DTO

- DTOs define API input and output contracts.
- DTO names should end with `Request`, `Response`, `Dto`, or a more specific domain suffix.
- Do not put business logic in DTOs.
- Validate request DTOs at the boundary.
- Do not expose entities directly as API responses.

## Package

- Package names should reflect feature, domain, or layer consistently.
- Avoid catch-all packages such as `common` unless the content is genuinely shared.
- Keep controller, service, repository, DTO, config, and exception responsibilities clear.

## Controller

- Controllers handle HTTP input and output only.
- Controllers validate, map, delegate, and return responses.
- Controllers should not contain business rules.

## Service

- Services contain business logic and orchestration.
- Services own transaction boundaries when database changes are involved.
- Services should depend on abstractions or repositories, not controllers.

## Repository

- Repositories handle persistence only.
- Repository methods should describe data access intent.
- Complex queries should be named, tested, and documented when needed.

## Comments

- Comments should explain why, not repeat what the code does.
- Avoid stale comments.
- Add comments for non-obvious business rules, trade-offs, and temporary decisions.

## Method Length

- Keep methods short enough to understand without scrolling excessively.
- Extract private methods when they clarify intent.
- Avoid extraction that only hides straightforward logic.

## Class Responsibility

- Each class should have one primary reason to change.
- Avoid service classes that mix validation, persistence, mapping, external calls, and formatting without clear structure.
- Split responsibilities when behavior becomes difficult to test.
