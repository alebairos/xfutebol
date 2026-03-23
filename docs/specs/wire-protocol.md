# Wire Protocol

Binary serialization format used between `xfutebol-multiplayer` and `xfutebol-app` over BLE.

## Encoding

- **Production:** Postcard (binary, `serde` + `postcard` crate)
- **Debug/logs:** JSON (`serde_json`)

## Message envelope

<!-- Define the top-level message wrapper as it stabilizes. -->

```
[msg_type: u8][payload_len: u16][payload: [u8; payload_len]]
```

## Message types

| ID | Name | Direction | Description |
|----|------|-----------|-------------|
| _(TBD)_ | | |

## Versioning

- Protocol version is exchanged during BLE session handshake.
- Breaking changes require a version bump; old versions must be rejected explicitly.

## Constraints

- Max payload size: _(TBD — BLE MTU minus envelope overhead)_
- `xfutebol-multiplayer` owns serialization/deserialization; the app never parses raw bytes.
