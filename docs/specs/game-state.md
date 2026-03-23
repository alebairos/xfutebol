# Game State Schema

The canonical state produced by `xfutebol-engine`, consumed by both the bridge (FFI) and multiplayer (BLE sync).

## Principles

- `xfutebol-engine` is the single source of truth — state is never mutated outside it.
- State is passed across boundaries by value (serialized), never by shared reference.

## Top-level structure

<!-- Fill in as the engine's public API stabilizes. -->

```rust
// xfutebol-engine — sketch, not final
pub struct GameState {
    pub board: Board,
    pub turn: Turn,
    pub score: Score,
    pub phase: GamePhase,
}
```

## Board

- 8×8 grid (see `docs/manual.md` for board rules)
- Each cell may hold a piece, be empty, or be a special area (goal, penalty, etc.)

## State transitions

All transitions go through the engine's action dispatcher. Valid actions:

| Action | Description |
|--------|-------------|
| _(TBD)_ | |

## Serialization

- FFI boundary: encoded via `flutter_rust_bridge` codec (auto-generated).
- BLE boundary: Postcard binary (see `wire-protocol.md`).
