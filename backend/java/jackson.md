# Jackson

## Purpose

Guide JSON serialization and deserialization in Java services.

## Rules

- Keep JSON shape explicit through DTOs.
- Avoid exposing entities directly to Jackson.
- Use clear property names that match API vocabulary.
- Be intentional with date, time, enum, and nullable field handling.
- Avoid global serializer changes unless all API consumers can accept the behavior.
