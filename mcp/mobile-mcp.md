# Mobile MCP

Mobile device automation server for interacting with iOS and Android devices.

**Repository:** [mobile-next/mobile-mcp](https://github.com/mobile-next/mobile-mcp)

## Capabilities

- Control iOS simulators and Android emulators
- Interact with real devices
- Tap, swipe, scroll, and gesture controls
- Capture screenshots and device state
- Launch and interact with mobile apps
- Access device logs and performance metrics

## Used By

- [Mobile](../claude/mobile/README.md) - iOS developer agent and future mobile workflows

## Setup

### Why WebDriverAgent?

mobile-mcp needs WebDriverAgent (WDA) to fully control iOS simulators (tap, swipe, read UI tree). WDA is not included with Xcode, so you must:

1. Get a maintained WDA fork (Appium's)
2. Install its dependencies
3. Build & run it on your target simulator

Once WDA is running, mobile-mcp can talk to it via port 8100 and stop falling back to simctl.

### Prerequisites (one-time per Mac)

```bash
# Xcode CLT
xcode-select --install

# Carthage (needed by WDA; Apple Silicon fix)
brew install carthage
sudo mkdir -p /usr/local/bin
sudo ln -s /opt/homebrew/bin/carthage /usr/local/bin/carthage
```

Make sure you have Node 18+ and Xcode installed.

### Clone WebDriverAgent

```bash
cd ~/Code  # or wherever you keep projects
git clone --depth 1 https://github.com/appium/WebDriverAgent.git
cd WebDriverAgent
```

Use Appium's fork, not the archived Facebook one.

### Bootstrap WDA Dependencies

```bash
./Scripts/bootstrap.sh
```

This pulls Carthage frameworks + Inspector dependencies.

### Build & Start WDA on Simulator

Boot your desired simulator (e.g., iPhone 16 Pro) in Simulator.app, then:

```bash
xcodebuild \
  -project WebDriverAgent.xcodeproj \
  -scheme WebDriverAgentRunner \
  -destination "platform=iOS Simulator,name=iPhone 16 Pro" \
  test
```

This compiles WDA, installs the test bundle into that simulator, and starts the WDA HTTP server on `127.0.0.1:8100`.

**Verify it's running:**

```bash
curl http://127.0.0.1:8100/status
# should return JSON
```

### Run mobile-mcp

Let your MCP client launch it, or run manually:

```bash
npx -y @mobilenext/mobile-mcp@latest
```

For Claude Code:

```bash
claude mcp add mobile-mcp -- npx -y @mobilenext/mobile-mcp@latest
```

Now when you ask the agent to use mobile-mcp (list devices, take screenshot, tap UI, etc.), it will use WDA instead of just simctl.

## Full Documentation

For complete setup instructions, Android support, and API reference, see the official repository:

[mobile-next/mobile-mcp](https://github.com/mobile-next/mobile-mcp)
