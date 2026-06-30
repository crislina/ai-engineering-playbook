# Migration Strategy

## Purpose

Guide safe schema and data changes.

## Rules

- Prefer additive migrations.
- Keep migration files immutable after they have been applied outside local development.
- Use clear versioned migration names.
- Separate risky data backfills from schema changes when practical.
- Plan rollback or forward-fix strategy.
- Test migrations with representative data when risk is high.
