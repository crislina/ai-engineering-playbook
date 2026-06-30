# PostgreSQL

Load only for PostgreSQL-specific behavior.

- Use `jsonb` for genuinely semi-structured data, not to avoid modeling central domain concepts.
- Choose GIN or expression indexes from the actual `jsonb` operators queried.
- Use optimistic versioning, row locks, advisory locks, or transaction isolation according to the conflict being controlled.
- Make lock ordering and retry behavior explicit for contentious workflows.
- Use concurrent index operations and online migration techniques when table size and availability require them.
- Verify important changes with PostgreSQL query plans and production-like statistics.
