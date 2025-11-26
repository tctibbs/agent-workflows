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

### [iOS Design Review](./agents/ios-design-review.md)

iOS design review agent specializing in Apple HIG compliance and accessibility.

- Human Interface Guidelines evaluation
- VoiceOver and Dynamic Type testing
- Multi-device and Dark Mode verification
- Simulator testing via Mobile MCP

**Usage:**
```
@ios-design-review Review the profile settings screen for HIG compliance
```

## Commands

### [iOS Design Review Command](./commands/ios-design-review.md)

Slash command for on-demand iOS design reviews.

```
/ios-design-review
```

## Resources

- [iOS Design Principles](../../context/ios-design-principles.md) - HIG-based design checklist
- [CLAUDE.md Snippet](./CLAUDE-SNIPPET.md) - Project integration for iOS visual checks

## Future Additions

- Android developer agent (Kotlin/Jetpack Compose)
- Flutter developer agent
- React Native developer agent
- Cross-platform testing workflows

## Installation

Copy agents and commands to your Claude directory:

```bash
cp -r agents/* ~/.claude/agents/
cp -r commands/* ~/.claude/commands/
```
