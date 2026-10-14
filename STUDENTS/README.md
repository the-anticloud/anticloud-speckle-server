# Students — SPECKLE_SERVER

**Project:** SPECKLE_SERVER  
**Category:** ARCHITECTURAL_DESIGN  
**Upstream:** https://github.com/specklesystems/speckle-server  
**Pinned commit:** `51d43b91c4681a75bff8b285da7f443a4599da67`  
**Assurance:** 16/16 checks passing  
**Ledger head:** `f4f392e1e42c353ff734c0a21ea9fda955a2429e09bfcbbb21ae28122d877ae5`  
**Date:** October 2026

## What this project gives you

A complete worked example of offline-first packaging with a cryptographic audit
chain: source pinned at `51d43b91c4681a75bff8b285da7f443a4599da67`, a 16-check assurance suite, an evidence register
with per-check hashes, and an AIOSS ledger chain ending at `f4f392e1e42c353ff734c0a21ea9fda955a2429e09bfcbbb21ae28122d877ae5`.

## Learn by verifying

```
python tools/run_bench.py --out BENCH.json
```

Then take any row from `ISOLATED_LAB_RESULTS/03_Result_Register.md`, recompute
the SHA3-256 of its evidence file, and confirm it matches. If it does not match,
the record has been altered — that is the whole point of the chain.

## Licence

Apache 2.0 terms apply to study and teaching use.
