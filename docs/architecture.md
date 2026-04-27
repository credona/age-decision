<h1>Architecture</h1>

Age Decision is built as a small ecosystem of independent services and clients.

The goal is to keep each responsibility isolated while allowing a public API to expose one unified decision.

<hr>

<h2>High-level flow</h2>

```text
Client
  -> Age Decision API
      -> Age Decision Core
      -> Age Decision AntiSpoof
  -> Unified response
```

<hr>

<h2>Components</h2>

<h3>Age Decision Core</h3>

Responsible for:

- face detection
- age estimation
- threshold policy
- age decision scoring
- privacy metadata
- proof-ready response metadata

<h3>Age Decision AntiSpoof</h3>

Responsible for:

- still-image anti-spoofing
- real / spoof decision
- anti-spoof confidence
- anti-spoof trust score
- presentation attack metadata

<h3>Age Decision API</h3>

Responsible for:

- public verification endpoint
- downstream orchestration
- request tracing
- global decision aggregation
- global score computation
- privacy metadata aggregation

<h3>Age Decision JS SDK</h3>

Responsible for:

- typed client access
- request helpers
- timeout handling
- retry handling
- typed response contracts

<hr>

<h2>Design principles</h2>

- services should remain stateless
- image processing should be ephemeral by default
- API contracts should be explicit
- scores should be named by responsibility
- global documentation should not be duplicated in technical repositories

<hr>

<h2>Score ownership</h2>

- `cred_decision_score`: produced by Core
- `cred_antispoof_score`: produced by AntiSpoof
- `cred_global_score`: produced by API

The JS SDK only consumes these fields.
