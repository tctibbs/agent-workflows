# Claude Workflows

This directory contains reusable agentic workflow packs for Claude Code, organized by platform.

## General Workflows

Platform-agnostic workflows that apply to any codebase regardless of language or platform.

### Workflows

#### [Code Review](./general/code-review/README.md)

Architecture-informed code review workflow.

- Comprehensive code quality feedback
- Readability, maintainability, and performance analysis
- GitHub Actions for automated PR reviews
- Customizable review criteria

#### [Security Review](./general/security-review/README.md)

Lightweight security scanning workflow.

- OWASP-based vulnerability detection
- High-confidence findings with false positive filtering
- Severity classification and remediation guidance
- GitHub Actions for automated security scanning

### Installation

Copy workflow assets to your Claude directory:

```bash
# For a specific workflow
cp -r code-review/agents/* ~/.claude/agents/
cp -r code-review/commands/* ~/.claude/commands/

# For GitHub Actions
cp code-review/actions/*.yml your-project/.github/workflows/
```

## Web Platform Workflows

Workflows and agents for web development, including design review, accessibility testing, and browser-based automation.

### Workflows

#### [Design Review](./web/design-review/README.md)

Automated UI/UX and front-end design critique workflow.

- Structured design feedback based on industry standards
- Live browser testing with Playwright integration
- Accessibility, responsiveness, and visual consistency checks
- CLAUDE.md snippet for project integration

## Mobile Platform Workflows

Workflows and agents for mobile application development across iOS and Android platforms.

### Agents

#### [iOS Developer](./mobile/agents/ios-developer.md)

Expert iOS development agent for Swift/SwiftUI projects.

- Swift 6 with strict concurrency and type safety
- SwiftUI-first UI with UIKit integration
- Apple ecosystem integration (iOS, watchOS, macOS)
- App Store guidelines compliance and optimization
- MVVM, Clean Architecture, and Coordinator patterns

**Usage:**
```
@ios-developer Help me implement Core Data with CloudKit sync
@ios-developer Create a custom SwiftUI component with accessibility support
@ios-developer Set up Xcode Cloud CI/CD pipeline
```

### Installation

Copy agents to your Claude directory:

```bash
cp -r agents/* ~/.claude/agents/
```