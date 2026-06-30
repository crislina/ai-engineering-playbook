# Context Routing

## Purpose

This document defines how AI assistants should discover and load engineering knowledge from this repository.

The goal is to maximize relevant context while minimizing unnecessary token usage.

Do not load the entire knowledge base. Load only the documents required to complete the current task.

---

# General Principles

## Understand before loading

Do not immediately search through all documentation.

First understand:

* What is the user trying to accomplish?
* What engineering problem needs to be solved?
* Which technologies are involved?

Only after understanding the task should additional knowledge be loaded.

---

## Load incrementally

Start with the minimum required knowledge.

Load additional documents only when new questions arise.

Avoid loading documents "just in case."

---

## Prefer concepts before implementations

When solving an engineering problem:

1. Load shared engineering concepts.
2. Then load language-specific implementations.
3. Finally load framework-specific guidance if required.

Example:

```text
REST API
  -> API Design
  -> DTO
  -> Validation
  -> Spring Boot
```

---

## Ignore unrelated technologies

Never load knowledge that is unrelated to the current task.

Examples:

Do not load:

* Kubernetes
* Docker
* MongoDB

when implementing a Java DTO.

---

# Step 1 - Classify the Task

Determine the primary engineering task.

Typical categories include:

* Architecture Design
* Feature Development
* REST API Development
* Database Design
* Code Review
* Debugging
* Refactoring
* Testing
* Performance Optimization
* Security
* Deployment

If multiple tasks exist, begin with the primary objective.

---

# Step 2 - Identify Required Knowledge

For each task, determine which engineering concepts are required.

Ask:

```text
What knowledge is necessary before implementation?
```

Do not think about programming language first. Think about engineering concepts.

---

## REST API Development

Questions:

* How should the API be designed?
* Does data cross application boundaries?
* Is input validation required?
* How should errors be returned?
* Does authentication apply?
* Is versioning required?

Possible knowledge:

* `backend/shared/api-design.md`
* `backend/shared/dto.md`
* `backend/shared/validation.md`
* `backend/shared/error-handling.md`
* `backend/shared/authentication.md`
* `backend/shared/versioning.md`

Only after these concepts are understood should language-specific guidance be loaded.

---

## Database Design

Questions:

* Relational or document database?
* Schema evolution required?
* Index strategy required?
* Data consistency requirements?

Possible knowledge:

* `database/schema-design.md`
* `database/migration-strategy.md`
* `database/index-strategy.md`

Then load technology-specific guidance such as:

* `database/postgres/postgres.md`
* `database/mysql/README.md`
* `database/mongodb/README.md`

depending on the selected technology.

---

## Code Review

Questions:

* Is this a design issue?
* Is this a coding style issue?
* Is this a security issue?
* Is this a testing issue?
* Is this a performance issue?

Possible knowledge:

* `global/review-checklist.md`
* `global/coding-principles.md`
* Relevant shared concept files
* Relevant technology-specific files

Load only the knowledge relevant to the review. Avoid loading every coding standard.

---

## Debugging

Questions:

* Is the problem functional?
* Performance?
* Infrastructure?
* Database?
* Networking?

Begin with the most relevant shared guidance, such as logging, observability, testing, or error handling.

Expand only if necessary.

---

## Security

Questions:

* Authentication?
* Authorization?
* Secrets?
* Input validation?
* SQL injection?
* XSS?
* CSRF?

Possible knowledge:

* `backend/shared/authentication.md`
* `backend/shared/authorization.md`
* `backend/shared/validation.md`
* `backend/shared/error-handling.md`

Load only the applicable security guidance.

---

# Step 3 - Select Implementation Guidance

After engineering concepts are understood, determine the implementation technology.

Examples:

Java:

* `backend/java/`

Go:

* `backend/go/`

Python:

* `backend/python/`

React:

* `frontend/react/`

Angular:

* `frontend/angular/`

Technology guidance should refine implementation, not replace engineering principles.

---

# Step 4 - Expand Context Only When Necessary

If implementation reveals additional concerns, load additional knowledge.

Examples:

```text
REST API
  -> Need authentication
  -> Load backend/shared/authentication.md
```

Do not load the entire backend folder.

```text
Spring Boot
  -> Need database optimization
  -> Load relevant database performance or indexing guidance
```

Do not load all database documentation.

---

# Decision Rules

When deciding whether to load a document, ask:

```text
Will this document directly improve the current task?
```

If no, do not load it.

---

Ask:

```text
Can this question be answered using knowledge already loaded?
```

If yes, do not load additional documentation.

---

Ask:

```text
Does the implementation require language-specific behavior?
```

If yes, load language guidance. Otherwise, remain at the shared engineering level.

---

# Context Budget

Treat context as a limited resource.

Every loaded document should provide meaningful value.

Prefer:

* focused documents
* reusable engineering concepts
* concise guidance

Avoid:

* large reference manuals
* duplicated knowledge
* unrelated documentation

High signal. Low token cost.

---

# Guiding Philosophy

The objective is not to read more.

The objective is to load the right knowledge at the right time.

Effective context selection is more valuable than a large context window.
