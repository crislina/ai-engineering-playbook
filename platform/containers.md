# Containers

Load when building or changing container images.

- Pin deliberate base versions and make builds reproducible.
- Separate build and runtime dependencies; keep the runtime image minimal.
- Run as a non-root user unless the workload requires otherwise.
- Keep secrets out of image layers and build arguments that persist.
- Define meaningful health checks and shutdown behavior.
- Scan and update images according to project security policy.
