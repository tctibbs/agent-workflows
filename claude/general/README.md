# General Workflows

Platform-agnostic workflows that apply to any codebase regardless of language or platform.

## Workflows

### [Code Review](./code-review/README.md)

Architecture-informed code review workflow.

- Comprehensive code quality feedback
- Readability, maintainability, and performance analysis
- GitHub Actions for automated PR reviews
- Customizable review criteria

### [Security Review](./security-review/README.md)

Lightweight security scanning workflow.

- OWASP-based vulnerability detection
- High-confidence findings with false positive filtering
- Severity classification and remediation guidance
- GitHub Actions for automated security scanning

## Installation

Copy workflow assets to your Claude directory:

```bash
# For a specific workflow
cp -r code-review/agents/* ~/.claude/agents/
cp -r code-review/commands/* ~/.claude/commands/

# For GitHub Actions
cp code-review/actions/*.yml your-project/.github/workflows/
```
