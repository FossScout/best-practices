# Kotlin Best Practices: Architecture

## Options

### Option A: Clean Architecture + DI (Hilt/Koin) + modules (Recommended)
- **Description**: Domain/data/presentation layers; DI for wiring; feature modules.
- **Pros**: Testable, scalable, clear boundaries.
- **Cons**: Boilerplate, over-engineering risk for small apps.
- **Best for**: Medium/large apps.

### Option B: Layered/simple architecture
- **Description**: Controller-service-repo without strict boundaries.
- **Pros**: Faster to start.
- **Cons**: Tangles at scale.
- **Best for**: Small/prototypes.

## Recommendation
Option A for production apps; Option B for prototypes.

## Rules
- Domain layer has no framework dependencies.
- Use interfaces for repositories; inject implementations.
- Keep ViewModels thin; move logic to use cases.
- Avoid leaking Android/framework types into domain.
- Module by feature when app grows.
- Prefer unidirectional data flow (UDF).
