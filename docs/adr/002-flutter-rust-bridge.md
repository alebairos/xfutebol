# ADR 002 — flutter_rust_bridge for FFI

**Status:** Accepted

## Context

The Flutter app needs to call into the Rust engine. Options: raw FFI, dart:ffi manually, flutter_rust_bridge.

## Decision

Use `flutter_rust_bridge` 2.x. It auto-generates Dart bindings from annotated Rust functions.

## Consequences

- Generated files under `lib/src/rust/` must never be hand-edited.
- Adding a new engine API requires: annotate in Rust → run codegen → commit generated files.
- Type safety across the FFI boundary is enforced by the generator.
