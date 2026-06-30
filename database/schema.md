# Schema Design

Load when stored data shape or invariants change.

- Model durable domain concepts explicitly.
- Protect essential invariants with constraints, including race-sensitive uniqueness.
- Make nullability, ownership, deletion, retention, and audit behavior intentional.
- Choose normalization or duplication from access and consistency requirements, not convenience alone.
- Do not use unstructured fields to postpone modeling important concepts.
- Record project naming and compatibility conventions in project rules.
