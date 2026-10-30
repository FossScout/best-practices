# REST API Best Practices: Documentation

## Options

### Option A: OpenAPI spec + contract tests (Recommended)
- **Description**: OpenAPI 3.x as source of truth; generate docs and clients; contract tests in CI.
- **Pros**: Standard, tooling, client generation.
- **Cons**: Spec maintenance.
- **Best for**: All APIs.

### Option B: Hand-written docs
- **Description**: Markdown docs.
- **Pros**: Flexible.
- **Cons**: Drift from implementation.
- **Best for**: Avoid for public APIs.

## Recommendation
Option A. Generate spec from code or vice versa; validate in CI.

## Rules
- Keep OpenAPI spec in repo.
- Generate client SDKs from spec.
- Run contract tests (e.g., Schemathesis, Dredd).
- Document auth, rate limits, pagination.
- Version docs with API.
- Provide examples and error responses.
