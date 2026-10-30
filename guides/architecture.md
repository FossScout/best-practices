# Architecture Guidelines (Reusable)

This is a reusable architecture guide. Adapt to project needs.

## Core Principles
- Maintenance over performance. Human-readable over clever. Simple over abstract. Explicit over implicit.
- Clear boundaries and separation of concerns
- Prefer composition over inheritance
- YAGNI - only abstract when there's a concrete need

## Module Structure
Define clear module boundaries:
- **App/Core**: Application entry point, shared infrastructure
- **Core modules**: Reusable utilities, UI components, data layers
- **Feature modules**: Isolated features, no cross-feature dependencies
- **Shared**: Cross-cutting concerns used by multiple modules

## Layered Architecture
- **Presentation**: UI + ViewModels/Presenters
- **Domain**: Business logic, use cases (when complex)
- **Data**: Repositories, data sources, models

## Dependency Rules
- Dependencies flow inward (Data -> Domain <- Presentation)
- Feature modules must not depend on other feature modules
- Core/shared modules have no feature dependencies
- Avoid circular dependencies

## State Management
- Use appropriate state management for the framework
- Separate UI state from one-off events
- Keep state immutable where possible

## Dependency Injection
- Prefer constructor injection
- Avoid service locators
- Scope dependencies appropriately

## Guidelines
- Document public APIs
- Keep modules independent and testable
- Follow framework conventions
- Evolve architecture via ADRs
