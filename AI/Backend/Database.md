# Database

## Purpose

Guide schema, query, and migration decisions.

## Flyway

- Use Flyway for database migrations when the project has a relational database.
- Keep migration files immutable after they have been applied outside local development.
- Use clear versioned migration names.
- Separate risky data backfills from schema changes when practical.

## Migration

- Prefer additive migrations.
- Document manual or operational steps.
- Plan rollback or forward-fix strategy.
- Test migrations with representative data when risk is high.

## Naming

- Use clear table, column, index, and constraint names.
- Match domain vocabulary.
- Avoid abbreviations unless they are standard in the domain.

## JSONB

- Use JSONB only for flexible, semi-structured data that does not require frequent relational querying.
- Do not use JSONB to avoid modeling important domain concepts.
- Index JSONB fields intentionally when querying them.
- Document why JSONB is used in `AI/Project/Decisions.md`.

## Index

- Add indexes for frequent filters, joins, and ordering.
- Avoid unused indexes that slow writes.
- Review query plans for important paths.

## Soft Delete

- Use soft delete only when records must be restorable or auditable.
- Ensure queries consistently exclude deleted records.
- Document retention behavior.

## Version

- Use version columns for optimistic locking when concurrent updates matter.
- Make conflict behavior visible through API errors.

## Query Rules

- Avoid N+1 query patterns.
- Fetch only needed data.
- Keep high-traffic queries observable.
