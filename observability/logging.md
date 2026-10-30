# Observability Best Practices: Logging

## Rules
- Structured JSON logs with timestamp, level, service, traceId, requestId.
- Log at appropriate levels; avoid debug in prod.
- Never log secrets/PII.
- Correlation IDs propagated across services.
- Centralize logs (Loki/ELK/Datadog).
- Retention policy defined.
