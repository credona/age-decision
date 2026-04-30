<h1>Age Decision</h1>

<p>
  <img src="https://img.shields.io/badge/license-Apache%202.0-blue" alt="License">
  <img src="https://img.shields.io/badge/privacy-first-green" alt="Privacy First">
  <img src="https://img.shields.io/badge/decision-probabilistic-purple" alt="Probabilistic Decision">
  <img src="https://img.shields.io/badge/status-open%20source-black" alt="Open Source">
</p>

<h2>What is Age Decision</h2>


Age Decision is a privacy-first age decision system designed to determine whether a user is likely above or below a threshold (e.g. 18), without performing identity verification.

It provides probabilistic decisions that can be used as a pre-filter before stronger verification systems.

<hr>

<h2>What it is NOT</h2>

Age Decision does NOT:
- prove legal age
- perform identity verification
- perform biometric authentication
- replace KYC systems

<hr>

<h2>Typical use cases</h2>

- age gating before KYC
- reducing cost of identity verification providers
- filtering obviously underage users
- privacy-preserving eligibility checks

<hr>

<h2>Quick start</h2>

Choose your entry point:

1. API usage  
   https://github.com/credona/age-decision-api

2. JavaScript SDK  
   https://github.com/credona/age-decision-js

3. Core decision logic  
   https://github.com/credona/age-decision-core

4. Anti-spoof protection  
   https://github.com/credona/age-decision-antispoof

<hr>

<h2>Repositories</h2>

- Core: https://github.com/credona/age-decision-core
- AntiSpoof: https://github.com/credona/age-decision-antispoof
- API: https://github.com/credona/age-decision-api
- JS SDK: https://github.com/credona/age-decision-js

<hr>

<h2>System overview</h2>

Age Decision is composed of four repositories:

- `age-decision-core`: age estimation and decision policy
- `age-decision-antispoof`: still-image anti-spoofing analysis
- `age-decision-api`: public gateway and decision aggregation
- `age-decision-js`: TypeScript and JavaScript client SDK

<hr>

<h2>Documentation</h2>

- Architecture: docs/architecture.md
- Privacy: docs/privacy.md
- Scoring: docs/scoring.md
- Zero Knowledge: docs/zero-knowledge.md
- Research and references: docs/research.md
- Repository map: docs/repositories.md
- Governance: CONTRIBUTING.md

<hr>

<h2>Roadmap</h2>

See ROADMAP.md.

<hr>

<h2>Contributing</h2>

See CONTRIBUTING.md.

<hr>

<h2>Security</h2>

See SECURITY.md.

<hr>

<h2>License</h2>

This project is released under the Apache License 2.0.
