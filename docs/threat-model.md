# Threat Model

## Key Management

- Keys (CAK, SAK) are held in memory only; never written to disk
- Keys are zeroized on process termination or when no longer needed (e.g., after SA expiration)

## Logging

- Logs must not contain key material, CAK names, or other secrets
- SCI and MAC addresses may be logged for debugging

## Least Privilege

- Process runs without root where possible
- Only required capabilities are requested (e.g., `CAP_NET_ADMIN` on Linux)
- No unnecessary file system or network access

## Crash Dumps

- Core dumps are disabled by default to prevent key leakage
- If enabled for debugging, dumps must be stored securely and deleted after analysis
