<h1>Repository Map</h1>

This document defines where information should live across the Age Decision ecosystem.

<hr>

<h2>Central repository</h2>

Repository:

```text
credona/age-decision
```

Contains:

- global project overview
- architecture overview
- privacy model
- scoring model
- Zero Knowledge direction
- research references
- governance
- security policy

Does not contain:

- implementation details for each service
- per-repository changelogs
- service-specific test instructions
- model runtime configuration

<hr>

<h2>Core repository</h2>

Repository:

```text
credona/age-decision-core
```

Contains:

- age estimation service
- face detection
- decision policy
- core API contract
- core model documentation
- core benchmark notes

Recommended docs:

```text
docs/usage.md
docs/models.md
docs/benchmarks.md
CHANGELOG.md
CONTRIBUTING.md
```

<hr>

<h2>AntiSpoof repository</h2>

Repository:

```text
credona/age-decision-antispoof
```

Contains:

- anti-spoofing service
- still-image spoof detection
- model and heuristic fusion
- anti-spoof score contract
- anti-spoof benchmark notes

Recommended docs:

```text
docs/usage.md
docs/models.md
docs/benchmarks.md
CHANGELOG.md
CONTRIBUTING.md
```

<hr>

<h2>API repository</h2>

Repository:

```text
credona/age-decision-api
```

Contains:

- public gateway
- orchestration
- global decision aggregation
- public verification contract
- global score computation

Recommended docs:

```text
docs/usage.md
CHANGELOG.md
CONTRIBUTING.md
```

<hr>

<h2>JS SDK repository</h2>

Repository:

```text
credona/age-decision-js
```

Contains:

- TypeScript and JavaScript client
- typed request and response contracts
- retry and timeout handling
- SDK usage examples

Recommended docs:

```text
docs/usage.md
CHANGELOG.md
CONTRIBUTING.md
```

<hr>

<h2>Documentation rule</h2>

One topic should have one source of truth.

Do not copy the same explanation across multiple repositories.
