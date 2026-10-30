# IaC Best Practices: State Management

## Rules
- Never store state locally for shared infra.
- Enable state locking to prevent concurrent applies.
- Backup state; version it.
- Use state encryption at rest.
- Import existing resources; don't recreate.
- Periodic `terraform state list` audits.
