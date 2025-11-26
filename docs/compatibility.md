# Workflow Compatibility

Quick reference for workflow availability across AI coding assistants.

## Compatibility Matrix

| Workflow | Claude | Gemini | Cursor | Codex |
|----------|--------|--------|--------|-------|
| **General** |
| Code Review | ✓ | · | ✗ | ✗ |
| Security Review | ✓ | · | ✗ | ✗ |
| **Web** |
| Design Review | ✓ | · | ✗ | ✗ |
| **Mobile** |
| iOS Developer | ✓ | ✗ | ✗ | ✗ |
| iOS Design Review | ✓ | ✗ | ✗ | ✗ |

**Legend:** ✓ Full · Partial ✗ Not available

## Platform Notes

### Claude Code

Full implementation with:
- Agents (subagents with specialized prompts)
- Commands (slash commands with dynamic git context)
- GitHub Actions (automated PR reviews)
- MCP integration (Playwright, Mobile MCP)

### Gemini CLI

Partial implementation with:
- TOML-based commands
- Growing workflow support

### Cursor / Codex

Not yet available. Planned for future support.
