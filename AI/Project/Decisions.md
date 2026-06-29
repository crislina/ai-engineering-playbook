# Decisions

## Purpose

Record important project decisions so future contributors understand the context.

## Decision Log

### 2026-06-29: Initial Playbook Structure

Status: Accepted

Decision: Organize guidance into `AI/Global`, `AI/Backend`, `AI/Frontend`, and `AI/Project`, with `CLAUDE.md` as the main index.

Reason: The structure separates universal collaboration rules from technology-specific and project-specific guidance.

Consequences:

- Contributors can find relevant rules quickly.
- Future project templates can copy only the sections they need.

### 2026-06-29: Use Markdown as the Source of Truth

Status: Accepted

Decision: Store the playbook as Markdown files rather than a database, wiki, or generated site.

Reason: Markdown is easy to review, version, copy, and use directly by AI assistants.

Consequences:

- Changes are visible in git history.
- Documentation can evolve without application infrastructure.

### Pending: JSONB Usage

Status: Template

Decision: Use JSONB only when flexible semi-structured data is necessary and relational modeling would create unnecessary churn.

Reason: JSONB can reduce schema friction, but overuse hides important domain concepts and weakens constraints.

Consequences:

- JSONB fields need clear ownership, validation, and indexing rules.
- Important queryable data should remain relational.

### Pending: MongoDB

Status: Template

Decision: Do not use MongoDB unless document storage is a clear project requirement.

Reason: Relational data, transactions, reporting, and migrations are often easier to manage in PostgreSQL for business applications.

Consequences:

- Avoids unnecessary operational complexity.
- Revisit if the domain becomes document-first.

### Pending: Redis

Status: Template

Decision: Do not introduce Redis unless caching, distributed locking, rate limiting, or queue-like behavior is required.

Reason: Redis adds infrastructure and consistency considerations.

Consequences:

- Start without Redis.
- Add only with measured need and documented invalidation strategy.

### Pending: Kafka

Status: Template

Decision: Do not introduce Kafka unless event streaming, asynchronous integration, or high-volume event processing is required.

Reason: Kafka adds significant operational and design complexity.

Consequences:

- Prefer simple synchronous or job-based flows first.
- Revisit when event volume, ordering, or decoupling requirements justify it.
