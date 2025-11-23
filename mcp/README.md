# MCP Servers

This directory documents the MCP (Model Context Protocol) servers used by the workflow packs in this repository.

## What is MCP?

[Model Context Protocol](https://modelcontextprotocol.io/) is an open standard that enables AI assistants to interact with external tools and services. MCP servers provide capabilities like browser automation, mobile device control, and API integrations that extend what agents can do.

## Servers

| Server | Type | Repository | Used By |
|--------|------|------------|---------|
| [Playwright](./playwright.md) | Browser | [microsoft/playwright-mcp](https://github.com/microsoft/playwright-mcp) | [Web](../claude/web/README.md) |
| [Mobile MCP](./mobile-mcp.md) | Mobile | [mobile-next/mobile-mcp](https://github.com/mobile-next/mobile-mcp) | [Mobile](../claude/mobile/README.md) |

## Adding New Servers

When adding a new MCP server:

1. Create a new markdown file (e.g., `server-name.md`) with:
   - Repository link
   - Capabilities overview
   - Which workflows use it
   - High-level setup instructions
   - Link to repo for complete docs

2. Add an entry to the summary table above

3. Update relevant workflow pack READMEs to reference the dependency
