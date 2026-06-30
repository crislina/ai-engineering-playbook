# Architecture Boundaries

Load when defining modules, dependencies, or public contracts.

- Dependencies point toward stable business policy, not transport or storage details.
- Keep transport, domain/use-case, persistence, and external-client models separate when they evolve for different reasons.
- Cross a boundary through an explicit contract; keep framework types inside their owning adapter.
- Prevent cycles and broad `common` modules that become unowned dependencies.
- Add an abstraction only when it isolates volatility, enables substitution, or removes meaningful duplication.

Project architecture and exceptions belong in project rules or ADRs.
