# The Master

The Master is a local Codex orchestration project. Its documentation is the durable source of truth for coordinating work across Alberto's Codex projects without depending on one conversation.

## Start here

1. Open this folder as a Codex project.
2. Start a new chat from this project.
3. Ask the chat to read `AGENTS.md`, `GOALS.md`, `PLANS.md`, and `state/REGISTRY.md`.
4. Give it the project outcome or coordination task.

Codex reads `AGENTS.md` automatically when a chat runs from this repository. The other files preserve goals, operating policy, project mappings, decisions, and handoffs across chats.

## Repository map

- `AGENTS.md` — binding instructions for every agent working here.
- `GOALS.md` — outcomes, scope, and success conditions.
- `PLANS.md` — operating phases and next improvements.
- `docs/OPERATIONS.md` — coordination workflow.
- `docs/PROJECTS.md` — known project inventory and routing guidance.
- `docs/SETUP.md` — one-time Codex project registration.
- `docs/USAGE_POLICY.md` — five-hour usage and token safeguards.
- `docs/CLEANUP_POLICY.md` — safe chat archiving and generated-artifact cleanup rules.
- `state/REGISTRY.md` — compact live registry of workers and work.
- `state/DECISIONS.md` — durable decisions and unresolved questions.
- `handoffs/TEMPLATE.md` — required format for moving work to a fresh chat.

## Important limitation

The Master coordinates projects through Codex project and thread tools. A chat does not automatically gain filesystem access to every project. Work that requires project files should run in a chat created for that project. The Master keeps the registry and routes the work.
