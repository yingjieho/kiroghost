---
inclusion: auto
---

# Project Overview

## Purpose

Kiroghost is a Kiro IDE workspace configured with custom AI agents, hooks, skills, and steering files to streamline AI-powered development workflows.

## Architecture

The project is structured around the `.kiro/` configuration directory:

- **Agents** (`.kiro/agents/`) — Custom sub-agent definitions that can be invoked for specialised tasks (AI engineering, business analysis).
- **Skills** (`.kiro/skills/`) — Manually activatable expertise profiles that augment agent sessions with domain-specific knowledge.
- **Hooks** (`.kiro/hooks/`) — Event-driven automation that enforces workflows (commit approval gates, documentation sync, code cleanup).
- **Steering** (`.kiro/steering/`) — Persistent context and conventions included in agent interactions.
- **Specs** (`.kiro/specs/`) — Structured feature specifications with requirements, design, and implementation tasks.

## Key Design Decisions

- Agents and skills are separated: agents are autonomous sub-agents invoked for delegation, while skills are context injections that augment the current session.
- Hooks enforce quality gates (commit message approval) and automation (README/steering updates on push, code cleanup on file save).
- Git conventions are codified in steering to ensure consistent commit messages and branch workflows.
