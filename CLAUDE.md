# xFutebol — Monorepo Overview

Strategic soccer board game. Flutter UI over a Rust game engine, with BLE local multiplayer.

## Repository map

| Repo | Path | Language | Role |
|------|------|----------|------|
| xfutebol-engine | ./xfutebol-engine | Rust | Core game logic, rules, AI, state machine |
| xfutebol-multiplayer | ./xfutebol-multiplayer | Rust | BLE transport, wire protocol, session management |
| xfutebol-app | ./xfutebol-app | Flutter/Dart | Mobile UI, depends on engine via FFI bridge |
| xfutebol_flutter_bridge | ./xfutebol-app/packages/xfutebol_flutter_bridge | Rust + Dart | FFI bridge (flutter_rust_bridge) between app and engine |

## Dependency graph

```
xfutebol-app (Flutter)
  └── xfutebol_flutter_bridge (FFI)
        └── xfutebol-engine (Rust)
  └── xfutebol-multiplayer (Rust, BLE sync)
        └── xfutebol-engine (Rust)
```

## Architectural rules

- **Never duplicate game logic in the app.** All rules, validation, and state transitions live in `xfutebol-engine`.
- The app is a presentation layer only: render state, dispatch actions, handle navigation.
- `xfutebol-multiplayer` handles wire serialization and BLE transport; it never owns game state.
- The flutter bridge (`flutter_rust_bridge`) auto-generates Dart bindings — do not hand-edit generated files under `lib/src/rust/`.

## Tech stack

- Rust 2021 edition (engine + multiplayer + bridge rust side)
- Flutter 3.x / Dart 3.10+ (app + bridge dart side)
- FFI via `flutter_rust_bridge` 2.x
- BLE via `btleplug` 0.11
- Local DB: Isar 3.x
- State management: Provider
- Serialization: Serde + Postcard (binary wire), JSON (debug/logs)
