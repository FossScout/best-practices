# Git Best Practices: Final Decisions

Default rules to follow unless explicitly overridden.

## Branching Strategy
- **Decision**: Trunk-Based Development (Option A)
- Short-lived branches (< 2 days), protect main, require PR + CI + review.

## Commit Messages
- **Decision**: Conventional Commits (Option A)
- Enforce via commitlint + husky; subject <= 72 chars.

## Merge vs Rebase
- **Decision**: Rebase locally; squash-merge PRs (Option A/B hybrid)
- Never force-push shared branches; use `--force-with-lease` only on own branches.

## PR & Review Workflow
- **Decision**: Small PRs + required review + CI (Option A)
- PRs <= 400 lines, at least one approval, green CI, squash merge.

## Tagging & Versioning
- **Decision**: SemVer with annotated tags (Option A)
- Tag on main after CI green; automate releases; maintain CHANGELOG.
