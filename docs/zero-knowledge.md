<h1>Zero Knowledge</h1>

Age Decision is currently proof-ready, not proof-generating.

The system exposes response structures that can later support verifiable claims without exposing unnecessary internal data.

<hr>

<h2>Goal</h2>

The long-term goal is to support verification flows where a relying party can verify an age-related claim without seeing:

- the raw image
- the estimated age
- internal model outputs
- downstream service internals

<hr>

<h2>Current state</h2>

Current services may expose metadata such as:

- proof readiness
- claim type
- proof status
- decision threshold

This metadata is a contract placeholder.

It is not a cryptographic proof.

<hr>

<h2>Future direction</h2>

Future work may include:

- signed verification results
- proof verification endpoints
- reusable Credona claim envelope
- verifier-side SDK helpers
- proof-friendly response parsing
- external verification examples

<hr>

<h2>Non-goals</h2>

The project does not currently provide:

- real Zero Knowledge proof generation
- legal proof of age
- identity binding
- reusable identity credential issuance
