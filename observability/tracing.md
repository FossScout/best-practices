# Observability Best Practices: Tracing

## Rules
- Use OpenTelemetry for traces.
- Propagate trace context across services (W3C traceparent).
- Sample appropriately (head/tail sampling).
- Instrument critical paths and external calls.
- Correlate traces with logs (traceId).
- Store traces in backend (Jaeger/Tempo/Datadog).
