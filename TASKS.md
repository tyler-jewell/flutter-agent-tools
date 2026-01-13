# ✅ TASKS.md

Detailed, prioritized task list for full development and deployment. Grouped by phase with checkboxes.

## Phase 1: Repository Setup
- [ ] Create public GitHub repo `tech-swindler/agent-browser-flutter` (monorepo structure)
- [ ] Add LICENSE (MIT)
- [ ] Setup GitHub Actions CI:
  - Lint/test on push
  - Matrix: macOS/Linux/Windows
  - Auto-publish to npm (on tag) + pub.dev
- [ ] Add Husky pre-commit hooks
- [ ] Write initial README.md, ROADMAP.md, TASKS.md
- [ ] Add .gitignore (Dart + Node)

## Phase 2: Core Plugin (agent-browser-flutter npm package)
- [ ] Scaffold npm package (bin, skills dir)
- [ ] Implement CLI wrapper:
  - `agent-browser-flutter run` → auto-start `flutter run -d web-server --wasm`
  - `agent-browser-flutter session --url <port> --headed`
  - `agent-browser-flutter bootstrap` → add dependency + debug main
- [ ] Custom skills:
  - Enhanced snapshot (Flutter semantics)
  - Streaming hooks (logs, network, jank, layout diffs via MutationObserver)
  - Reset session command
- [ ] Auto-detect Flutter dev server port
- [ ] Post-install script: check Flutter in PATH, suggest fixes

## Phase 3: flutter_agent_tools (pub.dev package)
- [ ] Scaffold Dart package
- [ ] Define annotations (@AgentRepo, @ExposeTool)
- [ ] Build code generator (source_gen/build_runner):
  - Scan for annotated classes/methods
  - Generate registry + manifest
  - Auto-CRUD detection
- [ ] JS interop bridge (dart:js_interop):
  - Init in debug mode only
  - Expose window.flutterAgent.call/toolList
  - JSON param serialization + Zod validation in plugin
- [ ] Security: Disable in release builds
- [ ] Example repo class in package

## Phase 4: Boilerplate & Docs
- [ ] Create minimal Flutter web template
  - Semantic labels best practices
  - Example annotated repo
  - main.debug.dart with bridge init
- [ ] Integration guides:
  - Cursor/Claude/Aider prompts
  - Common workflows
- [ ] SKILL.md for agent-browser skill format

## Phase 5: Testing (Implement All Functional Requirements)
### Setup & Installation
- [ ] SETUP-01 to SETUP-04 (automated scripts + manual)

### Observation & Streaming
- [ ] OBS-01 to OBS-04 (WS monitoring scripts)

### Interactions
- [ ] INT-01 to INT-03 (e2e command sequences)

### Code Editing & Hot Reload
- [ ] CODE-01 to CODE-03 (file watcher + error induction)

### Session Management & Reset/Seeding
- [ ] SESS-01 to SESS-04

### Tool Exposure
- [ ] TOOL-01 to TOOL-04 (manifest checks + release build test)

### Reliability & Edge Cases
- [ ] REL-01 to REL-04 (Chrome traces + error scenarios)

- [ ] Add GitHub Actions for automated subset
- [ ] Manual test checklist in docs

## Phase 6: Deployment & Launch
- [ ] Publish v0.1.0 to npm (core plugin)
- [ ] Publish flutter_agent_tools to pub.dev
- [ ] Announce on X (@tech_swindler), Reddit, Flutter community
- [ ] Add badges to README
- [ ] Create demo video (headed session with agent)

Total estimated: 4–6 weeks for MVP (v0.1–0.2).
