# AI project deployment readiness

## Outcome

Prepare a meeting-ready deployment and production credential-migration plan without reading or changing credentials.

## Verified architecture

- A Python web application serves the interface and read-only API.
- A local database and downloaded documents require persistent storage.
- A separate scheduled pipeline collects data and optionally generates AI summaries.
- Production readiness depends on hosting, storage, access controls, monitoring, billing ownership, and rollback planning.

## Deployment checklist

1. Select the approved hosting platform, domain, application owner, and intended audience.
2. Use a tested Python runtime and install pinned or reviewed dependencies.
3. Allocate persistent storage for the database, documents, logs, and pipeline state.
4. Begin with one application instance and one scheduled worker.
5. Back up data and test restoration.
6. Deploy a specific verified revision.
7. Start staging without paid AI generation.
8. Run health, API, persistence, scheduling, and download smoke tests.
9. Add uptime, failed-job, storage, backup, and freshness monitoring.
10. Define launch ownership and rollback authority.

## Credential migration

- Create a production-specific credential under the approved billing project.
- Store it only in the deployment platform's secret manager.
- Grant it only to the worker that requires AI generation.
- Never commit development environment files or secret values.
- Verify staging and one controlled request before revoking the old credential.
- Confirm quotas, rate limits, alerts, and spending ownership.

## Important risks

Public access requires explicit decisions about authentication, throttling, HTTPS, storage concurrency, monitoring, and cost controls. Do not deploy or rotate credentials solely from this handoff.