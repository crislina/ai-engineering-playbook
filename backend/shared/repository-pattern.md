# Repository Pattern

## Purpose

Separate persistence access from business logic.

## Responsibilities

- Repositories own data access.
- Repositories hide query and storage details from service logic.
- Repository methods should describe data access intent.
- Complex queries should be named, tested, and documented when needed.

## Boundaries

- Repositories should not contain business rules.
- Services or domain operations decide what should happen.
- Repositories decide how data is loaded or persisted.
