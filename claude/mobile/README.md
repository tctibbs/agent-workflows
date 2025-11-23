# Mobile Platform Workflows

Workflows and agents for mobile application development across iOS and Android platforms.

## MCP Dependencies

- [Mobile MCP](../../mcp/mobile-mcp.md) - Mobile device automation for simulator/emulator testing

## Agents

### [iOS Developer](./agents/ios-developer.md)

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

## Future Additions

- Android developer agent (Kotlin/Jetpack Compose)
- Flutter developer agent
- React Native developer agent
- Cross-platform testing workflows

## Installation

Copy agents to your Claude directory:

```bash
cp -r agents/* ~/.claude/agents/
```
