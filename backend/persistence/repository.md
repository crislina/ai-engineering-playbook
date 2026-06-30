# Repository Boundary

Load when defining data access.

- Repository operations express persistence intent in domain/use-case vocabulary.
- Repositories own query, storage, and mapping mechanics; they do not decide business policy.
- Return only data required by the caller when full entities are unnecessary.
- Name and test complex queries; make ordering and cardinality explicit.
- Do not add a repository abstraction when the project's existing data-access boundary already serves the same purpose.
