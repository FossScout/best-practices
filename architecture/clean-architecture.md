# Architecture Best Practices: Clean Architecture

## Rules
- Domain layer framework-free; depend inward.
- Use cases orchestrate domain logic.
- Adapters (DB, web) depend on domain, not vice versa.
- Dependency inversion via interfaces.
- Keep boundaries explicit.
- Test domain in isolation.
