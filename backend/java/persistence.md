# JPA and Hibernate

Load when ORM behavior affects correctness or performance.

- Define relationship ownership, cascade, orphan removal, and fetch behavior deliberately.
- Do not rely on open-session-in-view for use-case correctness.
- Prevent N+1 access with projections, entity graphs, fetch joins, or batching chosen for the query.
- Fetch only required data and inspect generated SQL for important paths.
- Keep entity equality and hash behavior stable across transient and persisted states.
- Test complex queries and concurrency behavior with representative persistence.
