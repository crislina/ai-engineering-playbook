# Service Layer

## Purpose

Describe the layer that owns application use cases and business orchestration.

## Responsibilities

- Own business logic and use-case flow.
- Coordinate repositories, domain objects, and external client abstractions.
- Own transaction boundaries when database changes are involved.
- Translate domain outcomes into application-level results.

## Rules

- Controllers should delegate business decisions to services.
- Services should not depend on controllers or transport concerns.
- Services should remain testable without starting the full application.
