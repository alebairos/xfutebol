# Agent & Claude Code Workflow

How to work with Claude Code across this monorepo.

## How context propagation works

Claude Code reads `CLAUDE.md` by walking up the directory tree from wherever it is invoked. This means every per-repo session automatically inherits the workspace rules:

```
xfutebol/CLAUDE.md               ← always in context (architecture, cross-repo rules)
xfutebol-engine/CLAUDE.md        ← also in context when invoked from engine
```

No configuration needed — just invoke from the right directory.

## Default: per-repo sessions

Start Claude from inside the repo you are working on.

```bash
cd xfutebol-engine && claude
cd xfutebol-app && claude
cd xfutebol-multiplayer && claude
```

| Task | Invoke from |
|------|-------------|
| Engine logic, rules, AI, state machine | `xfutebol-engine/` |
| Flutter UI, navigation, rendering | `xfutebol-app/` |
| BLE transport, wire protocol | `xfutebol-multiplayer/` |
| FFI bridge changes | `xfutebol-app/` (bridge lives under `packages/`) |

Per-repo sessions have focused file access and don't burn context on unrelated code.

## Cross-repo sessions

Invoke from the workspace root when the task genuinely spans multiple repos.

```bash
cd xfutebol && claude
```

Use this for:
- Designing a new engine API that also changes the FFI bridge and the app
- Debugging an issue that crosses the BLE transport and the app layer
- Updating a spec in `docs/specs/` alongside its implementation

## Pulling in sibling context on demand

Even in a per-repo session you can reference a file from a sibling repo:

```
@../xfutebol-engine/src/state.rs
```

Use this when you need a single file for reference without opening a full workspace session.

## Adding a new repo

1. Create the repo under `xfutebol/`.
2. Add a `CLAUDE.md` inside it with repo-specific rules.
3. Update the repository map and dependency graph in `xfutebol/CLAUDE.md`.
4. Add relevant specs under `docs/specs/` if the repo introduces a new cross-repo boundary.
