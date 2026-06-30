# AI Index

This repository is a reusable AI engineering playbook. Before making changes, AI assistants should read the relevant files below and follow the rule priority at the end of this document.

## Global

Read these first for every task:

- [AI Collaboration](global/ai-collaboration.md)
- [Workflow](global/workflow.md)
- [Architecture Principles](global/architecture-principles.md)
- [Coding Principles](global/coding-principles.md)
- [Naming Principles](global/naming-principles.md)
- [Documentation Guidelines](global/documentation-guidelines.md)
- [ADR Guidelines](global/adr.md)
- [Git](global/git.md)
- [Review Checklist](global/review-checklist.md)

---

## Backend Shared

Use these for backend concepts independent of language or framework:

- [API Design](backend/shared/api-design.md)
- [DTO](backend/shared/dto.md)
- [Repository Pattern](backend/shared/repository-pattern.md)
- [Service Layer](backend/shared/service-layer.md)
- [Validation](backend/shared/validation.md)
- [Error Handling](backend/shared/error-handling.md)
- [Authentication](backend/shared/authentication.md)
- [Authorization](backend/shared/authorization.md)
- [Logging](backend/shared/logging.md)
- [Observability](backend/shared/observability.md)
- [Pagination](backend/shared/pagination.md)
- [Versioning](backend/shared/versioning.md)
- [Testing Strategy](backend/shared/testing-strategy.md)

---

## Backend Java

Use these when Java implementation details are involved:

- [Spring Boot](backend/java/spring-boot.md)
- [JPA](backend/java/jpa.md)
- [Hibernate](backend/java/hibernate.md)
- [Bean Validation](backend/java/bean-validation.md)
- [Jackson](backend/java/jackson.md)
- [MapStruct](backend/java/mapstruct.md)
- [Lombok](backend/java/lombok.md)
- [Package Structure](backend/java/package-structure.md)
- [Java Coding Style](backend/java/java-coding-style.md)

---

## Frontend

Use shared frontend files for framework-independent concepts and React files for React-specific implementation:

- [Component Design](frontend/shared/component-design.md)
- [State Management](frontend/shared/state-management.md)
- [Routing](frontend/shared/routing.md)
- [Accessibility](frontend/shared/accessibility.md)
- [Responsive Design](frontend/shared/responsive-design.md)
- [Frontend Testing](frontend/shared/frontend-testing.md)
- [React](frontend/react/react.md)
- [Hooks](frontend/react/hooks.md)

---

## Database

Use these when schema, migration, or query behavior is involved:

- [Naming Convention](database/naming-convention.md)
- [Schema Design](database/schema-design.md)
- [Migration Strategy](database/migration-strategy.md)
- [Index Strategy](database/index-strategy.md)
- [Performance Optimization](database/performance-optimization.md)
- [PostgreSQL](database/postgres/postgres.md)

---

## Infrastructure

Use these for platform, delivery, and operational work:

- [CI/CD](infra/ci-cd.md)
- [Docker](infra/docker/docker.md)
- [Kubernetes](infra/kubernetes/kubernetes.md)
- [Terraform](infra/terraform/terraform.md)
- [Monitoring](infra/monitoring.md)
- [Deployment Strategies](infra/deployment-strategies.md)

---

## Rule Priority

1. Read global guidance before planning.
2. Read shared concept files before technology-specific files.
3. Read only the technology-specific files relevant to the task.
4. Keep project-specific facts, roadmap, domain rules, and private decisions outside this repository.
5. Follow AI Collaboration and Workflow rules first.
6. If conflicts exist, apply this priority: AI Collaboration > Workflow > Architecture Principles > technology-specific guidance > checklist guidance.
