# Validation

Load when input has constraints or a use case has preconditions.

- Boundary validation owns shape, required values, ranges, length, and format.
- Use-case or domain validation owns business rules and current-state checks.
- Database constraints protect persisted invariants and race-sensitive uniqueness.
- Do not duplicate a rule across layers unless each layer protects a distinct boundary.
- Return field details and stable codes only when clients can use them.
- Never expose exception classes or stack traces.
