# Educators — AIDBOX

**Project:** AIDBOX  
**Category:** MEDICAL_HEALTH  
**Upstream:** https://github.com/HealthSamurai/aidbox-ts-sdk.git  
**Pinned commit:** `c6b1ee79b2b2c8ec1f142e8187831baa626c652a`  
**Assurance:** 16/16 checks passing  
**Ledger head:** `c3cd9588c79339bddd85549f0a6a1382a795261092364468aea3b3ed872837da`  
**Date:** October 2026

## Teaching with AIDBOX

The project is usable as a worked example of offline-first packaging with a
cryptographic audit chain. It ships with the assurance suite, the evidence
register and the ledger, so students can verify claims rather than take them on
faith.

## Suggested exercises

1. Run `python tools/run_bench.py --out BENCH.json` and read the 16 results.
2. Recompute the SHA3-256 of a row's evidence file and compare to the register.
3. Walk the AIOSS chain from genesis to head `c3cd9588c79339bddd85549f0a6a1382a795261092364468aea3b3ed872837da` and confirm every link.
4. Break one artifact and observe the chain fail to verify.

## Licence for teaching

Apache 2.0 terms apply to academic and teaching use. See `24_ANTICOMMONS_LICENSE`.
