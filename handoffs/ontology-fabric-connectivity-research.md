# Ontology and Microsoft Fabric connectivity research

## Outcome

Identify safe, supported ways for an AI coding agent to help improve a Fabric-backed ontology without exposing credentials or HR data.

## Current evidence

No ontology artifact or schema export was available for direct review. Recommendations therefore remain architectural until metadata is supplied.

## Options

### Metadata export — recommended first step

Export table and column definitions, types, candidate keys, relationships, and status/date fields. This is the lowest-risk route for building an initial conceptual model without sharing row-level personal data.

### Read-only SQL profiling

If metadata alone cannot establish row grain, uniqueness, nulls, or status semantics, run a small read-only profiling pass using an existing authorized identity. Share aggregate outputs rather than raw HR rows.

### Restricted intermediary service

For ongoing integration, use an allowlisted read-only gateway or MCP service with least-privileged identity, secret storage, minimized responses, and controlled logging. Do not expose unrestricted query or write tools.

### Git integration

Use Git integration to version and review supported artifact definitions. Treat workspace synchronization as a separate write action requiring approval.

## Recommended ontology scope

Start with Person, Employment, Assignment, Job Profile or Position, and Organizational Unit. Record row grain, business keys, effective dates, status rules, relationship cardinality, and headcount semantics. Add pay and time-off concepts only after their sensitivity and meaning are validated.

## Next action

Provide metadata exports for the four core source tables. Use read-only profiling only when specific modeling questions remain unresolved.