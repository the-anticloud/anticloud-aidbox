# Students — AIDBOX

**Project:** AIDBOX  
**Category:** MEDICAL_HEALTH  
**Upstream:** https://github.com/HealthSamurai/aidbox-ts-sdk.git  
**Pinned commit:** `c6b1ee79b2b2c8ec1f142e8187831baa626c652a`  
**Assurance:** 16/16 checks passing  
**Ledger head:** `c3cd9588c79339bddd85549f0a6a1382a795261092364468aea3b3ed872837da`  
**Date:** October 2026

## What this project gives you

A complete worked example of offline-first packaging with a cryptographic audit
chain: source pinned at `c6b1ee79b2b2c8ec1f142e8187831baa626c652a`, a 16-check assurance suite, an evidence register
with per-check hashes, and an AIOSS ledger chain ending at `c3cd9588c79339bddd85549f0a6a1382a795261092364468aea3b3ed872837da`.

## Learn by verifying

```
python tools/run_bench.py --out BENCH.json
```

Then take any row from `ISOLATED_LAB_RESULTS/03_Result_Register.md`, recompute
the SHA3-256 of its evidence file, and confirm it matches. If it does not match,
the record has been altered — that is the whole point of the chain.

## Licence

Apache 2.0 terms apply to study and teaching use.
