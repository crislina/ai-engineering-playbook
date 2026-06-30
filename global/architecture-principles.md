# Architecture Principles

## Purpose

Guide technical decisions so systems remain understandable as they grow.

## Principles

- Separate business rules from frameworks and infrastructure.
- Keep domain concepts stable and explicit.
- Prefer use-case-oriented design over database-oriented design.
- Let outer layers depend on inner layers, not the reverse.
- Keep architecture decisions visible through an ADR or project decision log.

## Layer Responsibilities

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
