# Configuration Specification

## Format

TOML

## Schema

```toml
[[interface]]
name = "eth0"
policy = "encrypt"  # encrypt | integrity-only | bypass

[interface.key]
ckn = "0123456789abcdef"  # CAK Name (hex string)
cak = "0123456789abcdef0123456789abcdef"  # CAK (hex string)

[interface.rekey]
interval = 3600  # seconds, 0 = no automatic rekey
```

## Fields

| Field | Required | Description |
|-------|----------|-------------|
| `interface.name` | yes | Network interface name |
| `interface.policy` | yes | MACsec policy |
| `interface.key.ckn` | yes | CAK Name (hex) |
| `interface.key.cak` | yes | Connectivity Association Key (hex) |
| `interface.rekey.interval` | no | Rekey interval in seconds (default: 0) |

## Example

```toml
[[interface]]
name = "eth0"
policy = "encrypt"

[interface.key]
ckn = "0102030405060708"
cak = "0123456789abcdef0123456789abcdef"

[interface.rekey]
interval = 3600
```

## Notes

- CAK is stored in plaintext in config file (v1 limitation)
- Config file should have restricted permissions (0600)
