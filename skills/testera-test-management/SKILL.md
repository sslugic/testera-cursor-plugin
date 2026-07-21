---
name: testera-test-management
description: Manage Testera test projects, cases, plans, runs, environments and tasks via MCP. Use when the user wants to create or update QA artifacts in Testera, sync test coverage, or inspect run status.
---

# Testera test management

Use the hosted Testera MCP tools (`testera_*`) against the user's tenant.

## Auth

- Preferred: OAuth Connect on the `testera` MCP server (no API key in config).
- Optional: API key `tk_…` from Testera → Settings → API Keys, set as plugin variable `TESTERA_API_TOKEN`.

## Typical workflows

1. **Orient** — `testera_get_profile`, then `testera_list_projects`.
2. **Cases** — `testera_list_test_cases` with project filter; create/update with clear titles and steps.
3. **Plans / journeys** — `testera_list_test_plans` / `testera_create_test_plan` (`user_journey` when needed) with linked case IDs.
4. **Runs** — create or update runs; compare environments when asked.
5. **Hygiene** — use labels and assignees; avoid duplicate titles.

## Title format

Prefer `<fileBase> — <test name>` for imported automation cases. Do not put `[domain/kind]` prefixes in titles — those belong in Testera labels.

## Product links

- App: https://app.testera.io
- Marketing: https://testera.io
- MCP health: https://mcp.testera.io/health
