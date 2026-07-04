---
inclusion: auto
---

# Coding Standards

## General Conventions

- Use descriptive names for files, agents, hooks, and steering docs.
- Keep hook prompts focused — each hook should have a single clear responsibility.
- Use JSON for hook definitions and Markdown for agents and steering files.

## Hook Design

- Hooks should include clear CONDITION or EXCLUSION sections at the top of their prompts.
- Use matchers to limit hook scope to relevant tool invocations.
- Prefer `agent` action type for prompts that guide behavior; use `command` for shell-based automation.

## Steering Files

- Always include `inclusion: auto` front-matter for files that should be loaded in every session.
- Keep steering content concise and actionable — avoid verbose explanations.
- Update steering files when project structure or conventions change.

## Git Workflow

- Use descriptive commit messages with category prefixes: `Init:`, `Feat:`, `Fix:`, `Refactor:`, `Docs:`, `Chore:`.
- Keep commits focused on a single concern.
- Update README and steering docs before pushing to remote.
