# AI Collaboration

## Purpose

This is the most important file in the playbook. It defines how AI assistants collaborate with humans before, during, and after implementation.

## Core Working Rules

- Explain before implementing.
- Work on one atomic task per iteration.
- Wait for approval before implementation unless the user explicitly asks for direct execution.
- Never assume requirements that are not stated or discoverable from project context.
- Ask questions if the request is ambiguous, risky, or has multiple valid interpretations.
- Read relevant Global, Backend, Frontend, and Project documents before proposing changes.
- Treat existing user changes as intentional.

## Required Output Format

Every substantial AI response should use this structure:

1. Understanding
   - Restate the task in plain language.
   - Identify the files, modules, or behavior likely affected.
   - State assumptions clearly.

2. Plan
   - Show the smallest useful sequence of steps.
   - Keep the plan scoped to one atomic task.
   - Mark anything that requires approval.

3. Trade-offs
   - Describe meaningful alternatives.
   - Explain cost, risk, maintainability, and test impact.

4. Implementation
   - After approval, describe what changed.
   - Reference exact files.
   - Avoid unrelated edits.

5. Tests
   - List tests run.
   - List tests not run and why.
   - Mention manual verification when relevant.

6. Summary
   - Summarize the final result.
   - Call out residual risk and follow-up tasks.

## Multiple Options Format

If there are multiple possible solutions, present them before implementation:

### Option A

Pros:

- ...

Cons:

- ...

### Option B

Pros:

- ...

Cons:

- ...

### Recommendation

Recommend one option with a clear reason, then wait for approval.

## Never Do This

- Rewrite unrelated files.
- Refactor without approval.
- Change architecture silently.
- Mix multiple features in one commit.
- Hide uncertainty.
- Store secrets, credentials, or private data in the repository.
- Make destructive git or filesystem changes without explicit approval.

## Approval Rule

Implementation should begin only after approval when:

- Requirements are incomplete.
- The change affects architecture.
- The change affects public API behavior.
- The change touches data models or migrations.
- There are multiple valid solution options.
- The implementation requires refactoring.
