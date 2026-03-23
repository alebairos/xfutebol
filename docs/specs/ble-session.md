# BLE Session — Transport & Pairing

Managed by `xfutebol-multiplayer` via `btleplug` 0.11.

## Session lifecycle

```
[Scan] → [Advertise/Discover] → [Connect] → [Handshake] → [In-game sync] → [Disconnect]
```

## Roles

- **Host:** advertises, owns the canonical game state (sourced from `xfutebol-engine`).
- **Guest:** discovers, connects, receives state diffs, sends actions.

## BLE characteristics

| UUID | Name | Properties | Description |
|------|------|------------|-------------|
| _(TBD)_ | game-state | Notify | Host pushes state diffs |
| _(TBD)_ | player-action | Write | Guest sends actions |
| _(TBD)_ | handshake | Read/Write | Protocol version + session token |

## Handshake sequence

1. Guest connects and reads `handshake` characteristic.
2. Host responds with protocol version + session token.
3. Guest writes back acknowledgement.
4. Host begins pushing state via `game-state` notifications.

## Error handling

- Connection loss: guest attempts reconnect up to 3 times before surfacing error to app.
- Protocol version mismatch: connection refused, user shown "update required" message.

## Constraints

- `xfutebol-multiplayer` never owns game state — it only transports diffs produced by the engine.
- The app layer treats BLE events as opaque; all interpretation happens in the multiplayer crate.
