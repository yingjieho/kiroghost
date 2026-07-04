---
inclusion: always
---

# Git Conventions

## Branch Strategy

- The default branch is `main`. Always push to `main` unless explicitly told otherwise.
- Never push directly to `main` for feature work in established projects — use feature branches and PRs.
- For initial project setup or scaffolding, pushing directly to `main` is acceptable.

## Commit Messages

- Use descriptive commit messages that clearly state what was done.
- Prefix with a category when appropriate: `Init:`, `Fix:`, `Feat:`, `Refactor:`, `Docs:`, `Kiro:`, `Chore:`.
- Keep the subject line under 72 characters.
- Category guidelines:
  - `Init:` — initial project setup or scaffolding
  - `Feat:` — new features or functionality
  - `Fix:` — bug fixes
  - `Refactor:` — code restructuring without behavior change
  - `Docs:` — updates to documentation files (README, guides, etc.)
  - `Kiro:` — changes to files in the `.kiro` directory (steering, hooks, specs, skills, settings)
  - `Chore:` — maintenance tasks, dependency updates, CI config
- Examples:
  - `Init: Added .kiro directory with agents, hooks, skills`
  - `Feat: Add user authentication endpoints`
  - `Fix: Resolve null pointer in payment processing`
  - `Docs: Update README with setup instructions`
  - `Kiro: Add git-conventions steering file`

## Commit-to-Push Workflow (Human Approval Gate)

After creating a commit, you MUST follow this workflow before pushing:

1. **Create the commit** — stage files and commit with a well-formed message.
2. **Present the commit message for approval** — display the commit message to the user and explicitly ask for their approval before pushing. Use a clear prompt like:
   > "Here's the commit message I've prepared: `<message>`. Approve to push to remote?"
3. **Wait for human approval** — do NOT proceed with `git push` until the user explicitly confirms.
4. **Push only after approval** — once the user approves, push to the remote.

If the user rejects the commit message:
- Amend the commit with a revised message based on their feedback.
- Present the revised message for approval again.
- Repeat until approved.

**This approval gate is mandatory.** Never push to remote without explicit user confirmation of the commit message.

## Push Workflow

- Always set up tracking with `-u` on first push: `git push -u origin main`
- If the remote has commits not in local history (e.g., GitHub-created README), merge with `--allow-unrelated-histories` before pushing.
- Stage specific files rather than using `git add .` to avoid committing unintended changes.

## General Rules

- Do not modify git config.
- Do not use destructive commands (force push, reset --hard, clean -fd) without explicit permission.
- Do not skip hooks (--no-verify) unless explicitly asked.
- Prefer non-interactive git commands.
