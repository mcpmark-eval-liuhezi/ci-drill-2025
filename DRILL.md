# CI Drill 2025

This repository hosts a live-fire drill of the CI incident runbook.

## Workflows

- **Drill CI** (`.github/workflows/drill-ci.yml`) — triggered on push and manual dispatch; the `drill` job deliberately fails with `exit 1`.
- **Drill Soak** (`.github/workflows/drill-soak.yml`) — manual dispatch only; the `soak` job sleeps for ~20 minutes (1200s).

## Drill steps

1. Push a change to `main` to trigger the Drill CI workflow.
2. Wait for the run to go red, then capture the failed job log as evidence.
3. Open a tracking issue titled `CI drill: broken build on main` with the failed run id.
4. Dispatch the Drill Soak workflow and cancel it while it is in flight.
5. Re-run only the failed jobs of the Drill CI run.
6. Comment `DRILL COMPLETE` on the tracking issue.
