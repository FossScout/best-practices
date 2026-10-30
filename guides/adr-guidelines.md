# ADR Index Guidelines

Use this to maintain an ADR index in projects.

## Naming
- `NNNN-short-title.md` where NNNN is sequential (0001, 0002, ...)
- Use kebab-case for title
- Start from 0000 for template if desired

## Index Format
Create `docs/adr/README.md` with:
```markdown
# Architecture Decision Records

| ADR | Title | Status | Date |
|---|------|--------|------|
| `0001` | Use an example decision | Accepted | YYYY-MM-DD |
```

## Workflow
1. Copy template from best-practices to `docs/adr/NNNN-title.md`
2. Fill in sections
3. Add to index
4. Link from relevant docs if needed
5. Update status as decisions evolve
