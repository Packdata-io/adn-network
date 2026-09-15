# Light client — request frugality (2026-09-14)

The Packdata light client is throttled by design: 40 KB max requests
(fragmented data), user-adjustable pace (cycle interval, delay between
requests, AI-driven auto mode) with upfront impact estimate — zero impact on
data plans or battery at standard settings.

Each check starts from a single public URL, fetches only the observed
counter, and only the before/after delta travels. Each check is
declared, visible to the user and can be disabled at any time.
Requests carry only fingerprints, never raw data.
