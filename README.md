# One Root: The Session Identity Architecture

**knell** — Paper I of the Session trilogy.

Timestamp of record (archive.org): https://archive.org/details/knell-one-root

An audit of the Session messenger's identity architecture. Every account's master Ed25519 seed is a 16-byte seed padded with 16 zero bytes, and every key in the system is a public, labeled hash-chain derivation from that single 128-bit root. No forward secrecy, no rotation, no revocation — one recovery-phrase compromise is total and retroactive. All claims verified in the shipped clients and libraries; pins and proofs inside.

## Verify

```
gpg --import knell-public.asc
gpg --verify paper1-one-root-session-knell.md.asc
```

Expect: `Good signature from "knell"`, key 133883AB9F6EDE5B9BA6B82E27BEDAF0CE152F25
Fingerprint: 1338 83AB 9F6E DE5B 9BA6 B82E 27BE DAF0 CE15 2F25
