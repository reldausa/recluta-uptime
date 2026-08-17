# recluta-uptime

External uptime monitor for the Recluta bot (`n8n.recluta.app`).

A GitHub Action probes `/healthz` every ~10 minutes from GitHub's
infrastructure. Three consecutive failures (90s window) fail the workflow,
and GitHub emails the repo owner. Set up 2026-08-17 after a weekend outage
went unnoticed for 56 hours.
