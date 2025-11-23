```
 █████╗  ██████╗ ███████╗███╗   ██╗████████╗
██╔══██╗██╔════╝ ██╔════╝████╗  ██║╚══██╔══╝
███████║██║  ███╗█████╗  ██╔██╗ ██║   ██║
██╔══██║██║   ██║██╔══╝  ██║╚██╗██║   ██║
██║  ██║╚██████╔╝███████╗██║ ╚████║   ██║
╚═╝  ╚═╝ ╚═════╝ ╚══════╝╚═╝  ╚═══╝   ╚═╝
        W O R K F L O W S
```

A personal, curated collection of reusable agentic workflow packs containing agents, slash commands, and shared context files built to enhance my developer experience using agentic tools like Claude Code.

These workflow packs are designed around how I prefer to structure reviews, organize context, and interact with agentic systems across my projects. This repo is not a framework or a standard — just the patterns and tools I personally rely on.

## 📦 Workflow Packs

### [Web](./claude/web/README.md)

Web platform workflows using browser automation.

- **[Design Review](./claude/web/design-review/README.md)** - UI/UX critique with Playwright integration

### [Mobile](./claude/mobile/README.md)

Mobile platform workflows for iOS and Android development.

- **[iOS Developer](./claude/mobile/agents/ios-developer.md)** - Swift 6/SwiftUI expert agent

### [General](./claude/general/README.md)

Platform-agnostic workflows for any codebase.

- **[Code Review](./claude/general/code-review/README.md)** - Architecture-informed code feedback
- **[Security Review](./claude/general/security-review/README.md)** - Lightweight vulnerability scanning

## 🔌 MCP Servers

Some workflow packs require MCP (Model Context Protocol) servers for enhanced capabilities like browser automation and mobile device control. See [mcp/README.md](./mcp/README.md) for setup instructions and server details.

## 🧠 Shared Context

All workflow packs draw from the shared documents in `/context`.
These files define reusable reasoning rules for things like:

- design reviews
- code analysis
- architectural expectations

Projects can override or extend these within their local project context.

## Note

This is a personal toolbox. Everything here is tailored to my workflow, my style, and my expectations of agent behavior.  

Feel free to adapt or reuse anything that’s helpful!
