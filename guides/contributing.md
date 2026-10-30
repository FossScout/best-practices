# Contributing Guide (Reusable)

This is a reusable contributing guide. Projects should adapt it to their needs.

## Prerequisites
- Development environment setup for the tech stack
- Required tools and SDKs

## Setup
1. Clone the repository.
2. Follow project-specific setup instructions.
3. Install dependencies.

## Development Workflow
Follow the project's AGENTS.md or equivalent guidelines:
1. Read relevant files before writing code.
2. Ask if unclear or if you need to add dependencies/abstractions/config options.
3. Propose improvements with tradeoffs before implementing if you see a better approach.
4. Implement minimal changes.
5. Verify.
6. Create a new branch and open a PR with a Conventional Commits message.

## Branching
- Never commit directly to main/master. Always create a new branch.
- Keep branches short-lived (< 2 days) when possible (trunk-based development).
- Use clear branch names (e.g., `feat/`, `fix/`, `refactor/`, `docs/`).

## Commits
- Follow [Conventional Commits](https://www.conventionalcommits.org/). Subject line <= 72 chars.
- Keep commits focused and atomic.

## Pull Requests
- Keep PRs small (<= 400 lines preferred).
- Use the project PR template.
- Link related issues.
- Include screenshots/videos for UI changes.
- Ensure CI is green and reviews obtained before merge.
- Prefer squash merge.

## Code Guidelines
- Follow project architecture and coding conventions.
- Respect module boundaries.
- No drive-by cleanups, no abstractions "for future use", no new dependencies without approval.
- Write tests for non-trivial changes.

## Getting Help
- Check existing docs and best-practices library.
- If unsure, ask before making assumptions.
