# API Versioning

Load when evolving a public contract.

- Prefer additive compatible changes.
- Treat removed/renamed fields, changed meaning, stricter accepted input, and altered status/error behavior as compatibility risks.
- Follow one project-selected versioning mechanism; do not introduce a new mechanism locally.
- When a break is required, define coexistence, deprecation signal, migration path, and removal trigger.
- Internal implementation versions do not belong in public API versions.
