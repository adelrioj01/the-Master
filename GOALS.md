# Goals

## Purpose

Provide a durable, local control plane for coordinating Alberto's Codex projects across multiple chats.

## Desired outcomes

- New chats can recover the orchestration policy and current state from repository files.
- Work is routed to the correct project and duplicate workers are avoided.
- The five-hour usage window stays below the configured 40% hard stop.
- High-context chats are replaced with focused chats using concise handoffs.
- Material decisions, blockers, and next actions survive chat turnover.

## Success conditions

- `AGENTS.md` is present and concise enough to load on every chat.
- The project registry identifies each known project and its role.
- Active work has an owner, status, next action, and handoff location.
- Usage checks happen before substantial dispatches and during the recurring guard.
- A new chat can continue using only this repository and current Codex thread state.

## Non-goals

- Combining all project files into this repository.
- Bypassing project permissions or sandbox boundaries.
- Guaranteeing exact per-chat token accounting when the app does not expose it.
- Automatically making destructive, external, deployment, or sharing changes.


