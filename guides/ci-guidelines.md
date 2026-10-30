# CI Guidelines (Reusable)

This guide complements `best-practices/ci-cd/github-actions.md`.

## Principles
- All changes go through CI
- Required status checks on protected branches
- Fast feedback
- Reproducible builds

## Recommended Checks
- Build
- Unit tests
- Lint/static analysis
- Type checking (if applicable)
- Security scans (optional)

## Branch Protection
- Require pull request reviews
- Require status checks to pass
- Require branches to be up to date
- Restrict pushes to main
- Require linear history (if using rebase/squash)

## Caching
- Cache dependencies
- Use appropriate cache keys
- Don't cache secrets

## Secrets
- Use CI secret store
- Never log secrets
- Limit permissions

## Artifacts
- Upload test reports
- Upload build artifacts when needed
- Clean up old artifacts
