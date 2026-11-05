# Usage and context policy

## Account protection

Use the live application usage indicator before substantial dispatches. The advisory boundary is 60% consumed in any applicable active account-usage window. At or above it, report the condition, prefer finishing the current verified milestone, and avoid starting work likely to cross the warning boundary. The warning boundary is 80% consumed. At or above it, do not start or resume substantial workers; finish only the safest bounded step, capture a compact handoff, and wait for reset or explicit user authorization. The hard-stop boundary is reached when ordinary usage is unavailable, a rate limit is reported as reached, or the applicable window is fully consumed; preserve state and stop all dispatch.

The coordinator must distinguish account usage from chat context capacity. Creating a successor chat or compacting a transcript reduces repeated context input but does not restore account quota already consumed.

Default to one substantial worker at a time. Use at most two parallel workers only when live usage is verified as comfortably below 80% consumed and both tasks are short and independent. If live usage cannot be verified, do not parallelize.

## Model selection

- Efficient tier: triage, extraction, routine inspection, and short summaries.
- Balanced tier: complex technical work, debugging, architecture, and coordinated deliverables.
- Frontier tier: ambiguous problems, conflicting evidence, demanding synthesis, and high-impact review.

Use the lowest reasoning effort that meets the acceptance criteria. Escalate after evidence, not intuition.

## Context efficiency

- Send compact briefs with relevant facts and constraints only.
- Reuse evidence packets and handoffs instead of repeating discovery.
- Parallelize independent reviews and synthesize once.
- Use bounded outputs, stop conditions, and focused verification passes.
- Do not store credentials, secrets, private identifiers, or full transcripts.
- Roll over to a successor chat when a worker has mixed objectives, repeated discovery, multiple resumptions, or enough history that the next step would reread substantial context. Pass only a compact verified handoff and the relevant artifact references.

## Verification strategy

- During implementation, run the smallest focused checks that cover the changed behavior and its direct callers.
- Run the complete project verification suite at integration, before delivery, or when shared contracts, migrations, security boundaries, or cross-cutting configuration change.
- Do not repeat a complete suite after documentation-only or unrelated changes unless project instructions require it.
- Record pre-existing failures separately and require evidence that the bounded change did not add regressions.
