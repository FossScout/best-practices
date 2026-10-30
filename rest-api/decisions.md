# REST API Best Practices: Final Decisions

Default rules to follow unless explicitly overridden.

## Design
- **Decision**: Resource-oriented, HTTP semantics, pagination (Option A)

## Versioning
- **Decision**: URL path versioning (Option A)

## Auth
- **Decision**: OAuth2 + short-lived JWT (Option A); API keys for services (Option B)

## Errors
- **Decision**: RFC 7807 Problem Details with stable error codes

## Documentation
- **Decision**: OpenAPI spec + contract tests in CI (Option A)
