<h1>Governance</h1>

Age Decision is maintained by Credona.

This document defines how the ecosystem is organized.

<hr>

<h2>Repository roles</h2>

- `age-decision`: global documentation and project coordination
- `age-decision-core`: age estimation service
- `age-decision-antispoof`: anti-spoofing service
- `age-decision-api`: public gateway
- `age-decision-js`: JavaScript and TypeScript SDK

<hr>

<h2>Documentation ownership</h2>

Global concepts are maintained in this repository.

Technical implementation details are maintained in the relevant technical repository.

This avoids duplicated documentation and keeps each repository focused.

<hr>

<h2>Decision model</h2>

Public decisions are probabilistic.

The system should never claim to prove a person's real age, identity or legal status.

The project may expose scores and metadata to help downstream systems decide how to handle uncertainty.

<hr>

<h2>Compatibility policy</h2>

Public API fields should remain stable once adopted by downstream repositories.

When a field is renamed, a temporary compatibility alias may be kept during a transition period.

Breaking changes should be documented in the relevant repository changelog.

<hr>

<h2>Release ownership</h2>

Each technical repository owns its own release lifecycle.

The central repository tracks project direction but does not replace per-repository changelogs.

<hr>

<h2>Contribution review</h2>

Changes should be reviewed for:

- privacy impact
- API compatibility
- reproducibility
- documentation clarity
- model and benchmark transparency
