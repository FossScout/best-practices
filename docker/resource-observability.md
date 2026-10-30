# Docker Best Practices: Resource Limits & Observability

## Options

### Option A: Explicit limits + structured logs + health/metrics (Recommended)
- **Description**: Set CPU/mem limits and reservations; structured JSON logs; expose metrics/health endpoints.
- **Pros**: Prevents noisy neighbors, enables monitoring and autoscaling.
- **Cons**: Tuning effort.
- **Best for**: Production.

### Option B: No limits, default logging
- **Description**: Rely on host defaults.
- **Pros**: Simple.
- **Cons**: OOM kills, unbounded resource use, poor debuggability.
- **Best for**: Dev only.

## Recommendation
Option A in prod; Option B in dev.

## Rules
- Set `mem_limit`, `mem_reservation`, `cpus` (or deploy.resources).
- Set `logging.driver` with size/rotation (`max-size`, `max-file`).
- Healthcheck on every service.
- Expose `/health` and `/metrics` where applicable.
- Use consistent log format (JSON) with correlation IDs.
- Monitor container restarts and OOM events.
