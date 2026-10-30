# KMP Best Practices: Project Structure

## Options

### Option A: Shared module + platform modules (Recommended)
- **Description**: `:shared` KMP module with `commonMain` + platform source sets; platform apps consume it.
- **Pros**: Clear boundaries, reusable logic, testable common code.
- **Cons**: Build complexity, expect/actual boilerplate.
- **Best for**: Most KMP projects.

### Option B: Monolithic with source sets
- **Description**: Single module with all targets.
- **Pros**: Simpler initially.
- **Cons**: Scales poorly, tight coupling.
- **Best for**: Prototypes.

## Recommendation
Option A. Keep `commonMain` framework-free.

## Rules
- `commonMain` has no platform APIs; use `expect`/`actual` or interfaces.
- Platform modules (`:androidApp`, `:iosApp`) depend on `:shared`.
- Use source sets: commonMain, commonTest, androidMain, iosMain, jvmMain, etc.
- Keep shared module small and focused.
- Version targets explicitly (Kotlin, KMP plugin).
