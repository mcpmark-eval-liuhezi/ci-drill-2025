# CI Drill Repository

This is a throwaway public repo used for a live-fire drill of the CI incident runbook.

## Workflows
- `.github/workflows/drill-ci.yml` — "Drill CI": triggered on push and manual dispatch; contains a job that deliberately fails (`exit 1`).
- `.github/workflows/drill-soak.yml` — "Drill Soak": manual dispatch only; single job that sleeps ~20 minutes.
