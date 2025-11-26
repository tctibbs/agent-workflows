## iOS Visual Development

### Design Principles
- iOS design checklist in `/context/ios-design-principles.md`
- Brand style guide in `/context/style-guide.md`
- When making iOS UI changes, always refer to Apple Human Interface Guidelines

### Quick iOS Visual Check

IMMEDIATELY after implementing any iOS UI change:

1. **Identify what changed** - Review modified SwiftUI views or UIKit controllers
2. **List simulators** - Use `mcp__mobile-mcp__list_devices` to find available devices
3. **Boot simulator** - Use `mcp__mobile-mcp__boot_device` with iPhone 15 Pro
4. **Launch app** - Use `mcp__mobile-mcp__launch_app` with your app's bundle ID
5. **Navigate to changed screens** - Use `tap`, `swipe` to reach affected views
6. **Verify HIG compliance** - Compare against `/context/ios-design-principles.md`
7. **Check accessibility** - Use `mcp__mobile-mcp__get_ui_tree` to verify VoiceOver labels
8. **Capture screenshots** - Use `mcp__mobile-mcp__take_screenshot` for each changed view
9. **Test Dark Mode** - Change appearance in Settings and verify colors

This verification ensures changes meet Apple HIG standards and accessibility requirements.

### Multi-Device Testing

For significant iOS UI changes, test across device sizes:
- **iPhone SE (3rd gen)**: Smallest viewport, tests layout constraints
- **iPhone 15 Pro**: Standard size, primary development target
- **iPhone 15 Pro Max**: Largest iPhone, tests scaling
- **iPad Pro 11"**: If app supports iPad, tests size classes

### Accessibility Verification

Before finalizing iOS UI changes:
- **VoiceOver**: All interactive elements have `.accessibilityLabel`
- **Dynamic Type**: Layout handles `.accessibility1` through `.accessibility5` sizes
- **Touch targets**: Minimum 44x44pt (use `.frame(minWidth: 44, minHeight: 44)`)
- **Color contrast**: 4.5:1 ratio minimum for text
- **Reduce Motion**: Animations respect `UIAccessibility.isReduceMotionEnabled`

### Comprehensive iOS Design Review

Invoke the `@ios-design-review` subagent for thorough design validation when:
- Completing significant UI features
- Before finalizing PRs with visual changes
- Needing comprehensive HIG and accessibility testing
- Adding new screens or navigation flows
