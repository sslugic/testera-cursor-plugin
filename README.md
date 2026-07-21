# Testera for Cursor

Official Cursor plugin for [Testera](https://testera.io) — AI-assisted test management.

Install from the Cursor Marketplace (or this repo) to connect the hosted MCP server at [`https://mcp.testera.io/mcp`](https://mcp.testera.io/mcp). Create projects, test cases, plans, runs, environments, and tasks from chat.

## Install

### Marketplace (recommended)

1. Open **Cursor → Customize → Plugins** (or browse [cursor.com/marketplace](https://cursor.com/marketplace)).
2. Search for **Testera** and install.
3. Open **Settings → Tools & MCP**, find **testera**, click **Connect**.
4. Sign in with your Testera account (email/password or Google).

### Local / development

```bash
mkdir -p ~/.cursor/plugins/local/testera
cp -R ./* ~/.cursor/plugins/local/testera/
# ensure .cursor-plugin/plugin.json is at that root
```

Reload Cursor (`Developer: Reload Window`), then **Connect** the `testera` MCP server.

## What you get

| Component | Purpose |
|-----------|---------|
| **MCP server** | Remote Streamable HTTP MCP at `mcp.testera.io` |
| **Skill** | `testera-test-management` — workflows for cases, plans, runs |
| **Rule** | Guidance to use Testera MCP instead of ad-hoc trackers |

### MCP tools (examples)

- `testera_get_profile`, `testera_list_projects`, `testera_create_project`
- `testera_list_test_cases`, `testera_create_test_case`, `testera_update_test_case`
- `testera_list_test_plans`, `testera_create_test_plan` (including user journeys)
- `testera_list_test_runs`, `testera_create_test_run`, `testera_update_test_run`
- Environments, tasks, labels, assignees

## Auth

**Preferred:** OAuth Connect (no API key in config). This plugin ships:

```json
{
  "mcpServers": {
    "testera": {
      "url": "https://mcp.testera.io/mcp"
    }
  }
}
```

**Optional API key:** create a key in Testera → **Settings → API Keys**, then add headers manually:

```json
{
  "mcpServers": {
    "testera": {
      "url": "https://mcp.testera.io/mcp",
      "headers": {
        "Authorization": "Bearer tk_<keyId>_<secret>"
      }
    }
  }
}
```

## Links

- Product: [testera.io](https://testera.io)
- App: [app.testera.io](https://app.testera.io)
- MCP health: [mcp.testera.io/health](https://mcp.testera.io/health)
- Server source: [sslugic/testara](https://github.com/sslugic/testara) (`mcp/testera-server`)

## Privacy & security

- The plugin does **not** ship secrets.
- Auth uses Testera OAuth or your own API key.
- See [Testera privacy / DPA](https://testera.io) for vendor review docs.

## License

MIT
