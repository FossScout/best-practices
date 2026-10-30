# Git Best Practices: PR & Review Workflow

## Options

### Option A: Small PRs + required review + CI (Recommended)
- **Description**: PRs <= 400 lines; at least one approval; CI must pass; squash merge.
- **Pros**: Fast review, low risk, high quality.
- **Cons**: Requires discipline to split work; more PRs to manage.
- **Best for**: Most teams.

### Option B: Large batched PRs
- **Description**: Bundle multiple changes.
- **Pros**: Fewer PRs.
- **Cons**: Slow review, high risk, merge conflicts.
- **Best for**: Avoid.

## Recommendation
Small PRs with mandatory review and green CI; use draft PRs for early feedback.

## Rules
- PR title follows Conventional Commits.
- Description: what, why, how to test, screenshots if UI.
- Link issue; mark breaking changes.
- Keep PRs focused on one concern.
- Review within 24h; block merge on unresolved comments.
- Require status checks: lint, typecheck, tests.
- Use CODEOWNERS for critical paths.
- Delete branch after merge.
