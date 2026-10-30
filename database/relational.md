# Database Best Practices: Relational

## Options

### Option A: PostgreSQL with migrations + connection pooling (Recommended)
- **Description**: Postgres as default; schema migrations (Flyway/Liquibase); pooled connections (HikariCP/pgBouncer).
- **Pros**: ACID, rich features, mature ecosystem.
- **Cons**: Vertical scaling limits; ops overhead.
- **Best for**: Transactional/relational data.

### Option B: MySQL/MariaDB
- **Description**: Widely supported alternative.
- **Pros**: Familiar, broad hosting.
- **Cons**: Fewer advanced features.
- **Best for**: Compatibility needs.

## Recommendation
Option A. Use Postgres unless specific need.

## Rules
- Never edit schema manually in prod; use migrations.
- Index based on query patterns; review EXPLAIN.
- Use transactions; avoid long-running transactions.
- Connection pooling mandatory.
- Backup + PITR; test restores.
- Avoid SELECT *; paginate.
