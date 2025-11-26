# iOS Design Principles

Design checklist based on Apple Human Interface Guidelines for iOS applications.

## Core Principles

### Clarity
- [ ] Text is legible at all sizes
- [ ] Icons are clear and recognizable (SF Symbols preferred)
- [ ] UI elements are purposeful and unambiguous
- [ ] Adequate spacing between elements

### Deference
- [ ] Content is prioritized over chrome
- [ ] UI doesn't compete with content
- [ ] Minimal use of bezels, gradients, and drop shadows
- [ ] Full-screen layouts utilize available space

### Depth
- [ ] Layering conveys hierarchy and position
- [ ] Translucency provides context
- [ ] Motion reinforces relationships between elements

## Typography & Dynamic Type

- [ ] SF Pro or system fonts used appropriately
- [ ] All text supports Dynamic Type
- [ ] Accessibility text sizes supported (AX1-AX5)
- [ ] Text truncation handled gracefully with ellipsis
- [ ] Line heights and letter spacing follow HIG
- [ ] Text remains readable at all supported sizes

## Layout & Safe Areas

- [ ] Content respects safe area insets
- [ ] Notch/Dynamic Island area handled correctly
- [ ] Home indicator area respected
- [ ] Landscape orientation supported (if applicable)
- [ ] iPad size classes handled properly
- [ ] Split View and Slide Over supported (iPad)
- [ ] Keyboard avoidance implemented for text fields

## Navigation

- [ ] Standard navigation patterns used (push, modal, tab)
- [ ] Back swipe gesture works correctly
- [ ] Navigation bar styling is consistent
- [ ] Tab bar has 5 or fewer items
- [ ] Tab bar icons use SF Symbols
- [ ] Modal presentation styles appropriate to content
- [ ] Search bar placement follows conventions

## Color & Appearance

- [ ] Light and Dark Mode fully supported
- [ ] System semantic colors used (label, secondaryLabel, etc.)
- [ ] 4.5:1 contrast ratio for normal text
- [ ] 3:1 contrast ratio for large text
- [ ] Tint color is consistent throughout app
- [ ] Colors adapt to Increase Contrast setting
- [ ] No color-only indicators (include icons/text)

## Accessibility

### VoiceOver
- [ ] All interactive elements have accessibility labels
- [ ] Accessibility hints for non-obvious actions
- [ ] Accessibility traits set correctly (button, header, etc.)
- [ ] Custom actions for complex controls
- [ ] Logical reading order

### Other Accessibility Features
- [ ] Reduce Motion respected (disable animations)
- [ ] Bold Text supported
- [ ] Increase Contrast supported
- [ ] 44x44pt minimum touch targets
- [ ] Focus states visible for keyboard navigation
- [ ] No time-dependent interactions without alternatives

## Components & Patterns

### Standard Components
- [ ] UIKit/SwiftUI standard components used when possible
- [ ] Custom components follow platform conventions
- [ ] Consistent component styling throughout app

### SF Symbols
- [ ] SF Symbols used for system actions
- [ ] Proper symbol configuration (weight, scale)
- [ ] Symbols align with text properly
- [ ] Multicolor symbols used appropriately

### Feedback
- [ ] Haptic feedback for meaningful interactions
- [ ] Visual feedback for all touch interactions
- [ ] Loading indicators for async operations
- [ ] Error states clearly communicated
- [ ] Success confirmations where appropriate

### Context Menus & Actions
- [ ] Context menus for relevant items (long press)
- [ ] Swipe actions for list items where appropriate
- [ ] Action sheets for destructive actions
- [ ] Alerts used sparingly and appropriately

## Performance & Responsiveness

- [ ] 60fps scrolling maintained
- [ ] Immediate touch response (no perceptible delay)
- [ ] Skeleton screens for content loading
- [ ] Progressive loading for large content
- [ ] Smooth animations (when Reduce Motion is off)
- [ ] No dropped frames during transitions

## Device-Specific Considerations

### iPhone
- [ ] Works on smallest iPhone (SE)
- [ ] Scales appropriately to largest iPhone (Pro Max)
- [ ] Reachability considered for one-handed use

### iPad
- [ ] Optimized for larger screen (not just scaled up)
- [ ] Pointer/trackpad support
- [ ] Keyboard shortcuts for common actions
- [ ] Sidebar navigation for master-detail

## Review Checklist Summary

### Critical (Must Fix)
- Accessibility blockers (no VoiceOver labels)
- Safe area violations
- Dark Mode crashes or invisible content
- Touch targets under 44x44pt

### Important (Should Fix)
- Dynamic Type not fully supported
- Inconsistent navigation patterns
- Missing haptic feedback
- Color contrast issues

### Minor (Nice to Fix)
- SF Symbols not optimally configured
- Animation polish
- Keyboard shortcut additions
- Minor spacing adjustments
