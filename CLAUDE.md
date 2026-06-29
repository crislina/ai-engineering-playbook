# AI Index

This repository is an AI engineering playbook. Before making changes, Claude or any AI assistant must read the relevant files below and follow the rule priority at the end of this document.

## Global Rules

Read these first for every task:

- [Workflow](AI/Global/Workflow.md)
- [AI Collaboration](AI/Global/AI-Collaboration.md)
- [Coding Standards](AI/Global/Coding-Standards.md)
- [Architecture](AI/Global/Architecture.md)
- [Git](AI/Global/Git.md)
- [Testing](AI/Global/Testing.md)
- [Documentation](AI/Global/Documentation.md)
- [Review Checklist](AI/Global/Review-Checklist.md)

---

## Backend

Use these when backend work is involved:

- [Spring Boot](AI/Backend/SpringBoot.md)
- [API](AI/Backend/API.md)
- [Database](AI/Backend/Database.md)
- [Error Handling](AI/Backend/Error-Handling.md)

---

## Frontend

Use these when frontend work is involved:

- [UI Principles](AI/Frontend/UI-Principles.md)
- [React](AI/Frontend/React.md)
- [Components](AI/Frontend/Components.md)

---

## Current Project

Read these to understand the current product context:

- [Overview](AI/Project/Overview.md)
- [Domain](AI/Project/Domain.md)
- [Roadmap](AI/Project/Roadmap.md)
- [Decisions](AI/Project/Decisions.md)
- [POC](AI/Project/POC.md)
- [Out of Scope](AI/Project/Out-of-Scope.md)

---

## Rule Priority

1. Read all Global documents before planning.
2. Read Backend or Frontend documents relevant to the task.
3. Read all Project documents before changing project behavior.
4. Follow AI Collaboration rules first.
5. Wait for approval before implementation when the task changes code, architecture, scope, or product behavior.
6. If conflicts exist, apply this priority:
   AI Collaboration > Workflow > Project Decisions > Other documents.
