# Validation

## Purpose

Keep validation consistent across request boundaries, business rules, and persistence constraints.

## Layers

- Validate request structure at API boundaries.
- Validate business rules in services or domain operations.
- Enforce essential invariants with database constraints when persistence is involved.

## Error Reporting

- Return field-level details when useful.
- Use stable machine-readable error codes when clients need branching behavior.
- Do not expose internal exception names or stack traces.
