# Review Routing

Start from changed behavior and failure modes. Load only topic files implicated by the diff.

- Correctness: edge cases, error paths, concurrency, compatibility.
- Boundaries: ownership, dependency direction, leaked persistence or transport models.
- Security: trust boundaries, authorization, secrets, sensitive output.
- Data: migration compatibility, constraints, query count, indexes.
- API/UI: contract stability, all user-visible states, accessibility.
- Validation: regression coverage and meaningful tests for changed behavior.
- Operations: observability, rollout, rollback, and dependency failure.

Report actionable findings first, ordered by severity and tied to locations. Do not inflate the review with generic style advice already enforced by tools.
