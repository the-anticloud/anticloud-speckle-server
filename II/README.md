# Independent Insurance — SPECKLE_SERVER

**Project:** SPECKLE_SERVER  
**Category:** ARCHITECTURAL_DESIGN  
**Upstream:** https://github.com/specklesystems/speckle-server  
**Pinned commit:** `51d43b91c4681a75bff8b285da7f443a4599da67`  
**Assurance:** 16/16 checks passing  
**Ledger head:** `f4f392e1e42c353ff734c0a21ea9fda955a2429e09bfcbbb21ae28122d877ae5`  
**Date:** October 2026

## Why AI-specific cover matters

Deploying AI in a regulated sector creates liability surfaces that ordinary
technology cover does not reach: inference liability, audit-trail liability,
data-breach liability and IP-infringement liability.

## How this project's architecture reduces insurable risk

| Risk | Cloud AI | SPECKLE_SERVER with AIOSS |
|---|---|---|
| Audit-trail loss | high — vendor-controlled logs | low — append-only chain, verifiable offline |
| Data breach in transit | high — data transits external servers | low — no external endpoint |
| Compliance violation | high — cannot satisfy air-gap requirements | low — structural |
| IP liability | moderate | low — pinned provenance chain |

## Evidence package for an insurer

- AIOSS chain verification for head `f4f392e1e42c353ff734c0a21ea9fda955a2429e09bfcbbb21ae28122d877ae5`
- The 16-check register with per-check evidence hashes
- Framework control mapping in `BENCH.json`

## Contact

lois@0-1.gg
