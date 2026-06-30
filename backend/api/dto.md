# DTO Contracts

Load when an external request or response shape is created or changed.

- DTOs are boundary contracts; do not expose persistence entities.
- Separate request and response types when their fields, validation, or evolution differ.
- Keep business logic out of DTOs.
- Make mapping explicit enough that API and persistence can evolve independently.
- Define intentional handling for absent, nullable, date/time, enum, and unknown fields.
- Follow project naming; suffixes such as `Request` and `Response` are options, not universal rules.
