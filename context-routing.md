# Context Routing

Load the fewest rules that can change the result. Do not preload the repository.

## Routing Protocol

1. Classify the task and technologies from the request and repository.
2. Load one primary concept file from the routes below.
3. At each decision gate, load a dependency only when the task needs it.
4. Load technology guidance only for implementation details not already settled.
5. Stop when loaded knowledge is sufficient.

Do not load a file for familiar baseline practice, broad background, or possible future work. Prefer the most specific file when rules overlap.

## Routes

```text
REST API
  -> backend/api/api-routing.md
  -> Has request/response contracts? -> dto.md
  -> Has boundary input?             -> validation.md
  -> Needs custom failures?          -> errors.md
  -> Identifies actors?              -> authentication.md
  -> Restricts actions/data?         -> authorization.md
  -> Returns collections?            -> pagination.md
  -> Changes a public contract?       -> versioning.md
  -> Needs Java/Spring detail?        -> backend/java/spring.md
  -> Stop

Persistence
  -> backend/persistence/repository.md
  -> Orchestrates a use case/transaction? -> service-layer.md
  -> Java ORM behavior?                   -> backend/java/persistence.md
  -> Schema/query concern?                -> relevant database file
  -> Stop

Frontend
  -> relevant frontend concept file
  -> React-specific behavior? -> frontend/react.md
  -> Stop

Database
  -> database/schema.md
  -> Schema change?       -> migrations.md
  -> Query performance?   -> indexes.md
  -> PostgreSQL behavior? -> postgres.md
  -> Stop

Delivery or operations
  -> relevant platform file only
  -> Stop

Code review
  -> global/review.md
  -> load only files implicated by the diff
  -> Stop
```

For architecture decisions load `architecture/boundaries.md`; add `architecture/layering.md` only when layer ownership is disputed. For substantial collaboration or execution rules, load the matching file under `global/`.

Use [`ai-index.md`](ai-index.md) only when no route matches or when discovering available topics.

## Priority

Project rules and explicit user instructions override this reusable playbook. Within this repository:

```text
context routing > task-specific concept > technology guidance > review checklist
```

If two loaded rules duplicate each other, apply the more specific rule once.
