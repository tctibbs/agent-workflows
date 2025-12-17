# Documentation Workflow

Agents and skills for creating comprehensive technical documentation, API docs, tutorials, and diagrams.

## Agents

### [docs-architect](./agents/docs-architect.md)

Technical documentation architect for long-form documentation.

- Codebase analysis and architecture documentation
- Executive summaries and deep-dive technical manuals
- Design decision rationale and system overviews
- 10-100+ page comprehensive documentation

**Usage:**
```
@docs-architect Create comprehensive documentation for this microservices architecture
@docs-architect Document the authentication system with rationale for design decisions
```

### [api-documenter](./agents/api-documenter.md)

API documentation specialist for developer experience.

- OpenAPI 3.1+ specification authoring
- Interactive documentation with Swagger/Redoc
- SDK generation and code examples
- Developer portal architecture

**Usage:**
```
@api-documenter Create an OpenAPI 3.1 spec for this REST API
@api-documenter Generate SDK documentation for Python and JavaScript
```

### [tutorial-engineer](./agents/tutorial-engineer.md)

Tutorial engineering for progressive learning experiences.

- Step-by-step tutorials with hands-on exercises
- Progressive skill building and concept decomposition
- Multiple learning styles support
- Quick starts, deep dives, and workshop series

**Usage:**
```
@tutorial-engineer Create a getting started guide for this library
@tutorial-engineer Build a workshop series for learning this framework
```

### [mermaid-expert](./agents/mermaid-expert.md)

Mermaid diagram specialist for visual documentation.

- Flowcharts, sequence diagrams, ERDs
- State diagrams, Gantt charts, architecture diagrams
- Consistent styling and accessibility

**Usage:**
```
@mermaid-expert Create a sequence diagram for this API flow
@mermaid-expert Generate an ERD for these database models
```

## Skills

### architecture-decision-records

Write and maintain ADRs following best practices.

- MADR, Y-statement, and RFC templates
- ADR lifecycle management
- adr-tools automation

### changelog-automation

Automated changelog generation.

- Conventional commits parsing
- Release note generation

### openapi-spec-generation

OpenAPI specification patterns.

- Schema design best practices
- Validation and examples

## Installation

```bash
# Agents
cp -r agents/* ~/.claude/agents/

# Skills
cp -r skills/* ~/.claude/skills/
```
