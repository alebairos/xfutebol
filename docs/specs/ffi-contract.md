# FFI Contract — xfutebol_flutter_bridge

Bridge between `xfutebol-app` (Flutter/Dart) and `xfutebol-engine` (Rust) via `flutter_rust_bridge` 2.x.

## Principles

- The bridge exposes engine state and actions as Dart-callable async functions.
- Generated files under `lib/src/rust/` are **never hand-edited** — regenerate with `flutter_rust_bridge_codegen`.
- The Dart side is a thin pass-through; no game logic lives here.

## Key entry points

<!-- Document public Rust functions exposed via the bridge as they stabilize. -->
<!-- Format: `fn_name(args) -> ReturnType` — brief description -->

| Function | Description |
|----------|-------------|
| _(TBD)_  |             |

## Regenerating bindings

```bash
# From xfutebol-app/packages/xfutebol_flutter_bridge/
flutter_rust_bridge_codegen generate
```

## Known constraints

- All types crossing the FFI boundary must implement `flutter_rust_bridge`'s codec traits.
- Avoid passing raw pointers — use opaque handles or serialized structs.
