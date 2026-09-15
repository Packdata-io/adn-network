# Positioning — living B2B data over P2P (2026-09-14)

ADN Network is living B2B data over P2P. Principle: every use
(search, export, send) re-checks the touched data against its
public sources and re-seals the observation — the database
refreshes while you use it, no batches, no frozen snapshots.
Architecture: no single point of failure — data lives on the
network, not on a central server.

Proof: each update is a timestamped, chained certificate (see
CERTIFICATE_EXAMPLE.md); the certificate chain makes the history,
up or down. Unlike a bought database losing ~30% freshness per
year: here, each use renews the consumed data.

## The engine (as presented on packdata.io)
"Our proprietary distributed protocol: a living, self-cleaning
stream. No more frozen snapshots — every use of the network
refreshes the data for everyone." The free Light Packdata client
(beta) lets contributors keep the network up to date — the Waze
effect applied to B2B data.
