# AI Engineering Playbook

## Vision

As AI coding assistants become part of everyday software engineering, project knowledge should be organized for both humans and AI.

Traditional engineering documentation is written for people. AI assistants, however, benefit from modular, structured, and reusable knowledge.

The goal of AI Engineering Playbook is to provide an opinionated, AI-friendly engineering knowledge base that can be reused across projects, teams, languages, and AI tools.

This repository intentionally contains only reusable engineering knowledge. Project-specific documentation belongs in a separate private repository.

---

# Core Principles

## AI-first Documentation

Documentation should not only explain engineering decisions to developers, but also provide enough context for AI assistants to produce consistent, high-quality output.

Documentation becomes executable knowledge.

---

## Modular Knowledge

Avoid large documents covering many unrelated topics.

Instead of:

* Coding-Standards.md

Prefer:

* dto.md
* validation.md
* logging.md
* testing.md

Each document should focus on a single engineering concept.

Small modules are easier for both humans and AI to understand.

---

## Separate Concepts from Implementations

Many engineering concepts are language independent.

For example:

DTO is not a Java feature.

DTO is an architectural pattern.

The Java implementation (records, Jackson, Lombok, MapStruct) belongs to Java-specific documentation.

The concept belongs to shared backend knowledge.

The same principle applies to:

* Repository Pattern
* Service Layer
* API Design
* Validation
* Error Handling
* Logging
* Testing

---

## Prefer Principles over Rules

Instead of documenting only "what to do", explain:

* why the guideline exists
* when it should be applied
* common trade-offs
* recommended practices

AI generally performs better when it understands intent rather than memorizing rules.

---

## Technology-specific Knowledge

Language and framework specific guidance should be isolated.

Examples:

Java

* Spring Boot
* JPA
* Hibernate
* Lombok
* MapStruct

React

* Hooks
* Component composition
* State management

PostgreSQL

* Index design
* Schema evolution
* Query optimization

Keeping these separated allows projects to combine only the knowledge they need.

---

# Repository Structure

```text
ai-engineering-playbook/

CLAUDE.md
readme.md

global/
    ai-collaboration.md
    workflow.md
    architecture-principles.md
    coding-principles.md
    naming-principles.md
    documentation-guidelines.md
    adr.md
    git.md
    review-checklist.md

backend/
    shared/
        api-design.md
        dto.md
        repository-pattern.md
        service-layer.md
        validation.md
        error-handling.md
        authentication.md
        authorization.md
        logging.md
        observability.md
        pagination.md
        versioning.md
        testing-strategy.md
    java/
        spring-boot.md
        jpa.md
        hibernate.md
        bean-validation.md
        jackson.md
        mapstruct.md
        lombok.md
        package-structure.md
        java-coding-style.md
    go/
        README.md
    python/
        README.md
    nodejs/
        README.md

frontend/
    shared/
        component-design.md
        state-management.md
        routing.md
        accessibility.md
        responsive-design.md
        frontend-testing.md
    react/
        react.md
        hooks.md
    angular/
        README.md
    vue/
        README.md

database/
    naming-convention.md
    index-strategy.md
    migration-strategy.md
    schema-design.md
    performance-optimization.md
    postgres/
        postgres.md
    mysql/
        README.md
    mongodb/
        README.md
    redis/
        README.md

infra/
    ci-cd.md
    monitoring.md
    deployment-strategies.md
    docker/
        docker.md
    kubernetes/
        kubernetes.md
    terraform/
        terraform.md
```

---

# Suggested Content

## global

General engineering principles.

Possible topics:

* Architecture Principles
* AI Collaboration Guidelines
* Coding Principles
* Naming Principles
* Documentation Guidelines
* Architecture Decision Records (ADR)

---

## backend/shared

Concepts independent of programming language.

Possible topics:

* API Design
* DTO
* Repository Pattern
* Service Layer
* Validation
* Error Handling
* Authentication Concepts
* Authorization Concepts
* Logging
* Observability
* Pagination
* Versioning
* Testing Strategy

---

## backend/java

Java implementation details.

Possible topics:

* Spring Boot
* JPA
* Hibernate
* Bean Validation
* Jackson
* MapStruct
* Lombok
* Package Structure
* Java Coding Style

---

## frontend/shared

Frontend engineering concepts.

Possible topics:

* Component Design
* State Management
* Routing
* Accessibility
* Responsive Design
* Frontend Testing

---

## database

Database-specific knowledge.

Possible topics:

* Naming Convention
* Index Strategy
* Migration Strategy
* Schema Design
* Performance Optimization

Each database technology may provide additional guidance.

---

## infra

Infrastructure and platform engineering.

Possible topics:

* Docker
* Kubernetes
* CI/CD
* Infrastructure as Code
* Cloud Platform Guidelines
* Monitoring
* Alerting
* Deployment Strategies

---

# Design Philosophy

When adding documentation, ask two questions.

**Would this still be true if the programming language changed?**

If yes, place it under a shared module.

---

**Would this still be true if the project changed?**

If yes, it belongs in AI Engineering Playbook.

Otherwise, it belongs in the project's private repository.

---

# Long-term Vision

AI Engineering Playbook is not intended to replace project documentation.

Instead, it provides reusable engineering knowledge that can be shared across organizations, projects, and AI assistants.

The objective is to establish a consistent engineering foundation so that both humans and AI begin every project with the same understanding of architecture, engineering principles, and best practices.
