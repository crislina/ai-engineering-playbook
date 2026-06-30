# Service Layer

Load when a use case coordinates policy, persistence, or external systems.

- Services/use cases own business orchestration and application outcomes.
- Place database transaction boundaries around the smallest coherent state change.
- Avoid network calls inside database transactions unless consistency requirements justify the lock duration and failure coupling.
- Depend on persistence and external-client contracts, not controllers or transport types.
- Keep use cases testable without starting the full application.
