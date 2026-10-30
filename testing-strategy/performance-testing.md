# Testing Strategy: Performance Testing

## Rules
- Baseline performance; run load tests before releases.
- Use k6/JMeter/Gatling.
- Test realistic scenarios and data volumes.
- Set SLOs; fail on regression.
- Run in staging, not prod.
- Profile bottlenecks (CPU, memory, DB).
