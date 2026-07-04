---
inclusion: auto
---

# Coding Standards

## File Organisation

- Agent definitions go in `.kiro/agents/` as markdown files with YAML front-matter (name, description, tools).
- Skills go in `.kiro/skills/` as markdown files with `inclusion: manual` front-matter.
- Hooks go in `.kiro/hooks/` as JSON files created via the `createHook` tool.
- Steering files go in `.kiro/steering/` as markdown with `inclusion: auto` or `inclusion: manual` front-matter.

## Naming Conventions

- Use kebab-case for all `.kiro/` file names (e.g., `business-analyst.md`, `git-commit-approval.json`).
- Use descriptive, role-based names for agents and skills (e.g., `business-analyst`, `data-engineer`).
- Hook IDs should describe their purpose concisely (e.g., `git-commit-approval`, `lint-on-save`).

## Documentation Style

- Use British English spelling in documentation and agent prompts (e.g., "analyse", "organisation").
- Structure markdown with clear headings, tables for reference data, and bullet lists for enumeration.
- Keep front-matter minimal — only include required fields.

## Git Conventions

- Commit message prefixes: `Init:`, `Feat:`, `Fix:`, `Refactor:`, `Docs:`, `Kiro:`, `Chore:`
- Use `Kiro:` prefix for all changes to `.kiro/` directory contents.
- Stage specific files rather than using `git add .`.
- Subject lines under 72 characters.
