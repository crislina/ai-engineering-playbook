# Repository Policy

Keep only reusable guidance likely to change an AI assistant's decision.

## Placement

- Shared concept: top-level domain folder.
- Language or framework behavior: technology subfolder.
- Project convention or constraint: project repository, not this playbook.
- Consequential project choice: project ADR.
- Baseline knowledge, tutorial, or placeholder: omit.

## Admission Test

Add knowledge only when all are true:

1. A capable model might reasonably choose differently without it.
2. The rule applies across multiple projects.
3. The rule has a clear task trigger.
4. It is not already expressed by a more authoritative file.

Keep each file focused. State decisions, exceptions, and trade-offs; omit history and introductory teaching. Update `ai-index.md` and `context-routing.md` only when the new topic changes discovery or routing.
