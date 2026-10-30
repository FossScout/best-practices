# REST API Best Practices: Design

## Options

### Option A: Resource-oriented, HTTP semantics, pagination (Recommended)
- **Description**: Nouns for resources, correct HTTP methods/status codes, cursor/offset pagination, filtering/sorting.
- **Pros**: Predictable, cacheable, standard.
- **Cons**: Over-fetching; chatty.
- **Best for**: Most APIs.

### Option B: RPC-style over HTTP
- **Description**: Action endpoints.
- **Pros**: Simple for complex ops.
- **Cons**: Less cacheable, non-standard.
- **Best for**: Internal/complex operations.

## Recommendation
Option A. Use POST for actions not representable as resources.

## Rules
- Plural nouns for collections; kebab-case paths.
- Use proper status codes (201, 204, 400, 401, 403, 404, 409, 422, 429, 500).
- Paginate lists (cursor preferred for large sets).
- Filter/sort via query params; validate allow-list.
- Use ETags/If-Match for concurrency.
- Keep payloads focused; avoid over-fetching (field selection optional).
- HATEOAS optional; don't force.
