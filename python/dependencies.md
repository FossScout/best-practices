# Python Best Practices: Dependencies

## Options

### Option A: uv/pip-tools with lockfile (Recommended)
- **Description**: Resolve and lock dependencies; reproducible installs.
- **Pros**: Fast, reproducible, modern.
- **Cons**: Tooling choice.
- **Best for**: All projects.

### Option B: requirements.txt (unpinned)
- **Description**: Loose pins.
- **Pros**: Simple.
- **Cons**: Non-reproducible.
- **Best for**: Avoid in prod.

## Recommendation
Option A. Commit lockfile.

## Rules
- Separate runtime and dev dependencies.
- Pin exact versions in lockfile.
- Update via bots (Dependabot/Renovate).
- Avoid global installs; use venv.
- Audit deps for CVEs (pip-audit).
