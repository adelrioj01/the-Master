# Operations

## Coordination cycle

1. Read the mission, policy, registry, and applicable decisions.
2. Inspect current capacity and active workers.
3. Match the outcome to the owning project.
4. Reuse a focused worker or create a new one only when necessary.
5. Before creating a new chat, compact the relevant prior chat into a structured handoff.
6. Dispatch a bounded assignment with that handoff and monitor relevant workers.
7. Verify results and reconcile durable state.

## Task lifecycle

Use:

`queued → assigned → running → review → complete`

Use `blocked` when progress requires a decision, permission, missing artifact, or unavailable worker.

Each evidence packet should contain only:

- objective and acceptance criteria;
- owner project and worker;
- verified findings and changed artifacts;
- review or test evidence;
- risks, blockers, and next action.

## Context continuity between chats

Every new chat or worker created by The Master must receive a compact context packet from the relevant predecessor. This rule applies both to successor chats in The Master and to workers in every coordinated project.

The packet must contain:

- objective, scope, acceptance criteria, and stop condition;
- verified current state and lifecycle status;
- decisions already made and constraints that remain in force;
- relevant artifacts and changed files, using private local references only where permitted;
- verification or test evidence;
- unresolved blockers, risks, and the single next action.

Do not paste the prior transcript or assume access to it. Exclude superseded discussion, speculation, secrets, credentials, private identifiers from public files, and unrelated project context. If there is no relevant predecessor, state that the worker starts from repository and registry evidence only.

Before dispatch, verify that the packet names the owning project and distinguishes confirmed facts from inferences. After completion, replace stale state with the worker's verified outcome in the registry or a handoff.

## Documentation language

Use English for all repository documentation, durable state, handoffs, evidence packets, and prompts created by The Master. Non-English material may appear only when preserving source evidence or a user-provided artifact; identify it as quoted or source material and provide an English operational summary when relevant.

## Efficient routing

Use the lightest capable model and reasoning effort. Reserve stronger reasoning for ambiguity, conflicting evidence, difficult implementation, and high-impact review. Escalate only after a focused attempt fails or the quality bar is not met.

Keep prompts short, reuse handoffs, avoid transcript duplication, and stop once the acceptance criteria are satisfied.

## Cleanup

Inventory before changing anything. Archive stale conversations when possible, protect active and material work, and verify exact document targets before removal. Route project-file cleanup to the owning project.
