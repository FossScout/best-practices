# Database Best Practices: Final Decisions

Default rules to follow unless explicitly overridden.

## Relational
- **Decision**: PostgreSQL + migrations + pooling (Option A)
- Index by query patterns; backup + PITR.

## NoSQL
- **Decision**: Use only when relational doesn't fit (Option A document / Option B kv)
- Model for access patterns; handle eventual consistency.

## Column-Oriented
- **Decision**: ClickHouse/BigQuery for analytics; separate from OLTP (Option A)

## Offline-First
- **Decision**: Local DB + sync engine for mobile (Option A); online-first for web (Option B)

## Syncable
- **Decision**: Server-authoritative sync default; CRDT for real-time collab (Option B / Option A)
