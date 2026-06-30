# AI Engineering Playbook

A token-efficient collection of reusable rules for AI coding assistants.

## Start

1. Load [`context-routing.md`](context-routing.md).
2. Follow one route.
3. Load only rules that can change the current result.

The complete topic catalog is in [`ai-index.md`](ai-index.md). Knowledge placement rules are in [`repository-policy.md`](repository-policy.md).

## Scope

This repository contains reusable engineering guidance with meaningful behavioral value. It excludes tutorials, baseline model knowledge, empty technology placeholders, secrets, and project-specific facts.

Projects should define their own architecture decisions, domain rules, API contracts, naming, formatting, Git workflow, deployment approvals, and security constraints. Those rules override this playbook.

## Design

- One concept per file.
- Shared concepts before technology details.
- Decision gates instead of bundled reading lists.
- No duplicated rule unless a boundary needs explicit protection.
- Remove guidance that modern coding models reliably know and projects do not specialize.
