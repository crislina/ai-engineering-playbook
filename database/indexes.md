# Query and Index Strategy

Load when a query is slow, high-volume, or newly introduced on a critical path.

- Start from actual filter, join, ordering, and cardinality patterns.
- Inspect the query plan and measured workload before adding complexity.
- Design composite index column order for the real predicates and sort.
- Fetch only required columns and bound large results.
- Avoid duplicate or unused indexes that add write and storage cost.
- Re-evaluate plans as data distribution and product behavior change.
