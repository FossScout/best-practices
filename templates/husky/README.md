# Commitlint + Husky Setup

This provides a reusable setup for enforcing [Conventional Commits](https://www.conventionalcommits.org/) as per `best-practices/git/decisions.md`.

## Files
- `templates/commitlint.config.cjs` - Commitlint configuration
- `templates/husky/commit-msg` - Husky commit-msg hook

## Setup in a project
1. Install dependencies:
```bash
npm install --save-dev @commitlint/cli @commitlint/config-conventional husky
```
2. Copy `commitlint.config.cjs` to project root as `commitlint.config.cjs` (or symlink it).
3. Initialize husky and copy/symlink the hook:
```bash
npx husky install
cp templates/husky/commit-msg .husky/commit-msg
chmod +x .husky/commit-msg
```
Or use symlinks to keep in sync with the best-practices library.

## Notes
- Subject line max length: 72 chars
- Allowed types: feat, fix, docs, style, refactor, perf, test, build, ci, chore, revert, wip
- Scope should be kebab-case
- Subject should not be sentence/start/pascal/upper case, not empty, no trailing period
