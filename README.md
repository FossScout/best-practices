# Best Practices Library

Reusable guides, templates, and checklists shared across projects.

## Structure

- `guides/` — project-agnostic guides such as architecture, testing, security, and release process.
- `templates/` — reusable files such as ADR, PR, issue, editorconfig, and gitignore templates.
- `checklists/` — copy/paste checklists for reviews, releases, and audits.
- Domain directories such as `android/`, `kotlin/`, `git/`, and `security/` — focused decisions and practices.

## Using this library from another repository

Add this repository as a Git submodule at a stable in-repo path:

```bash
git submodule add https://github.com/FossScout/best-practices.git tools/best-practices
git commit -m "chore(docs): add shared best-practices submodule"
```

Clone with submodules:

```bash
git clone --recurse-submodules <project-url>
```

Existing clones:

```bash
git submodule update --init --recursive
```

Update the pinned library version deliberately:

```bash
git submodule update --remote tools/best-practices
git add tools/best-practices
git commit -m "chore(docs): update shared best practices"
```

Keep project-specific files local. In particular, do not symlink `.gitignore`, issue templates, PR templates, or project release runbooks to this repository; GitHub and contributors expect those files to exist directly in the project.

## License

Released under the [MIT License](LICENSE).
