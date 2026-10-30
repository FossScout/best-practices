# Security Best Practices: Secrets Management

## Rules
- Never commit secrets; use secret manager (Vault, cloud KMS).
- Rotate on exposure; use short-lived credentials.
- Least privilege for secret access.
- Audit secret access.
- Use environment injection at runtime.
- Scan repo for leaked secrets (gitleaks/trufflehog) in CI.
