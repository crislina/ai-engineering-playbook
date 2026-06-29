# Architecture

## Purpose

Guide technical decisions so the system stays understandable as it grows.

## Clean Architecture

- Separate business rules from frameworks and infrastructure.
- Keep domain concepts stable and explicit.
- Let outer layers depend on inner layers, not the reverse.
- Prefer use-case-oriented design over database-oriented design.

## Layer Responsibility

### Controller Layer

- Owns transport concerns.
- Accepts requests and returns responses.
- Delegates business decisions to services.

### Service Layer

- Owns business logic.
- Coordinates repositories, external clients, and domain operations.
- Owns transactions for business use cases.

### Repository Layer

- Owns persistence access.
- Hides query and storage details from service logic.
- Does not contain business rules.

### Entity Layer

- Represents persisted domain state.
- Should not be exposed directly through public APIs.
- Should not depend on controllers or API DTOs.

### DTO Layer

- Defines boundary contracts.
- Keeps API shape separate from persistence shape.
- Can change independently from entities when API requirements evolve.

## Dependency Rule

- Controllers may depend on services and DTOs.
- Services may depend on repositories, domain objects, and external client abstractions.
- Repositories may depend on persistence frameworks.
- Entities must not depend on controllers, HTTP, UI, or external transport concerns.

## Design Rules

- Business logic belongs in services or domain operations, not controllers or repositories.
- Never expose entities directly in API responses.
- Prefer composition over inheritance.
- Prefer explicit mapping between DTOs and entities.
- Keep architecture changes visible in `AI/Project/Decisions.md`.
- Do not introduce a new architectural pattern without approval.

## Documentation

Record meaningful architecture choices in `AI/Project/Decisions.md`.
