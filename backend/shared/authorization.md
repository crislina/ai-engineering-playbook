# Authorization Concepts

## Purpose

Define reusable authorization concepts independent of a specific framework.

## Principles

- Authorization decides what an authenticated or anonymous actor may do.
- Check permissions close to the boundary of the protected use case.
- Prefer explicit policies over scattered conditionals.
- Deny by default when permission is unclear.
- Keep authorization failures distinguishable from authentication failures.

## Data Access

- Apply authorization to both actions and data visibility.
- Avoid relying only on frontend checks.
- Test permission boundaries for sensitive workflows.
