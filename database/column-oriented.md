# Database Best Practices: Column-Oriented

## Options

### Option A: ClickHouse / BigQuery for analytics (Recommended)
- **Description**: Columnar storage optimized for aggregations and large scans.
- **Pros**: Fast analytics, compression, scale.
- **Cons**: Poor for OLTP/updates; different mental model.
- **Best for**: Analytics, BI, event data.

### Option B: Row store with materialized views
- **Description**: Use relational DB with aggregations.
- **Pros**: Simpler ops.
- **Cons**: Slower at scale.
- **Best for**: Small analytics.

## Recommendation
Option A for analytics workloads; keep OLTP separate.

## Rules
- Separate OLTP and OLAP stores.
- Batch inserts; avoid row-by-row.
- Partition by time.
- Materialize aggregates.
- Monitor query cost.
