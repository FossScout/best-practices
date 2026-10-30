# Git Best Practices: Merge vs Rebase

## Options

### Option A: Rebase for local, Merge for integration (Recommended)
- **Description**: Rebase feature branches onto main before PR; use merge commits (or squash) on integration.
- **Pros**: Linear, readable history; preserves individual commits; clean blame.
- **Cons**: Rewrites public history if misused; conflict resolution repeated.
- **Best for**: Most teams.

### Option B: Squash merge only
- **Description**: Squash all commits into one on merge.
- **Pros**: Clean main history, one commit per PR.
- **Cons**: Loses granular history; harder bisect within PR.
- **Best for**: Teams prioritizing simple main history.

### Option C: Merge commits always
- **Description**: Always create merge commit.
- **Pros**: Preserves full graph, easy revert of whole feature.
- **Cons**: Noisy history, harder to read.
- **Best for**: Audit-heavy or regulated environments.

## Recommendation
Rebase locally to keep branches current; squash-merge PRs to main for clean history. Never rebase shared/public branches.

## Rules
- Never force-push to main/develop/release branches.
- Rebase only your own feature branches.
- Resolve conflicts locally, not on main.
- Prefer `git pull --rebase` for syncing.
- Use `--force-with-lease` if force push unavoidable.
