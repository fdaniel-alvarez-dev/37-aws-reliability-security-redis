# SLOs and error budgets (practical template)

This document turns reliability goals into measurable targets.

## Service context
- What are we protecting? A customer-visible API / data pipeline / database.
- Top pains this repo targets:
  1) Making stateful services boring again—predictable performance, safe backups, and repeatable recovery drills.
  2) Replacing manual, risky changes with automation—repeatable workflows and safer operational runbooks.
  3) Enforcing security and governance without slowing delivery—explicit guardrails and production-safe validation paths.

## Suggested SLIs (examples)
- Availability: successful requests / total requests
- Latency: p95 / p99 per endpoint or per pipeline step
- Correctness: data validation pass rate (data roles)
- Recovery: time-to-restore from backup (database roles)

## Suggested SLOs (start conservative, iterate)
- Availability: 99.9% monthly
- Latency: p95 < 250ms for critical endpoints
- Recovery: restore drill succeeds in < 30 minutes

## Error budget policy
- If error budget burn is high, freeze risky changes, focus on stability.
- If stable, ship improvements with stronger automation.
