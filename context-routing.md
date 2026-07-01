
# Loading Strategy

## Lazy Mode

Always load:

- Global Guardrails
- Project Guardrails
- Project Overview

Load all other context only when required by task routing.

---

## Eager Mode

Always load:

- Global Guardrails
- Project Guardrails
- Project Overview
- Global Development
- Matching Stack Context

Load additional project context according to task routing.


## Routing Protocol

1. Read `CLAUDE.md`.
2. Identify `context.loading_mode`.
3. Identify `project.stacks`.
4. Load baseline context based on loading mode.
5. Identify the task type.
6. Load task-specific context according to the routing table.
7. Load only stack context that matches `project.stacks`.
8. Do not load unrelated stack context.

Do not load a file for familiar baseline practice, broad background, or possible future work. Prefer the most specific file when rules overlap.

## Routes

```text
End-to-end feature
  -> global/workflow.md
  -> Changes module or dependency boundaries?
       -> architecture/boundaries.md
  -> Has HTTP behavior?
       -> backend/api/api-routing.md
  -> Coordinates business workflow or transactions?
       -> backend/persistence/service-layer.md
  -> Reads or writes stored data?
       -> backend/persistence/repository.md
  -> Changes stored shape?
       -> database/schema.md
       -> Schema migration? -> database/migrations.md
  -> Has user-facing UI?
       -> Follow the Frontend route
  -> Needs runtime diagnostics?
       -> platform/observability.md
  -> Stop

REST API
  -> backend/api/api-routing.md
  -> Has request/response contracts? -> backend/api/dto.md
  -> Has boundary input?             -> backend/api/validation.md
  -> Needs custom failures?          -> backend/api/errors.md
  -> Identifies actors?              -> backend/api/authentication.md
  -> Restricts actions/data?         -> backend/api/authorization.md
  -> Returns collections?            -> backend/api/pagination.md
  -> Changes a public contract?       -> backend/api/versioning.md
  -> Needs Java/Spring detail?        -> backend/java/spring.md
  -> Stop

Persistence
  -> backend/persistence/repository.md
  -> Orchestrates a use case/transaction? -> backend/persistence/service-layer.md
  -> Java ORM behavior?                   -> backend/java/persistence.md
  -> Changes stored shape?                -> database/schema.md
  -> Schema migration?                    -> database/migrations.md
  -> Query performance?                   -> database/indexes.md
  -> PostgreSQL behavior?                 -> database/postgres.md
  -> Stop

Frontend
  -> Component behavior?      -> frontend/components.md
  -> State ownership?         -> frontend/state.md
  -> Navigation or URL state? -> frontend/routing.md
  -> Interactive UI?          -> frontend/accessibility.md
  -> Multiple viewports?      -> frontend/responsive.md
  -> React-specific behavior? -> frontend/react.md
  -> Stop

Database
  -> database/schema.md
  -> Schema change?       -> database/migrations.md
  -> Query performance?   -> database/indexes.md
  -> PostgreSQL behavior? -> database/postgres.md
  -> Stop

Delivery or operations
  -> CI, release, or deployment? -> platform/delivery.md
  -> Runtime diagnostics?        -> platform/observability.md
  -> Container image?            -> platform/containers.md
  -> Kubernetes behavior?        -> platform/orchestration.md
  -> Terraform infrastructure?   -> platform/iac.md
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
