# CLAUDE.md

This file provides guidance for AI assistants (Claude and others) working in this repository.

---

## Repository Overview

This is a new repository. As the project grows, update this file to reflect the actual codebase structure, conventions, and workflows.

---

## Project Structure

```
Rep1/
├── CLAUDE.md          # This file — AI assistant guidance
└── ...                # Add structure here as files are created
```

> Update this tree as the project develops.

---

## Development Workflow

### Branching Convention

- Feature branches: `feature/<short-description>`
- Bug fixes: `fix/<short-description>`
- AI-generated work: `claude/<task-description>-<session-id>`
- Never push directly to `main` or `master` without review.

### Commit Messages

Use the imperative mood with a concise subject line (≤72 chars):

```
Add user authentication module
Fix null pointer in order processor
Refactor database connection pooling
```

For larger commits, add a body after a blank line explaining *why*, not *what*.

### Pull Requests

- PRs should reference the relevant issue if one exists.
- Include a brief summary, test plan, and any notable trade-offs.
- Squash or rebase before merging to keep history clean.

---

## Build & Test

> Fill in the actual commands once the project tech stack is established.

```bash
# Install dependencies
# <command>

# Run tests
# <command>

# Build / compile
# <command>

# Lint / format
# <command>
```

---

## Key Conventions

### Code Style

- Follow the language/framework conventions standard for this project.
- Prefer clarity over cleverness.
- Keep functions small and single-purpose.
- Delete dead code rather than commenting it out.

### Error Handling

- Validate at system boundaries (user input, external APIs).
- Do not add defensive error handling for internal invariants that cannot fail.
- Propagate errors rather than swallowing them silently.

### Testing

- Write tests for all new functionality.
- Unit tests live alongside source files or in a dedicated `tests/` directory.
- Prefer deterministic, isolated tests with no external dependencies.

### Security

- Never commit secrets, credentials, API keys, or `.env` files.
- Sanitize and validate all external input.
- Avoid common vulnerabilities: SQL injection, XSS, command injection, path traversal.

---

## AI Assistant Instructions

When working in this repository, an AI assistant should:

1. **Read before editing.** Always read the relevant files before making changes.
2. **Minimal changes.** Only modify what is necessary for the task at hand.
3. **No unnecessary files.** Do not create documentation, README stubs, or boilerplate unless explicitly requested.
4. **No over-engineering.** Do not add abstractions, helpers, or features beyond what was asked.
5. **Prefer editing over creating.** Extend existing files rather than creating new ones when possible.
6. **Verify before committing.** Run linters and tests (when available) before committing.
7. **Descriptive commits.** Write clear commit messages that explain the change.
8. **Branch discipline.** Develop on the designated branch; never push to main without permission.
9. **Ask when uncertain.** If requirements are ambiguous, ask rather than guess.
10. **Update this file.** When significant new patterns, tooling, or conventions are established, update CLAUDE.md.

---

## Environment & Configuration

| Item | Details |
|------|---------|
| Repository | `marcelohralves-cell/Rep1` |
| Primary branch | `main` (or `master`) |
| AI work branches | `claude/<description>-<session-id>` |

> Add environment variables, required tools, and local setup steps here as the project develops.

---

## Updating This File

This file should evolve with the project. When you:
- Add a new tech stack or framework → document build/test commands
- Establish a new code convention → add it to the Conventions section
- Add CI/CD → document the pipeline
- Define env var requirements → list them in the Environment section

Keep this file concise and accurate. Outdated guidance is worse than no guidance.
