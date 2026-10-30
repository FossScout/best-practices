# Git Best Practices: Branching Strategy

## Overview
Choose a branching model that matches team size, release cadence, and deployment model.

## Options

### Option A: Trunk-Based Development (Recommended)
- **Description**: Single main branch; short-lived feature branches (< 1 day) merged via PR.
- **Pros**: Simple history, fast feedback, continuous deployment friendly, minimal merge conflicts.
- **Cons**: Requires strong CI, feature flags for incomplete work, disciplined small commits.
- **Best for**: Teams practicing CI/CD, frequent releases, small-to-medium teams.

### Option B: GitHub Flow
- **Description**: main + feature branches; deploy from main after PR merge.
- **Pros**: Simple, well-documented, good for SaaS/web apps.
- **Cons**: No explicit release branches; hotfixes go through main.
- **Best for**: Web applications with continuous deployment.

### Option C: Git Flow
- **Description**: main, develop, feature/*, release/*, hotfix/* branches.
- **Pros**: Clear release management, supports parallel releases, explicit hotfix path.
- **Cons**: Complex, long-lived branches cause merge drift, slower feedback.
- **Best for**: Versioned products with scheduled releases, larger teams.

## Recommendation
Use **Trunk-Based Development** for most modern teams; fall back to **GitHub Flow** for simpler setups; reserve **Git Flow** for versioned release products.

## Rules
- Branch names: `type/short-description` (e.g., `feat/login`, `fix/null-check`).
- Delete branches after merge.
- Keep branches short-lived (< 2 days).
- Protect main: require PR + CI green + review.
- Never commit directly to main.
