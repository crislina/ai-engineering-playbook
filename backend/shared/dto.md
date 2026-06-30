# DTO

## Purpose

Describe Data Transfer Objects as boundary contracts, independent of language implementation.

## Principles

- DTOs define API input and output contracts.
- DTOs keep external API shape separate from persistence shape.
- DTOs should not contain business logic.
- Request DTOs should be validated at the boundary.
- Entities should not be exposed directly as API responses.

## Naming

- Use names that reveal the boundary and purpose.
- Common suffixes include `Request`, `Response`, `Dto`, or a specific domain boundary suffix.

## Mapping

- Keep mapping explicit enough that API and persistence changes can evolve independently.
- Prefer clear mapping code or mapping tools over implicit coupling.
