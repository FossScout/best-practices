# KMP Best Practices: Final Decisions

Default rules to follow unless explicitly overridden.

## Project Structure
- **Decision**: Shared module + platform modules (Option A)
- commonMain framework-free; expect/actual sparingly.

## expect/actual & Interop
- **Decision**: Interfaces + DI over expect/actual (Option A)
- Wrap coroutines for Swift; use interop annotations.

## Testing & Targets
- **Decision**: commonTest + platform tests (Option A)
- Run commonTest on all targets in CI.
