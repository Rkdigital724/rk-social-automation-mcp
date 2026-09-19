# Changelog

## 2.0.1 — Hardening

- Added content-platform/account-platform matching guards before scheduling and publishing.
- Added expired social-account credential checks.
- Implemented the documented `create_weekly_plan` automation action.
- Normalized non-finite analytics input values.
- Added regression tests for publishing safety and weekly automation.
- Verified source syntax and automated test suite: **8/8 passing**.

## 2.0.0 — Complete nine-phase architecture

- Consolidated the nine planned automation phases into one standalone MCP agent.
- Added brand intelligence, content, campaigns, creative briefs, scheduling, publishing adapters, analytics, optimization and automation worker.
