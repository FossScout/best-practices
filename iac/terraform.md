# IaC Best Practices: Terraform

## Options

### Option A: Terraform with remote state + modules (Recommended)
- **Description**: HCL modules, remote state (S3/GCS) with locking, workspaces/environments.
- **Pros**: Mature, large ecosystem, declarative.
- **Cons**: HCL learning, state management risk.
- **Best for**: Most cloud infra.

## Recommendation
Option A.

## Rules
- Remote state with locking (DynamoDB/S3).
- Use modules for reusable components.
- Pin provider versions.
- `terraform fmt` + `validate` in CI.
- Plan in PR; apply on merge via CI.
- Never commit state or secrets.
- Use workspaces or separate state per env.
