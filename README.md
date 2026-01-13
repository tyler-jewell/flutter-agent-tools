# 🚀 agent-browser-flutter

**Seamless AI-Agentic Development for Flutter Web**

[![npm version](https://img.shields.io/npm/v/agent-browser-flutter.svg?style=flat-square)](https://www.npmjs.com/package/agent-browser-flutter)
[![Pub Version](https://img.shields.io/pub/v/flutter_agent_tools?style=flat-square)](https://pub.dev/packages/flutter_agent_tools)
[![License: MIT](https://img.shields.io/badge/license-MIT-blue.svg?style=flat-square)](https://opensource.org/licenses/MIT)
[![Stars](https://img.shields.io/github/stars/tech-swindler/agent-browser-flutter?style=flat-square)](https://github.com/tech-swindler/agent-browser-flutter)

**Turn any Flutter web app into a live, agent-controllable playground.**  
Built as a lightweight plugin for **[agent-browser](https://agent-browser.dev)** (Vercel Labs), this project lets AI coding agents (Cursor, Claude Code, Aider, Open Code, etc.) **see**, **interact**, **edit**, and **control** your Flutter web app in real time — with automatic hot-reload, precise observations, and optional direct tool calling.

No heavy servers. No state-management lock-in. Just drop-in magic for the tightest agentic coding loop on Flutter web.

### 🔥 Why This Changes Everything

- **Continuous Vision**: Real-time accessibility snapshots + streamed layout/logs/jank → agents always "see" the exact current state.
- **Pixel-Perfect Interactions**: Semantic clicks, fills, scrolls, drags — exactly like a human tester.
- **Instant Feedback Loop**: Edit code → auto hot-reload → streamed confirmation within seconds.
- **Optional Superpower**: `flutter_agent_tools` package lets you annotate repos/services → expose CRUD/direct logic as callable tools (seed data, reset state, run hidden ops).
- **Human-in-the-Loop Ready**: `--headed` mode for live monitoring while the agent works.
- **WASM-Ready**: Full support for `--wasm` + skwasm rendering.

Perfect for rapid prototyping, test-driven development, or letting Claude/Cursor build your next Flutter web app **live**.

### 🚀 Quick Start (Under 5 Minutes)

```bash
# 1. Install agent-browser (if not already)
npm install -g agent-browser
agent-browser install

# 2. Install this plugin
npm install -g agent-browser-flutter

# 3. In your Flutter web project
flutter pub add flutter_agent_tools   # Optional: for direct tool calling
agent-browser-flutter bootstrap       # Adds debug entrypoint + examples

# 4. Launch!
agent-browser-flutter run             # Auto-starts Flutter dev server + headed browser
