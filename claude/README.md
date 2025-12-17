# Claude Workflows

This directory contains reusable agentic workflow packs for Claude Code, organized by platform and domain.

## General Workflows

Platform-agnostic workflows that apply to any codebase regardless of language or platform.

#### [Code Review](./general/code-review/README.md)
Architecture-informed code review with severity triage. GitHub Actions for automated PR reviews.

#### [Security Review](./general/security-review/README.md)
OWASP-based vulnerability detection with severity classification and remediation guidance.

---

## Development Workflows

Language and framework-specific agents and skills for building software.

### Python

**Agents:**
- **[python-developer](./development/python/agents/python-developer.md)** - Modern Python 3.12+, uv, ruff, async patterns
- **[fastapi-developer](./development/python/agents/fastapi-developer.md)** - FastAPI, SQLAlchemy 2.0, Pydantic V2

**Skills:**
- **async-python-patterns** - asyncio, concurrent programming, producer-consumer
- **uv-package-manager** - Modern Python package management (10-100x faster than pip)
- **python-testing-patterns** - pytest, fixtures, mocking, property-based testing

### TypeScript

**Agents:**
- **[typescript-developer](./development/typescript/agents/typescript-developer.md)** - Advanced types, generics, strict type safety

**Skills:**
- **typescript-advanced-types** - Generics, conditional types, mapped types, utility types

### Backend Architecture

**Agents:**
- **[backend-architect](./development/backend/agents/backend-architect.md)** - API design, microservices, event-driven architecture

**Skills:**
- **api-design-principles** - REST/GraphQL design, versioning, pagination

---

## Infrastructure Workflows

DevOps, CI/CD, and deployment automation.

### DevOps

**Agents:**
- **[deployment-engineer](./infrastructure/devops/agents/deployment-engineer.md)** - CI/CD, GitHub Actions, GitOps, container security

**Skills:**
- **github-actions-templates** - Production-ready workflows, matrix builds, Docker, Kubernetes deploy

---

## Web Platform Workflows

Workflows for web development including design review and browser-based automation.

#### [Design Review](./web/design-review/README.md)
UI/UX critique with Playwright browser integration. Accessibility, responsiveness, and visual consistency checks.

---

## Mobile Platform Workflows

Native iOS development with security patterns.

**Agents:**
- **[ios-developer](./mobile/agents/ios-developer.md)** - Swift 6, SwiftUI, UIKit integration, App Store optimization
- **[ios-design-reviewer](./mobile/agents/ios-design-reviewer.md)** - Apple HIG compliance, accessibility review
- **[mobile-security-coder](./mobile/agents/mobile-security-coder.md)** - iOS security (Keychain, biometrics, ATS, WebView security)

**Commands:**
- **/ios-design-review** - Run design review on iOS app

---

## Installation

Copy workflow assets to your Claude directory:

```bash
# Agents
cp -r development/python/agents/* ~/.claude/agents/
cp -r development/typescript/agents/* ~/.claude/agents/
cp -r development/backend/agents/* ~/.claude/agents/
cp -r infrastructure/devops/agents/* ~/.claude/agents/
cp -r mobile/agents/* ~/.claude/agents/

# Skills
cp -r development/python/skills/* ~/.claude/skills/
cp -r development/typescript/skills/* ~/.claude/skills/
cp -r development/backend/skills/* ~/.claude/skills/
cp -r infrastructure/devops/skills/* ~/.claude/skills/

# Commands
cp -r general/code-review/commands/* ~/.claude/commands/
cp -r general/security-review/commands/* ~/.claude/commands/
cp -r mobile/commands/* ~/.claude/commands/
```

## About Skills

Skills are modular knowledge packages following [Anthropic's Agent Skills Specification](https://github.com/anthropics/skills/blob/main/agent_skills_spec.md). They provide deep expertise that activates automatically when Claude detects matching patterns in your requests.

**Progressive disclosure:** Skills load their content on-demand to optimize context usage:
1. **Metadata** (always loaded) - Name and activation criteria
2. **Instructions** (on activation) - Core guidance and patterns
3. **Resources** (on demand) - Examples and templates