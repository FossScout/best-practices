# Docker Best Practices: Dependency License Check

## Options

### Option A: Automated license scan in CI (Recommended)
- **Description**: Use tools (license-checker, pip-licenses, cargo-license, FOSSA, Snyk) to list and allow/deny licenses per project policy.
- **Pros**: Repeatable, policy-enforced, catches copyleft early.
- **Cons**: False positives; license metadata gaps.
- **Best for**: Any shipped product.

### Option B: Manual review
- **Description**: Periodic manual audit.
- **Pros**: Flexible.
- **Cons**: Error-prone, not continuous.
- **Best for**: Small/internal-only projects.

## Recommendation
Option A in CI with an allow-list policy; fail build on disallowed licenses.

## Rules
- Define allowed license list (e.g., MIT, Apache-2.0, BSD) in repo config.
- Run license check on every PR and release.
- Include transitive dependencies.
- Generate license report artifact for releases.
- Review new dependencies' licenses before adding.
- Keep third-party notices file updated.
