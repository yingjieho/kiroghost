---
inclusion: auto
---

# Project Overview

## Purpose

Kiroghost is a Kiro IDE workspace configured with custom AI agents, hooks, and automation for AI-powered development workflows.

## Architecture

The project is structured around Kiro's `.kiro/` configuration directory:

- **Agents** (`.kiro/agents/`): Custom agent definitions with specialized capabilities. Currently includes an `ai-engineer` agent for building AI tools, applications, MCP servers, and development infrastructure.
- **Hooks** (`.kiro/hooks/`): Automated triggers that fire on IDE events. Includes:
  - `cleanup-after-codegen.json` — Cleans up, refactors, and checks for errors after code generation.
  - `update-readme-and-steering.json` — Updates README and steering docs before pushing to remote.
- **Steering** (`.kiro/steering/`): Always-included context files that guide agent behavior with project conventions and architecture knowledge.

## Tech Stack

- Kiro IDE with custom agent and hook configurations
- Git for version control
- Markdown and JSON for configuration
