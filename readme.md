# Project Name: ai-engineering-playbook
# Project Description: A collection of reusable AI collaboration guides, software engineering principles, language-specific best practices and project templates.

# Repo structure:
```
AI/
│
├── Global/
│   ├── Workflow.md
│   ├── AI-Collaboration.md
│   ├── Coding-Standards.md
│   ├── Architecture.md
│   ├── Git.md
│   ├── Testing.md
│   ├── Documentation.md
│   └── Review-Checklist.md
│
├── Backend/
│   ├── SpringBoot.md
│   ├── API.md
│   ├── Database.md
│   └── Error-Handling.md
│
├── Frontend/
│   ├── UI-Principles.md
│   ├── React.md
│   └── Components.md
│
└── Project/
    ├── Overview.md
    ├── Domain.md
    ├── Roadmap.md
    ├── Decisions.md
    ├── POC.md
    └── Out-of-Scope.md

CLAUDE.md
```

# CLAUDE.md file structure
```
# AI Index

## Global Rules

See:

- ai/global/workflow.md
- ai/global/coding.md
- ai/global/testing.md

---

## Backend

See:

- ai/backend/spring.md
- ai/backend/database.md

---

## Frontend

See:

- ai/frontend/react.md
- ai/frontend/ui.md

---

## Current Project

See:

- ai/project/overview.md
- ai/project/domain.md
- ai/project/poc.md
```

# CLAUDE rule priority
1. Read all Global documents.
2. Read Backend/Frontend documents relevant to the task.
3. Read all Project documents.
4. Follow AI Collaboration rules first.
5. If conflicts exist:
   AI Collaboration
      >
   Workflow
      >
   Project Decisions
      >
   Other documents