# Light client transparency

```
[ User machine ] --opt-in--> [ Light client: verifies one public profile ]
        |
        v  (SHA-256 hash + signature, never raw data)
[ ADN Network: seals, chains, timestamps ]
        |
        +--> shared freshness for all
        +--> extraction credits to the contributor
```

Packdata Lite, the free light client, can, only when explicitly enabled by the user, verify public professional profiles in the background and return confirmations to the ADN Network — following the participative-app principle (in the manner of Waze — a Google trademark, mentioned to explain, with no affiliation).

What leaves the machine: pseudonymous confirmation signals only. No private data, no customer data, no raw records — only hashes circulate (see WHITEPAPER.md § Privacy by design).

Control: the user can suspend or stop verification at any time from the settings. Packdata acts as data processor (GDPR Art. 28 in the EU, equivalent regimes elsewhere). Nothing is shared to the common network without explicit opt-in.

Sober by design: fragmented 40 KB maximum requests, user-adjustable pace, zero impact on data plan and battery at standard settings.

Segment targeting: the user chooses which segment their client verifies first (e.g. real estate). The network cleans that segment first, so data is already fresh on licence day. Everyone prepares their own ground.

Team plan: each equipped team member contributes to their company's segment freshness. Rollout subject to prior staff information and internal rules — activation stays individual and reversible at any time.

Incentive: each sealed contribution earns extraction credits. Extracting costs more than contributing: rates and caps are shown in the software and may evolve with notice. Contributing opens extraction — the more you refresh, the more you may extract. Signed, timestamped accounting, verifiable by any third party.

The light client contributes at its own pace: it is the gateway to the network. The licence grants full access to the ADN Network: searches, matches and extractions included per plan.

Licences capped at 1,500 per year, with verified B2B registration. The cap guarantees every node is an identified business and keeps the network fast.

## Architecture note

Native Rust light client (memory safety with no GC, strict isolation, minimal footprint), asynchronous multithreaded ingestion engine, real-time peer-to-peer mesh transport with NAT traversal (libp2p, WebRTC): no central server farm, no single point of failure.

Integrity: every contribution is sealed (SHA-256 fingerprint + ECDSA P-256 signature + append-only chaining) and verifiable by any third party holding the public key. A daily chain fingerprint is anchored publicly via OpenTimestamps.

Confidentiality: permanently encrypted transport (TLS 1.3 / DTLS, mandatory in WebRTC). Circulating hashes are pseudonymous, never raw records on the network.

Access: entry gated by signed API keys. Privilege separation: contributing opens no extraction rights beyond earned credits. Source code stays private; the above properties are auditable on request under NDA.

## Continuous verification, human-orchestrated

Packdata Lite runs alone in the background — available on Windows, Mac, iOS, Android and Chrome. Your choice: human, piloted, or accelerated by your own AI agent. In all cases your private meta-search engines cross-check any public observable — pages, APIs and public metrics — in parallel, in seconds and track-free — your device IP is never exposed to sources. Nothing leaves your device without opt-in: only signed hashes join the ADN Network. Every proof is chained, timestamped, third-party verifiable — sealed under the Cerveau Numérique protocol. Your sentinels keep continuous watch, you only review sensitive cases. Non-monetary credits and extraction rights, rates shown in-app, 1500 capped B2B-verified licences per year, possible future token under MiCA with no promise of value. Included in Packdata Lite, native to the software. Our autonomous agents remain R&D.

```
┌─ CLIENT DEVICE — all OS (trust boundary) ────────────┐
│ Windows · Mac · iOS · Android · Chrome               │
│ Lite alone · human / piloted / optional agent        │
│ You: mission, rules, sensitive-case review           │
│ Local agent: your key, filters, adjustable pace      │
│ Raw data: NEVER leaves the device                    │
│ Mobile: light watch (store rules) · Desktop /        │
│ Chrome: full watch                                   │
└───────────────┬──────────────────────────────────────┘
                │ fragmented ≤40 KB requests, TLS 1.3
                │ explicit opt-in, one-click stop
                ▼
┌─ PRIVATE ENGINES (operated by you, track-free) ──────┐
│ Any public observable: pages, APIs, public metrics   │
│ in parallel, in seconds, track-free                  │
│ Seen by sources: engine IP, never device IP          │
│ No request logs, rate-limit + backoff                │
└───────────────┬──────────────────────────────────────┘
                │ candidates: URL + excerpt + observed date
                ▼
┌─ VERIFIER (deterministic, not the LLM) ──────────────┐
│ Cross-check ≥2 concordant sources                    │
│ found → verified: sources + date + traced agent      │
└───────────────┬──────────────────────────────────────┘
                │ verified only
                ▼
┌─ SEALING — Cerveau Numérique (proof, no raw) ────────┐
│ SHA-256 (integrity) + ECDSA P-256 (signature)        │
│ append-only chaining + timestamping (OpenTimestamps) │
│ Hashes + metadata only, pseudonymous                 │
└───────────────┬──────────────────────────────────────┘
                ▼
┌─ ADN NETWORK ────────────────────────────────────────┐
│ Shared memory, mutual freshness                      │
│ Verifiable by any third party holding the public key │
└───────────────┬──────────────────────────────────────┘
                │ permanent watch (versioned rules)
                ▼
┌─ SENTINELS → VALIDATED ──────────────────────────────┐
│ You or confidence threshold (+ Supervisor/Compliance │
│ for sensitive actions). Corrections tighten rules.   │
│ Never infallible.                                    │
└──────────────────────────────────────────────────────┘
```
