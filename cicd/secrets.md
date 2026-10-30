# CI/CD Best Practices: Secrets

## Rules
- Store secrets in CI secret store; never in repo.
- Use OIDC/trusted publishing over long-lived tokens.
- Scope secrets to environments.
- Rotate regularly; audit access.
- Mask secrets in logs.
- Separate dev/staging/prod credentials.
