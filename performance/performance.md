# Performance Best Practices

## Rules
- Profile before optimizing (CPU, memory, IO).
- Benchmark with realistic data and load.
- Avoid premature optimization; optimize hot paths.
- Use caching (HTTP, DB, in-memory) with invalidation strategy.
- Lazy load and paginate.
- Monitor regressions in CI (perf budgets).
- Optimize DB queries (indexes, N+1 avoidance).
