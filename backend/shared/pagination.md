# Pagination

## Purpose

Keep collection APIs predictable, performant, and safe for large data sets.

## Rules

- Use pagination for collection endpoints.
- Enforce maximum page size.
- Include page, size, total count, and sorting metadata when relevant.
- Prefer stable ordering so results do not shift unexpectedly.
- Document cursor-based pagination when offset pagination is not sufficient.
