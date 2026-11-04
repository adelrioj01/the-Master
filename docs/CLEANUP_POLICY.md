# Cleanup policy

The Master may keep the Codex workspace organized, but cleanup must preserve recoverability and project boundaries.

## Chat cleanup

Use reversible archive as the default action. A chat is an archive candidate only when all of these are true:

- It is not pinned.
- It is not the current Master chat or an active worker chat.
- It has no active turn, unresolved blocker, or recorded next action.
- Its material decisions, results, and handoff state are already captured in the registry or a handoff file.
- No current project task depends on its context.

The current Codex app exposes archive/unarchive for chats, not general hard deletion. The Master must not claim to delete a chat when it has only archived it.

## Document and artifact cleanup

The Master may propose cleanup of generated files or artifacts only after checking:

- exact absolute path or artifact identity;
- owner project and worker chat;
- whether the item is a source, input, handoff, verified deliverable, or reproducible intermediate;
- references from the registry, README files, tests, or other artifacts;
- whether a recoverable move to quarantine/trash is available.

Never remove source data, credentials, secrets, project configuration, unpushed work, the latest verified deliverable, or an artifact needed by an active worker. Do not treat age alone as evidence that an item is unnecessary.

## Required cleanup workflow

1. Inventory candidates without changing anything.
2. Classify each candidate and record the reason it is safe to remove or archive.
3. Present or record the exact targets, action, recovery path, and exclusions.
4. Archive chats or quarantine files where supported.
5. Use irreversible deletion only for exact disposable targets after the user has authorized that cleanup scope.
6. Reconcile the registry and record what changed.

Cleanup should be bounded: process a small candidate set, stop when the evidence is insufficient, and never use broad recursive deletion or unresolved globs to identify targets.

