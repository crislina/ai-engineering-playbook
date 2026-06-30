# Migrations

Load for production schema or data changes.

- Prefer additive, backward-compatible evolution.
- Keep applied migration files immutable.
- Separate long-running backfills from schema changes when practical.
- During rolling delivery, keep schema compatible with both old and new application versions.
- For destructive changes, stage read/write transitions and define verification plus rollback or forward-fix.
- Test lock behavior, duration, and representative data volume when risk is material.
