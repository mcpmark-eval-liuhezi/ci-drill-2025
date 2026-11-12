# ci-drill-2025

Throwaway public repo hosting a live-fire CI incident runbook drill.

## Workflows

- **Drill CI** (`.github/workflows/drill-ci.yml`): triggered on `push` (main) and `workflow_dispatch`; job `drill` deliberately fails with `exit 1`.
- **Drill Soak** (`.github/workflows/drill-soak.yml`): manual dispatch only; job `soak` sleeps for ~20 minutes (1200s).

This repo is disposable and exists solely for the on-call rotation CI drill.
