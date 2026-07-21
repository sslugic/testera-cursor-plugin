# Marketplace submission notes

## Official Cursor Marketplace

1. Sign in at [cursor.com/marketplace/publish](https://cursor.com/marketplace/publish)
2. Paste repository URL:

```text
https://github.com/sslugic/testera-cursor-plugin
```

3. Submit for manual review (open source required).

Optional email: `kniparko@anysphere.com` with the same repo link.

## Community directory

1. [cursor.directory/plugins/new](https://cursor.directory/plugins/new)
2. Sign in with GitHub
3. Paste the same repository URL and submit

## Checklist

- [x] `.cursor-plugin/plugin.json` with unique `name: testera`
- [x] `mcp.json` → `https://mcp.testera.io/mcp`
- [x] `.mcp.json` (directory auto-detect)
- [x] Logo `assets/logo.svg`
- [x] README + MIT license
- [x] Skill + rule with frontmatter
- [x] Public GitHub repo
- [x] Local test path `~/.cursor/plugins/local/testera`
