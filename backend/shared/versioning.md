# Versioning

## Purpose

Manage API and contract evolution without surprising clients.

## Principles

- Version public APIs when breaking changes are possible.
- Prefer additive changes when practical.
- Document deprecation windows and migration paths.
- Keep old and new behavior clearly separated during transitions.

## Common Approaches

- URI versioning, such as `/api/v1`.
- Header-based versioning.
- Media-type versioning.

Choose one convention per project and apply it consistently.
