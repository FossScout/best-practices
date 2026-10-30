# CI/CD Best Practices: Final Decisions

Default rules to follow unless explicitly overridden.

## Pipelines
- **Decision**: GitHub Actions/GitLab CI with reusable workflows (Option A)
- Fast, cached, fail-fast, green required for merge.

## Secrets
- **Decision**: CI secret store + OIDC trusted publishing (Option A)

## Artifacts
- **Decision**: Build once, promote; version+SHA tags; sign.

## Deployments
- **Decision**: Progressive delivery for prod (Option A); direct for internal (Option B)

## Testing in CI
- **Decision**: Unit on PR; integration/E2E on main/staging.
