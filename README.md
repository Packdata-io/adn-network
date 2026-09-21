# ADN Network — Proof-of-Existence Anchor v1.0

**Date of publication:** 2026-09-13
**Owner of the sealed works:** Samy Benhellal Hugon (source code property retained)
**Licensed operator:** PACKDATA LTD (London, UK — Company No. 17445728), exploitation licence
**Conceived and authored by:** Samy Benhellal Hugon
**Status:** design anchor + hash manifest. **No source code is published in this repository.**

This repository publicly timestamps the conception of the **ADN Network** protocol —
a peer-to-peer B2B data network in which a free light client (*Packdata Lite*)
validates and refreshes public professional records in the background
(data that refreshes as you use it).
Full product description: [White Paper](https://packdata.io/white-paper.html)
([WHITEPAPER.md](WHITEPAPER.md) snapshot in this repo).

## 1. Protocol specification (technical thesis)

### 1.1 Roles
- **Licensed business** — uses *Packdata Lite* (free) + *Packdata Desktop* (ADN Network
  licence) to prospect and contact decision-makers on fresh data. Usage itself
  refreshes the network.
- **Company employees** — run the free light client (PC/Mac/iOS/Android/Chrome);
  their machines feed the network with updates and earn ADN / extraction credits.
- **Individual contributor** — the light client **randomly** queries public data to
  confirm or refresh it in the ADN Network. Every contribution is **signed and
  timestamped** and earns extraction rights / credits (usable from year 2).

### 1.2 Contribution flow (proof of contribution)
1. **Contribute** — a contributor confirms or refreshes one public professional record.
2. **Seal** — the contribution is sealed: **SHA-256** fingerprint (integrity) +
   **ECDSA P-256** signature (verifiable by any third party with the public key) +
   **chaining** (each block points to the previous one, append-only).
3. **Reward** — sealed contributions open **extraction rights**: the more you
   contribute to freshness, the more you may extract.
   Credits are non-monetary contribution units. Any exchangeable token is
   under study and would be legally regulated (MiCA) before any launch —
   no promise of value or return.
4. **Cycle** — the more active the network, the fresher the data for everyone.

### 1.3 Privacy by design
Only **fingerprints (hashes)** circulate on the chain — **never raw data**.
User queries and user data never leave the user's machine.

### 1.4 Decision protocol ("Cerveau Numérique")
Local-first compiled software, native streaming P2P network, no central cloud,
no single point of failure.
**Rule 1:** what can run alone, runs alone.
**Rule 2:** what engages liability requires a signature.
Every version is logged, verifiable and reversible.
Roadmap: a daily fingerprint of the chain anchored publicly via **OpenTimestamps**.

### 1.5 Vision — AI agents (R&D stealth — under study, non-operational)
Future direction: verified feeds as a trust layer for autonomous AI agents
(anti-hallucination). Status follows reality: moved to operational only
when proven.

## 2. Hash manifest (proof the secret code exists)

`MANIFEST.sha256` lists the **SHA-256 fingerprints** of the proprietary source files
(matching/aggregation engine + native app client) **as they existed on 2026-09-13**.
The code itself stays 100% private. Scope and reproduction rules are documented
in the manifest header.

**Verification procedure** (for a court-appointed expert):
1. Samy Benhellal Hugon discloses the secret source file under seal.
2. The expert computes `SHA-256(file)`.
3. If it matches the fingerprint published here on 2026-09-13, it is proven that
   Samy Benhellal Hugon possessed and authored that exact file on that date.

## 3. Licence

The sealed works are © 2026 Samy Benhellal Hugon, exploited under licence by
PACKDATA LTD (see [LICENSE](LICENSE)). Reading is allowed; any copy, modification,
commercial use or reverse-engineering is prohibited without written licence
from the author.

## 4. Evidentiary note

GitHub server-side push history provides public, third-party-dated corroboration
of anteriority. For maximum enforceability under French/EU law, this publication
is complemented by a sealed deposit (*enveloppe Soleau* / bailiff record).

Registered e-Soleau deposit: INPI No. **DSO2026033766** dated 2026-09-13
(5-year conservation, sealed files).
