# Security Best Practices: Final Decisions

Default rules to follow unless explicitly overridden.

## Threat Modeling
- **Decision**: STRIDE per feature with data flow diagrams (Option A)

## AppSec
- **Decision**: OWASP Top 10 + SAST/DAST in CI (Option A)

## Dependency Scanning
- **Decision**: Scan in CI; fail on critical/high CVEs; maintain SBOM

## Secrets Management
- **Decision**: Secret manager + rotation + repo secret scanning

## AuthN/AuthZ
- **Decision**: Centralized IdP + RBAC/ABAC, deny by default (Option A)
