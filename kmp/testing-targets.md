# KMP Best Practices: Testing & Targets

## Options

### Option A: commonTest + platform tests + KMP test runners (Recommended)
- **Description**: Shared tests in commonTest; platform-specific tests where needed; use `kotlin.test`.
- **Pros**: Broad coverage with minimal duplication.
- **Cons**: Some APIs untestable in common.
- **Best for**: Most KMP projects.

### Option B: Per-platform test suites only
- **Description**: Duplicate tests per platform.
- **Pros**: Full platform fidelity.
- **Cons**: Duplication, drift.
- **Best for**: Avoid.

## Recommendation
Option A. Run commonTest on all targets in CI.

## Rules
- Use `kotlin.test` annotations (works across targets).
- Mock with platform-appropriate tools (MockK on JVM, fakes elsewhere).
- Run tests on all declared targets in CI.
- Keep platform-specific code minimal and tested on that platform.
- Use Testcontainers only on JVM target.
- Version and matrix-test target platforms.
