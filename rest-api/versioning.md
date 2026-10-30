# REST API Best Practices: Versioning

## Options

### Option A: URL path versioning (/v1) (Recommended)
- **Description**: Major version in path; deprecate old with sunset header.
- **Pros**: Explicit, easy routing, cache-friendly.
- **Cons**: URL churn.
- **Best for**: Public APIs.

### Option B: Header versioning (Accept: application/vnd...)
- **Description**: Version via content negotiation.
- **Pros**: Clean URLs.
- **Cons**: Harder to test/cache.
- **Best for**: Internal.

## Recommendation
Option A for public; Option B acceptable internally.

## Rules
- Version only on breaking changes (major).
- Additive changes don't bump version.
- Deprecate with Sunset header + docs.
- Support N-1 versions; define EOL.
- Communicate changes via changelog.
