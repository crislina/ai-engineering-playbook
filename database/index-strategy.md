# Index Strategy

## Purpose

Use indexes intentionally to support important query paths.

## Rules

- Add indexes for frequent filters, joins, and ordering.
- Avoid unused indexes that slow writes.
- Review query plans for important paths.
- Consider composite indexes based on real query patterns.
- Revisit indexes as product behavior and data volume change.
