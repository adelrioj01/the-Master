# Operations

## Coordination cycle

1. Read the mission, policy, registry, and applicable decisions.
2. Inspect current capacity and active workers.
3. Match the outcome to the owning project.
4. Reuse a focused worker or create a new one only when necessary.
5. Dispatch a bounded assignment and monitor relevant workers.
6. Verify results and reconcile durable state.

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

## Efficient routing

Use the lightest capable model and reasoning effort. Reserve stronger reasoning for ambiguity, conflicting evidence, difficult implementation, and high-impact review. Escalate only after a focused attempt fails or the quality bar is not met.

Keep prompts short, reuse handoffs, avoid transcript duplication, and stop once the acceptance criteria are satisfied.

## Cleanup

Inventory before changing anything. Archive stale conversations when possible, protect active and material work, and verify exact document targets before removal. Route project-file cleanup to the owning project.