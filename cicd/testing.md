# CI/CD Best Practices: Testing in CI

## Rules
- Run unit tests on every PR.
- Run integration tests on merge/main.
- Parallelize test suites.
- Cache test dependencies.
- Fail build on coverage drop (optional threshold).
- Publish test reports and artifacts.
- Run E2E on staging before prod deploy.
