# Usage and context policy

## Account protection

Use the live application usage indicator before substantial dispatches. When usage approaches the configured warning boundary, do not start new workers; summarize or finish the safest bounded step. At the hard-stop boundary, pause dispatch and resume only after reset or explicit authorization.

The coordinator must distinguish account usage from chat context capacity. Creating a successor chat or compacting a transcript reduces repeated context input but does not restore account quota already consumed.

Default to one substantial worker at a time. Use at most two parallel workers only when live usage is verified as comfortably below the warning boundary and both tasks are short and independent. If live usage cannot be verified, do not parallelize.

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
