# Observability Best Practices: Metrics

## Options

### Option A: RED (Rate, Errors, Duration) + USE (Utilization, Saturation, Errors) (Recommended)
- **Description**: Standard metric sets; Prometheus format; scrape-based.
- **Pros**: Consistent, tooling support.
- **Cons**: Cardinality management.
- **Best for**: All services.

## Recommendation
Option A.

## Rules
- Expose /metrics endpoint.
- Use histograms for latency.
- Avoid high cardinality labels (no user IDs).
- Define SLOs on key metrics.
- Alert on symptoms, not causes.
