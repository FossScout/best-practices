# Git Best Practices: Commit Messages

## Options

### Option A: Conventional Commits (Recommended)
- **Format**: `type(scope): description`
- **Types**: feat, fix, docs, style, refactor, perf, test, build, ci, chore, revert
- **Pros**: Machine-parseable, drives changelogs, semantic versioning automation, clear intent.
- **Cons**: Discipline required; learning curve; can feel verbose for tiny changes.
- **Best for**: Most projects, especially those with automated releases.

### Option B: Free-form with Prefix
- **Format**: `prefix: description` (loose)
- **Pros**: Flexible, low friction.
- **Cons**: Inconsistent history, hard to automate changelogs.
- **Best for**: Solo/small projects, prototypes.

### Option C: Gitmoji
- **Format**: emoji + description
- **Pros**: Visual scanning.
- **Cons**: Not machine-friendly, accessibility issues, tooling gaps.
- **Best for**: Personal preference only.

## Recommendation
Use **Conventional Commits** with scopes; enforce via commitlint + husky.

## Rules
- Subject line <= 72 chars, imperative mood ("add", not "added").
- Body explains why, not what; wrap at 72 chars.
- Breaking changes: `feat!: ...` or `BREAKING CHANGE:` footer.
- One logical change per commit; don't mix refactor + feature.
- Reference issues: `Closes #123`.
- Never commit secrets, large binaries, or generated files.
