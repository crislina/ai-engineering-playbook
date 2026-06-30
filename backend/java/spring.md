# Spring

Load only for Spring-specific implementation decisions.

- Follow the project's package and component conventions; do not reorganize by default.
- Bind external configuration to typed configuration objects and validate required values at startup.
- Put transaction boundaries on service/use-case methods; use read-only transactions only when their semantics help.
- Keep controllers limited to transport mapping, validation activation, and delegation.
- Use focused slice tests for adapter behavior and integration tests for wiring or cross-boundary contracts.
- Do not make remote calls inside a transaction without an explicit consistency reason.
