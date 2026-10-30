# Database Best Practices: NoSQL

## Options

### Option A: Document store (MongoDB) for flexible schemas (Recommended when needed)
- **Description**: Schema-flexible document DB with indexing.
- **Pros**: Flexible, horizontal scale, fast dev.
- **Cons**: Weaker consistency, query complexity, data duplication.
- **Best for**: Catalogs, content, variable schemas.

### Option B: Key-value (Redis/DynamoDB)
- **Description**: Fast lookups by key.
- **Pros**: Extremely fast, simple.
- **Cons**: Limited querying.
- **Best for**: Caching, sessions, simple state.

## Recommendation
Use NoSQL only when relational doesn't fit; prefer polyglot persistence.

## Rules
- Model for access patterns, not normalization.
- Define indexes explicitly.
- Handle eventual consistency in app.
- Avoid unbounded documents.
- Backup and test restore.
