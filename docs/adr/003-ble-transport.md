# ADR 003 — BLE for local multiplayer transport

**Status:** Accepted

## Context

Two players on the same physical table need a low-latency, no-internet connection for local multiplayer.

## Decision

Use Bluetooth Low Energy (BLE) via `btleplug` 0.11 in the `xfutebol-multiplayer` crate.

## Consequences

- No server infrastructure needed for local play.
- `xfutebol-multiplayer` owns all BLE and wire-protocol logic; it never owns game state.
- Game state diffs are serialized with Postcard (see `wire-protocol.md`).
- iOS and Android BLE permissions must be declared in the Flutter app manifest.
