# Playwright MCP

Browser automation server that enables agents to interact with web pages in real-time.

**Repository:** [microsoft/playwright-mcp](https://github.com/microsoft/playwright-mcp)

## Capabilities

- Navigate to URLs and capture accessibility snapshots
- Click, type, and interact with page elements
- Take screenshots (viewport, full page, or specific elements)
- Fill forms and handle dialogs
- Capture console messages and network requests
- Manage browser tabs

## Used By

- [Web / Design Review](../claude/web/design-review/README.md) - Visual verification, accessibility testing, responsive design checks

## Setup

### Prerequisites

- Node.js 18+
- Claude Code CLI

### Installation

Add Playwright MCP using the CLI command:

```bash
claude mcp add --transport stdio playwright -- npx -y @playwright/mcp@latest
```

This will:
- Add the Playwright MCP server to your configuration
- Store it in `~/.claude.json` (user scope) by default
- Verify the connection on next restart

**For project-specific configuration** (committed to git):
```bash
claude mcp add --transport stdio playwright --scope project -- npx -y @playwright/mcp@latest
```

This creates `.mcp.json` in your project root.

### Verify Installation

After adding, verify the configuration:

```bash
# List all configured MCP servers
claude mcp list

# Check Playwright connection status
claude mcp get playwright
```

Then **restart Claude Code** and verify with `/mcp` command.

### Browser Installation

Install Chromium browser for Playwright:

```bash
npx playwright install chromium
```

You can also install additional browsers as needed:
```bash
npx playwright install firefox
npx playwright install webkit
```

## Full Documentation

For complete setup instructions, configuration options, and troubleshooting, see the official repository:

[microsoft/playwright-mcp](https://github.com/microsoft/playwright-mcp)
