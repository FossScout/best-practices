# IaC Best Practices: Final Decisions

Default rules to follow unless explicitly overridden.

## Terraform
- **Decision**: Terraform + remote state + modules (Option A)

## Pulumi
- **Decision**: Pulumi when team prefers real languages; otherwise Terraform

## Ansible
- **Decision**: Roles/collections, idempotent, vault secrets

## State Management
- **Decision**: Remote state with locking; backup and encrypt

## Modules & Reuse
- **Decision**: Small composable versioned modules
