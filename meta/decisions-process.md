# Best Practices Evolution Process

This document defines how the best-practices library evolves over time.

## Principles
- Decisions should be practical and enforceable
- Keep changes minimal and well-documented
- Prefer consensus through discussion
- Maintain backward compatibility where possible

## Proposing Changes
1. **Identify need**: Document the problem or gap
2. **Research**: Look at existing decisions, consider alternatives
3. **Draft proposal**: Create/update `decisions.md` in relevant domain or new ADR
4. **Discuss**: Open an issue/PR with rationale and tradeoffs
5. **Review**: Get feedback from stakeholders
6. **Decide**: Update status to Accepted/Rejected

## Documenting Decisions
- For domain-wide rules, update `best-practices/<domain>/decisions.md`
- For significant architectural/process changes, create an ADR in `templates/` context or project ADRs
- Include: context, options, decision, consequences

## Review Process
- Changes to core decisions require review
- Templates and checklists can be updated more freely if they improve usability
- Breaking changes to established practices should be clearly communicated

## Maintenance
- Review best practices periodically
- Mark deprecated practices clearly
- Keep README index up to date
- Remove outdated guidance

## Versioning
- This library is used by reference (not versioned as a package currently)
- Document major changes in commit messages
- Consider tagging if it becomes a shared dependency
