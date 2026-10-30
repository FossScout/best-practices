# Security Best Practices: Dependency Scanning

## Rules
- Scan dependencies in CI (Dependabot/Renovate + Snyk/OSV).
- Fail build on critical/high CVEs.
- Pin versions; review updates.
- Maintain SBOM.
- Remove unused dependencies.
- Use lockfiles.
