# Logging

## Structured Fields (Draft)

| Field | Type | Description |
|-------|------|-------------|
| `iface` | string | Network interface name |
| `sci` | string | Secure Channel Identifier |
| `an` | u8 | Association Number (0-3) |
| `peer_sci` | string | Peer SCI |
| `event` | string | Event type |

*Fields to be finalized during detailed design.*

## Error Classification (Draft)

| Category | Description |
|----------|-------------|
| `config` | Configuration errors |
| `protocol` | MKA protocol errors |
| `system` | System/kernel errors |
| `internal` | Internal errors (should not happen) |

*Categories to be finalized during detailed design.*

## Error Codes

Error codes use string format: `CATEGORY_ERROR_NAME`

Examples:
- `CONFIG_INVALID_CAK`
- `PROTO_INVALID_MKPDU`
- `SYSTEM_NETLINK_FAILED`
- `INTERNAL_UNEXPECTED_STATE`
