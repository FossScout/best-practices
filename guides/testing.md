# Testing Guidelines (Reusable)

This is a reusable testing guide. Adapt to project testing stack.

## When to Write Tests
- **Must test**: Business logic, use cases, state holders, mappers, complex algorithms
- **Consider**: Error handling, edge cases, integrations
- **Skip**: Trivial changes, generated code, simple passthroughs

## Test Types
- **Unit tests**: Fast, isolated tests of individual components
- **Integration tests**: Test component interactions
- **UI tests**: Test user flows (use sparingly)

## Best Practices
- Test behavior, not implementation
- Keep tests focused and deterministic
- Use fakes/stubs over mocks when possible
- Follow AAA pattern (Arrange, Act, Assert)
- One assertion per test conceptually
- Avoid sleeping/waiting, use proper async testing

## Async/Reactive Testing
- Use framework-specific async test utilities
- Control schedulers/dispatchers in tests
- Test state emissions properly

## Coverage
- Don't chase 100% coverage
- Focus on critical paths and business logic
- Don't reduce existing coverage
- Update tests when changing APIs

## Running Tests
Document project-specific test commands in project docs.
