# Testing Strategy: Mutation Testing

## Options

### Option A: Mutation testing in CI (Recommended for critical code)
- **Description**: Mutate code; verify tests catch mutations (PIT, Stryker).
- **Pros**: Measures test quality.
- **Cons**: Slow; can be noisy.
- **Best for**: Critical libraries/core logic.

## Recommendation
Option A for core logic; not for all code.

## Rules
- Run on changed modules or nightly.
- Target mutation score threshold (e.g., 80%).
- Fix surviving mutants (test gaps or dead code).
- Exclude generated/boilerplate code.
