# JPA

## Purpose

Guide Java Persistence API usage.

## Principles

- Model entity relationships intentionally.
- Keep persistence annotations out of API DTOs.
- Avoid exposing entities directly through public APIs.
- Prefer clear repository methods for common access patterns.
- Use transactions around use cases that modify persistent state.

## Querying

- Avoid N+1 query patterns.
- Fetch only needed data.
- Use projections when full entities are unnecessary.
- Test complex queries with representative data.
