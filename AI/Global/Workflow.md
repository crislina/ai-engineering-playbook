# Workflow

## Purpose

Define the required workflow for AI-assisted engineering work.

## Required Flow

### 1. Plan

- Read relevant playbook files.
- Understand the request, affected scope, and expected result.
- Identify ambiguity, risk, and dependencies.
- Produce a small plan for one atomic task.

### 2. Approval

- Present the plan before implementation.
- Present options when more than one approach is reasonable.
- Wait for user approval before changing code, architecture, database schema, API behavior, or project scope.

### 3. Implementation

- Implement only the approved scope.
- Keep changes minimal and traceable.
- Do not mix unrelated cleanup, refactor, or new features.
- Preserve existing architecture and conventions unless the approved plan changes them.

### 4. Test

- Run the smallest meaningful validation first.
- Add or update tests when behavior changes.
- Run broader tests when shared behavior, architecture, or critical paths are touched.
- Report anything that could not be tested.

### 5. Commit

- Commit one feature, fix, or decision at a time.
- Use Conventional Commit format.
- Do not commit unrelated changes.
- Include tests and docs in the same commit only when they support the same atomic change.

### 6. Summary

- State what changed.
- List files touched.
- List validation performed.
- Note known risks, skipped tests, and next steps.

## Working Rules

- Preserve existing project style unless there is an approved reason to change it.
- Keep unrelated refactors out of focused tasks.
- Surface blockers early with concrete options.
- Never skip the approval step for ambiguous or architectural work.

## Definition of Done

- The requested change is implemented or the limitation is clearly documented.
- Relevant validation has run, or the reason it could not run is stated.
- The final response includes changed files and any follow-up risks.
