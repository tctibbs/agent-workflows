# GEMINI.md

This file provides guidance to the Gemini CLI when working with code in this repository.

## Project Overview

This repository contains reusable agentic workflow packs for the Gemini CLI. Each workflow pack includes slash commands, and optionally GitHub Actions that work together to accomplish specific tasks like code reviews, design reviews, and security scanning.

## Directory Structure

```
agent-workflows/
├── gemini/                    # Workflow packs organized by platform
│   ├── general/               # Platform-agnostic workflows
│   │   └── security-review/   # Security scanning workflow pack
│   └── web/                   # Web platform workflows
│       └── design-review/     # Design review with Playwright
├── context/                   # Shared context documents
│   └── design-principles.md   # Reusable design standards
└── mcp/                       # MCP server documentation
    ├── playwright.md          # Playwright MCP setup
    └── mobile-mcp.md          # Mobile MCP setup
```

## Workflow Pack Structure

Each workflow pack follows a consistent structure:

```
workflow-name/
├── README.md         # Overview, concept, and usage instructions
├── commands/         # Slash commands (markdown files with frontmatter)
└── actions/          # GitHub Actions workflow files (optional)
```

### Slash Commands

Command files use YAML frontmatter (this format might vary for Gemini, treat as a placeholder):

```yaml
---
allowed-tools: Bash, Glob, Grep, ...
description: Command description
---

Command prompt with dynamic shell commands using !`command` syntax
```

Commands can embed dynamic values using `!`backtick syntax` to execute shell commands inline (e.g., `!`git diff`).

### GitHub Actions

Action files follow standard GitHub Actions YAML format and typically integrate with Gemini tools via custom scripts or actions (e.g., `gemini-cli-action@v1`).

## Context Files

The `/context` directory contains shared documents that workflow packs reference:

- **design-principles.md**: Comprehensive UI/UX checklist inspired by Stripe, Airbnb, and Linear

These files define reusable reasoning rules that can be referenced by agents and commands across multiple workflow packs.

## MCP Server Integration

Some workflows require MCP (Model Context Protocol) servers:

- **Playwright MCP**: Browser automation for web-based workflows (design review)

Each MCP server has documentation in `/mcp` with setup instructions.

## Conventions

### File Naming
- Command files: Match the agent name for consistency
- Action files: Use descriptive names (e.g., `code-review.yml`, `code-review-custom.yml`)

### Command Patterns
- Include git context using dynamic shell commands (`git status`, `git diff`, etc.)
- Reference context files using relative paths from the project root
- Specify all required tools in the frontmatter

### Content Style
- Agent system prompts should be directive and establish expertise
- Include structured output formats (Summary, Findings, Priority levels)
- Reference engineering principles (SOLID, DRY, KISS) where applicable
- Categorize issues by severity (Critical, Important, Minor/Nit)

## Adding New Workflow Packs

1. Create a new directory under the appropriate platform (`general/`, `web/`)
2. Add a `README.md` with concept overview, methodology, and resource links
3. Create `commands/` directory with command markdown files
4. Optionally add `actions/` for GitHub Actions workflows
5. Update the root `README.md` to include the new workflow
6. If the workflow requires an MCP server, document it in `/mcp`

## Installation Pattern

Workflows are installed by copying assets to the user's Gemini directory (e.g., `~/.gemini/`):

```bash
# Copy commands
cp -r workflow-name/commands/* ~/.gemini/commands/

# Copy actions to target project
cp workflow-name/actions/*.yml project/.github/workflows/
```