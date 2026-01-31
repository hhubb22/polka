# Success Criteria

Minimum viable acceptance criteria for each milestone.

## M1: Lab Baseline

- [ ] netns/veth topology scripts work (`lab/ns-up.sh`, `lab/ns-down.sh`)
- [ ] Static MACsec link established with `ip macsec` commands
- [ ] Encrypted ping succeeds between namespaces
- [ ] Wireshark/tcpdump confirms EtherType 0x88E5

## M2: Southbound v0 (ip wrapper)

- [ ] `macsecctl apply` creates macsec link and configures SA
- [ ] `macsecctl status` outputs structured JSON
- [ ] Idempotent: repeated apply causes no unnecessary changes
- [ ] Keys never appear in logs or error messages

## M3: Southbound v1 (netlink)

- [ ] All operations use netlink directly (no `ip` parsing)
- [ ] Create/delete/update link, TXSA, RXSC, RXSA via netlink
- [ ] Diff engine computes minimal change set
- [ ] Unit tests for netlink encode/decode (no root required)

## M4: Daemon Skeleton

- [ ] `macsecd` starts, loads config, logs sanitized summary
- [ ] Reconcile loop maintains desired state
- [ ] Config reload via SIGHUP without restart
- [ ] Structured logs with `iface`, `sci`, `an` fields
- [ ] Clean shutdown with configurable cleanup policy
