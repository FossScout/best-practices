# Security Best Practices: AuthN/AuthZ

## Options

### Option A: Centralized IdP + RBAC/ABAC (Recommended)
- **Description**: Use IdP (OIDC/OAuth2); enforce RBAC or ABAC; deny by default.
- **Pros**: Centralized, auditable, scalable.
- **Cons**: Infra setup.
- **Best for**: Most apps.

## Recommendation
Option A. Deny by default; least privilege.

## Rules
- Use established IdP; don't roll own crypto.
- Enforce authorization server-side (never trust client).
- Deny by default; explicit allow.
- Separate authn (who) from authz (what).
- Audit auth events.
- MFA for privileged accounts.
- Session/token expiry and revocation.
