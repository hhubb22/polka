# ADR 001: Tech Stack

## Status

Accepted

## Context

Selecting the foundational technology choices for the MACsec control plane implementation.

## Decision

- **Language**: Rust - memory safety is critical for a cryptographic protocol implementation
- **Netlink library**: `neli` - lightweight, pure Rust, minimal dependencies
- **Test framework**: Built-in (`#[test]`, `cargo test`)
- **Packaging**: Static binary (musl) for initial release

## Consequences

- Rust's ownership model helps prevent key leakage and memory corruption
- `neli` keeps the dependency tree small while avoiding raw netlink boilerplate
- Static binary simplifies deployment across Linux distributions
