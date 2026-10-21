# recluta-uptime

External uptime monitor for the Recluta bot (`n8n.recluta.app`).

A GitHub Action probes `/healthz` every ~10 minutes from GitHub's
infrastructure. Three consecutive failures (90s window) fail the workflow,
and GitHub emails the repo owner. Set up 2026-08-17 after a weekend outage
went unnoticed for 56 hours.

**Schedule caveats (2026-10-21).** GitHub runs scheduled workflows on a
best-effort basis and throttles quiet repositories: by October the "every 10
minutes" cron was actually running every 3-5 hours, so this catches a long
outage, not a short one. It also disables the schedule after 60 days without a
commit; the `keepalive` job pushes an empty commit once the last one is 30 days
old. If the Actions tab ever shows the workflow as disabled, re-enable it there.

