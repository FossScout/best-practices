# REST API Best Practices: Auth

## Options

### Option A: OAuth2 + JWT (short-lived) + refresh tokens (Recommended)
- **Description**: OAuth2 flows; short-lived access tokens; refresh rotation.
- **Pros**: Standard, scalable, secure.
- **Cons**: Complexity.
- **Best for**: User-facing APIs.

### Option B: API keys
- **Description**: Static keys per client.
- **Pros**: Simple.
- **Cons**: Leakage risk, no user context.
- **Best for**: Server-to-server / internal.

## Recommendation
Option A for users; Option B for service accounts (with scopes).

## Rules
- Always HTTPS.
- Short token TTL; rotate refresh tokens.
- Scope permissions (least privilege).
- Rate limit per client/key.
- Never put tokens in URLs.
- Store secrets server-side; validate audience/issuer.
