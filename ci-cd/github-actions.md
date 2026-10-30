# GitHub Actions Best Practices

This guide complements `best-practices/cicd/decisions.md`.

## Principles
- Keep workflows fast and simple
- Use caching appropriately
- Fail fast
- Require status checks on protected branches
- Never log secrets

## Common Patterns
- **Build**: Cache Gradle dependencies, run on push/PR
- **Test**: Run unit tests, upload reports
- **Lint**: Run ktlint/detekt/lint
- **Security**: Dependabot + dependency review
- **Release**: Tag-based releases

## Caching
- Use `actions/cache` or built-in caching
- Cache Gradle: `~/.gradle/caches`, `~/.gradle/wrapper`
- Be careful with cache keys

## Required Checks
- Build must pass
- Tests must pass
- Lint/static analysis must pass
- At least one review required (branch protection)

## Secrets
- Use GitHub Secrets
- Never echo secrets
- Limit permissions with `permissions:` block

## Example Workflow Structure
```yaml
name: CI
on: [push, pull_request]
permissions:
  contents: read
jobs:
  build:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v4
      - uses: actions/setup-java@v4
        with:
          distribution: 'temurin'
          java-version: '17'
      - uses: gradle/actions/setup-gradle@v3
      - run: ./gradlew build
```

## Recommendations
- Use `gradle/actions/setup-gradle` for better caching
- Run matrix builds only if necessary
- Keep workflows in `.github/workflows/`
- Document required checks in project docs
