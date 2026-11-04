# Decisions

## Durable coordination

Use a repository as the durable source of truth for project routing, decisions, handoffs, and verified status.

## Project isolation

Keep file-level work in the owning project. The coordinator routes work through project workers and does not assume cross-project filesystem access.

## Efficient routing

Use the lightest capable model and bounded prompts for routine work. Escalate only when ambiguity, failed verification, or task complexity justifies it.

## Recoverable cleanup

Archive or quarantine material by default. Protect active, pinned, source, handoff, and verified work. Verify exact targets before irreversible removal.