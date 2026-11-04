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