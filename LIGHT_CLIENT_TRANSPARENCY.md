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

Packdata Lite, the free light client, can, only when explicitly enabled by the user, verify public professional profiles in the background and return confirmations to the ADN Network — the Waze principle applied to B2B data.

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
