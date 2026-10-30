# Observability Best Practices: Final Decisions

Default rules to follow unless explicitly overridden.

## Logging
- **Decision**: Structured JSON with correlation IDs; centralized

## Metrics
- **Decision**: RED + USE metrics via Prometheus format (Option A)

## Tracing
- **Decision**: OpenTelemetry with context propagation

## Alerting
- **Decision**: SLO burn-rate alerts with runbooks

## Dashboards
- **Decision**: Golden signals; Grafana as code
