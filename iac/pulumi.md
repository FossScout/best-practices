# IaC Best Practices: Pulumi

## Options

### Option A: Pulumi with general-purpose language (Recommended for code-heavy teams)
- **Description**: Define infra in TS/Python/Go/C# with strong typing.
- **Pros**: Real language, testing, IDE support.
- **Cons**: Less community modules than Terraform.
- **Best for**: Teams preferring code over HCL.

## Recommendation
Option A when team prefers real languages; Terraform otherwise.

## Rules
- Use stacks for environments.
- Store state in Pulumi Cloud or self-hosted backend.
- Use component resources for reuse.
- Test infra with unit/integration tests.
- Pin SDK versions.
