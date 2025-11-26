# General Workflows

Platform-agnostic workflows that apply to any codebase regardless of language or platform.

## Workflows

### [Security Review](./security-review/README.md)

Lightweight security scanning workflow.

- OWASP-based vulnerability detection
- High-confidence findings with false positive filtering
- Severity classification and remediation guidance
- GitHub Actions for automated security scanning

## Future Additions

- Documentation review workflow
- Refactoring assistant
- Test coverage analysis
- Dependency audit workflow

## Installation

Copy workflow assets to your Gemini directory:

```bash
# For a specific workflow
cp -r security-review/agents/* ~/.gemini/agents/
cp -r security-review/commands/* ~/.gemini/commands/
```