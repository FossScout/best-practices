# Java Best Practices: Project Setup

## Options

### Option A: Maven or Gradle + modules + LTS JDK (Recommended)
- **Description**: Use Maven/Gradle with multi-module; target LTS JDK (17/21).
- **Pros**: Standard, tooling support, long-term support.
- **Cons**: Build tool choice.
- **Best for**: All projects.

### Option B: Single module, latest JDK
- **Description**: Simple.
- **Pros**: Easy.
- **Cons**: Bleeding edge, less stability.
- **Best for**: Prototypes.

## Recommendation
Option A. Prefer Gradle with Kotlin DSL for new projects.

## Rules
- Target LTS JDK; set `source/target`/`release`.
- Use modules for large codebases.
- Use version catalogs (Gradle) or dependencyManagement (Maven).
- Enable preview features only deliberately.
