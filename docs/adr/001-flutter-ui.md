# ADR 001 — Flutter as the UI layer

**Status:** Accepted

## Context

The game needs a mobile UI targeting iOS and Android. Options considered: Flutter, React Native, pure Rust TUI.

## Decision

Use Flutter 3.x / Dart 3.10+.

## Consequences

- Single codebase for iOS + Android.
- Rust game logic is exposed via FFI (see ADR 002), keeping the UI as a pure presentation layer.
- UI developers work in Dart; engine developers work in Rust — clear boundary.
