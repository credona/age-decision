<h1>Age Decision Roadmap</h1>

This roadmap tracks the global direction of the Age Decision ecosystem.

Repository-specific implementation details are tracked in each technical repository.

<hr>

<h2>Current focus</h2>

- stabilize public API contracts
- keep score naming consistent across services
- improve model and benchmark transparency
- document privacy guarantees
- prepare proof-friendly response structures

<hr>

<h2>Phase 1 - Open source foundation</h2>

- [x] Publish core age estimation service
- [x] Publish anti-spoofing service
- [x] Publish public API gateway
- [x] Publish JavaScript and TypeScript SDK
- [x] Add Docker-based local development
- [x] Add automated CI
- [x] Add release workflows
- [x] Add CodeQL scanning
- [x] Add Dependabot updates

<hr>

<h2>Phase 2 - Contract stabilization</h2>

- [x] Define `cred_decision_score`
- [x] Define `cred_antispoof_score`
- [x] Define `cred_global_score`
- [x] Keep legacy score aliases temporarily where needed
- [x] Add stable error response schemas
- [x] Add request tracing across services
- [x] Add OpenAPI contract tests
- [ ] Add unified error code documentation
- [ ] Add compatibility policy

<hr>

<h2>Phase 3 - Scientific transparency</h2>

- [ ] Document all models used by each service
- [ ] Document model origins and licenses
- [ ] Document benchmark datasets
- [ ] Publish benchmark methodology
- [ ] Add calibration notes
- [ ] Add known limitations and bias considerations
- [ ] Add reproducible benchmark reports

<hr>

<h2>Phase 4 - Developer adoption</h2>

- [ ] Add API usage examples
- [ ] Add SDK examples
- [ ] Add Node.js example
- [ ] Add browser example
- [ ] Add Nuxt / Next.js examples
- [ ] Add deployment reference
- [ ] Add production configuration guide

<hr>

<h2>Phase 5 - Trust and proof layer</h2>

- [ ] Define proof-friendly claim format
- [ ] Add signed verification result prototype
- [ ] Add proof verification endpoint
- [ ] Add reusable Credona score envelope
- [ ] Add verifier-side SDK helpers
- [ ] Research Zero Knowledge proof integration
- [ ] Add external verification example

<hr>

<h2>Phase 6 - Advanced liveness</h2>

- [ ] Add image sequence input
- [ ] Add short video input
- [ ] Add temporal consistency checks
- [ ] Add active liveness challenge research
- [ ] Add stronger replay attack resistance
