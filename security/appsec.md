# Security Best Practices: AppSec

## Options

### Option A: OWASP Top 10 + secure coding + SAST/DAST (Recommended)
- **Description**: Follow OWASP; validate input; encode output; use SAST (Semgrep/CodeQL) and DAST in CI.
- **Pros**: Covers common vulns.
- **Cons**: Requires tooling and training.
- **Best for**: All apps.

## Recommendation
Option A.

## Rules
- Validate and sanitize all input (allow-list).
- Encode output to prevent XSS.
- Parameterized queries (no SQL injection).
- CSRF protection for state-changing endpoints.
- Secure headers (CSP, HSTS, X-Frame-Options).
- Run SAST in CI; DAST on staging.
- Dependency and container scanning.
