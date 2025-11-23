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

Add to your Claude Code MCP configuration:

```json
{
  "mcpServers": {
    "playwright": {
      "command": "npx",
      "args": ["-y", "@anthropic/playwright-mcp"]
    }
  }
}
```

### Prerequisites

- Node.js 18+

### Browser Installation

After adding the MCP config, install Chromium:

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
