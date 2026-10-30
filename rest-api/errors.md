# REST API Best Practices: Errors

## Rules
- Use RFC 7807 Problem Details (application/problem+json).
- Include type, title, status, detail, instance.
- Add machine-readable error code (e.g., `code: "USER_NOT_FOUND"`).
- Don't leak internals/stack traces in prod.
- Consistent error shape across all endpoints.
- Log full error server-side with correlation ID.
- Include `traceId`/`requestId` in response.
