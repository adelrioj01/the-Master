# Decisions

## Durable coordination

Use a repository as the durable source of truth for project routing, decisions, handoffs, and verified status.

## Project isolation

Keep file-level work in the owning project. The coordinator does not assume cross-project filesystem access.

## Efficient routing

Use the lightest capable model and bounded prompts for routine work. Escalate only when ambiguity, failed verification, or complexity justifies it.

## Recoverable cleanup

Archive or quarantine by default. Protect active, source, handoff, and verified work. Verify exact targets before irreversible removal.

## Temporary usage overrides

The user may authorize a temporary usage-limit override for a specific account window and bounded tasks. The override must be recorded locally, expires when the window resets, and does not modify the permanent default policy.

## Public documentation boundary

Keep operational methodology public when useful, but omit local paths, project and chat identifiers, live usage values, credentials, and private project evidence.

## Chat context continuity

Whenever The Master creates a successor chat or project worker, pass a compact structured handoff from the relevant prior chat. Apply this to The Master itself and to every coordinated project. Transfer verified state, decisions, artifacts, blockers, and next action; do not transfer full transcripts or unrelated context.

## Successor chat cleanup

After a successor chat confirms that it has sufficient compact context and the predecessor has no unresolved state, archive the predecessor promptly. Treat archive as the supported recoverable equivalent of deletion; do not claim permanent deletion when the application only provides archive and unarchive.

## Documentation language

English is the canonical language for repository documentation, durable state, handoffs, evidence packets, and coordination prompts. Preserve non-English text only as clearly identified source evidence or user-provided material.

## Usage-first dispatch

Check live account usage before substantial dispatch. Default to one worker, distinguish account quota from context capacity, and roll long workers into successor chats through compact handoffs. Compaction reduces repeated context but does not recover usage already consumed.

The permanent warning boundary is 80% consumed in any applicable active usage window. At or above it, do not start or resume substantial workers without explicit user authorization. Treat unavailable ordinary usage, a reported rate-limit stop, or a fully consumed applicable window as the hard-stop boundary.

Use 60% consumed as an advisory boundary: report it, favor completion of the current verified milestone, and avoid starting work likely to reach 80%.

Use focused tests during implementation and complete project verification at integration or delivery, with earlier full verification when shared contracts, migrations, security boundaries, or cross-cutting configuration change.

Use direct search before Graphify. Query Graphify only for relationship-heavy or persistent architecture work, verify that an existing graph matches the current source revision, and do not enable automatic hooks, watch mode, or MCP service by default.

## Ponytail installation boundary

Install Ponytail globally as a validated skill only. Do not install its plugin, lifecycle hooks, band, or board. Use the skill for implementation, refactoring, dependency selection, and code review where smaller complete changes can reduce work. Do not load it for coordination, simple documentation, factual questions, or routine status reporting.
