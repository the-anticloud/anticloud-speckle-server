# Ethics — SPECKLE_SERVER

**Project:** SPECKLE_SERVER  
**Category:** ARCHITECTURAL_DESIGN  
**Upstream:** https://github.com/specklesystems/speckle-server  
**Pinned commit:** `51d43b91c4681a75bff8b285da7f443a4599da67`  
**Assurance:** 16/16 checks passing  
**Ledger head:** `f4f392e1e42c353ff734c0a21ea9fda955a2429e09bfcbbb21ae28122d877ae5`  
**Date:** October 2026

## Position

SPECKLE_SERVER is packaged for offline deployment with a verifiable audit trail. The
ethical questions this raises are answered by making the system's behaviour
checkable rather than by policy statements.

## The four commitments

1. **No hidden egress.** The deployment has no external API dependency; this is
   testable by running it with the network disconnected.
2. **Attributable output.** Every artifact is recorded in a hash chain, so what
   the system produced can be reconstructed.
3. **Operator control.** The institution owns the hardware and the keys.
4. **Refusal to overclaim.** Where a certification is not held, the project says
   so rather than implying it.

## Dual use

This project is packaged for civilian and public-sector deployment. Where an
upstream has dual-use characteristics, the licence gate and the reference-only
marking in `BENCH.json` record that.
