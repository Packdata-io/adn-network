# Network shield — protocol meets the field

**Date:** 2026-10-06

## 1. What the protocol establishes

The application runs locally on the user's terminal. Only signed fingerprints
join the network, never raw data. Verification requests are fragmented
(≤ 40 KB) at a user-adjustable pace. There is no central collection server:
verification traffic originates from the contributors' own terminals.

## 2. What networks contribute

On fixed and mobile access alike, operators pool hundreds of subscribers
behind a single public address, reassigned frequently. A micro-request therefore
blends into ordinary traffic. Measurable consequence: blocking these addresses
at scale causes massive collateral damage (legitimate subscribers cut off),
which makes IP-based blocking costly and impractical as a primary method —
without making it impossible.

## 3. Synergy, with no absolutes

| Protocol | Network | Effect |
|---|---|---|
| ≤ 40 KB requests at adjustable pace | Lightweight traffic indistinguishable from normal browsing | Behavioral detection made difficult, not ruled out |
| No personal IP or identifier exposed | Shared, rotating public addresses | IP blocking impractical at scale, not impossible |
| Fingerprints only, data never leaves | Encrypted transport | Interception unusable; reduced legal surface (public data, consent, traceability), never total |
| No central collection server | Distributed terminals | No single point to block; initial bootstrapping and software updates remain the only admitted centralized points |

© 2026 — reading allowed; any copy, modification or commercial use requires
the author's written permission.
