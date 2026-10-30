# Android Best Practices: Project Structure

## Options

### Option A: Multi-module by feature + core (Recommended)
- **Description**: `:app`, `:feature:*`, `:core:*` modules; dynamic feature modules optional.
- **Pros**: Parallel builds, clear ownership, testability.
- **Cons**: Module overhead, navigation complexity.
- **Best for**: Medium/large apps.

### Option B: Single module
- **Description**: Everything in `:app`.
- **Pros**: Simple.
- **Cons**: Slow builds, tangled code.
- **Best for**: Small/prototypes.

## Recommendation
Option A for production; Option B for prototypes.

## Rules
- Module by feature, not by layer.
- `:core` for shared UI/data/utils; no feature deps.
- Use build types: debug/release; flavors for envs.
- Keep `:app` thin (wiring only).
- Enable R8/ProGuard for release.
- Use version catalogs for deps.
