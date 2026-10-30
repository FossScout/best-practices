# KMP Best Practices: expect/actual & Interop

## Options

### Option A: Interfaces + DI over expect/actual (Recommended)
- **Description**: Prefer interfaces in common code with platform implementations injected; use expect/actual sparingly.
- **Pros**: Easier testing, less platform coupling, clearer contracts.
- **Cons**: More wiring.
- **Best for**: Most shared logic.

### Option B: Heavy expect/actual
- **Description**: Platform-specific implementations via expect/actual.
- **Pros**: Direct, no DI overhead.
- **Cons**: Harder to test, scattered platform code.
- **Best for**: Low-level platform APIs.

## Recommendation
Option A for business logic; Option B only for platform primitives.

## Rules
- Minimize `expect`/`actual`; prefer interfaces.
- Keep actual implementations thin.
- Use `@ObjCName`/interop annotations for Swift/ObjC interop.
- Expose flows/state to Swift via SKIE or manual wrappers.
- Avoid exposing coroutines internals directly to Swift; wrap.
- Test common code with commonTest.
