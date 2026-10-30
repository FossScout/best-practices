# CI/CD Best Practices: Deployments

## Options

### Option A: Progressive delivery (canary/blue-green) (Recommended)
- **Description**: Gradual rollout with automated rollback on metrics.
- **Pros**: Low risk, fast feedback.
- **Cons**: Infra complexity.
- **Best for**: Production services.

### Option B: Direct deploy
- **Description**: Replace all at once.
- **Pros**: Simple.
- **Cons**: Higher risk.
- **Best for**: Low-traffic/internal.

## Recommendation
Option A for prod; Option B for internal.

## Rules
- Separate environments: dev/staging/prod.
- Manual approval gate for prod.
- Automated rollback on health failure.
- Database migrations before app deploy (backward-compatible).
- Feature flags for risky changes.
- Keep deploy idempotent.
