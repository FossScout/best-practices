# CI/CD Best Practices: Pipelines

## Options

### Option A: GitHub Actions / GitLab CI with reusable workflows (Recommended)
- **Description**: YAML pipelines with reusable workflows/templates, matrix builds.
- **Pros**: Version-controlled, scalable, ecosystem.
- **Cons**: YAML complexity, debugging.
- **Best for**: Most teams.

### Option B: Jenkins
- **Description**: Self-hosted, plugin-rich.
- **Pros**: Flexible, on-prem.
- **Cons**: Maintenance burden, security.
- **Best for**: Legacy/enterprise.

## Recommendation
Option A unless on-prem constraints.

## Rules
- Keep pipelines fast (< 10 min ideal).
- Cache dependencies.
- Fail fast on lint/tests.
- Use matrix for multi-version/platform.
- Separate build and deploy stages.
- Require green CI for merge.
