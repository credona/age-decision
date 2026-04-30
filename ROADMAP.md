<h1>Age Decision Roadmap</h1>

This roadmap tracks the global direction of the Age Decision ecosystem.

Repository-specific implementation details are tracked in each technical repository.

<hr>

<h2>Legend</h2>

<pre>
type:
- feat: new feature
- fix: bug fix
- chore: maintenance or cleanup
- infra: infrastructure or CI/CD
- arch: internal architecture refactoring
- test: test strategy
- research: exploration
- docs: documentation

impact:
- X: breaking change
- Y: backward-compatible feature
- Z: internal change or fix

versioning:
- X → major version
- Y → minor version
- Z → patch version

repos:
- Core: https://github.com/credona/age-decision-core
- AntiSpoof: https://github.com/credona/age-decision-antispoof
- API: https://github.com/credona/age-decision-api
- JS SDK: https://github.com/credona/age-decision-js

status:
- [ ] planned
- [~] in progress / partial
- [x] completed
- [!] blocked
- -   not applicable
</pre>

<hr>

<h2>Current versions</h2>

<div style="display:flex;align-items:center; gap: 20px">
  <div style="display:flex;align-items:center; gap: 10px">
    <strong>core</strong>
    <img src="https://img.shields.io/github/v/release/credona/age-decision-core" alt="Age Decision Core release">
  </div>
  <div style="display:flex;align-items:center; gap: 10px">
    <strong>antispoof</strong>
    <img src="https://img.shields.io/github/v/release/credona/age-decision-antispoof" alt="Age Decision AntiSpoof release">
  </div>
  <div style="display:flex;align-items:center; gap: 10px">
    <strong>api</strong>
    <img src="https://img.shields.io/github/v/release/credona/age-decision-api" alt="Age Decision API release">
  </div>
  <div style="display:flex;align-items:center; gap: 10px">
    <strong>SDK JS</strong>
    <img src="https://img.shields.io/npm/v/@credona/age-decision" alt="Age Decision JS SDK npm version">
  </div>
</div>

<hr>

<h2>Completed in v2.0.0</h2>

<pre>
| description                              | core | antispoof | api | sdk | status |
|------------------------------------------|------|-----------|-----|-----|--------|
| privacy-first public contract            | [x]  | [x]       | [x] | [x] | [x]    |
| removed legacy cred_score                | [x]  | [x]       | [x] | [x] | [x]    |
| removed estimated age exposure           | [x]  | -         | [x] | [x] | [x]    |
| removed raw confidence exposure          | [x]  | [x]       | [x] | [x] | [x]    |
| explicit score ownership                 | [x]  | [x]       | [x] | [x] | [x]    |
| request tracing                          | [x]  | [x]       | [x] | [x] | [x]    |
| model documentation                      | [x]  | [x]       | -   | -   | [x]    |
| model binary policy                      | [x]  | [x]       | [x] | [x] | [x]    |
| OpenAPI / contract tests                 | [x]  | [x]       | [x] | [x] | [x]    |
| ZK-ready / proof-ready structure         | [x]  | -         | [x] | [x] | [x]    |
</pre>

<hr>

<h2>Completed in v2.1.0</h2>

<pre>
| description                              | core | antispoof | api | sdk | status |
|------------------------------------------|------|-----------|-----|-----|--------|
| centralized project metadata             | [x]  | [x]       | [x] | [x] | [x]    |
| centralized compatibility metadata       | [x]  | [x]       | [x] | [x] | [x]    |
| version endpoint                         | [x]  | [x]       | [x] | [x] | [x]    |
| generated documentation blocks           | [x]  | [x]       | [x] | [x] | [x]    |
| metadata validation scripts              | [x]  | [x]       | [x] | [x] | [x]    |
| release tag validation                   | [x]  | [x]       | [x] | [x] | [x]    |
| compatibility documentation              | [x]  | [x]       | [x] | [x] | [x]    |
| unified CI graph                         | [x]  | [x]       | [x] | [x] | [x]    |
| Docker runtime validation                | [x]  | [x]       | [x] | [x] | [x]    |
</pre>

<hr>

<h2>Completed in v2.2.0</h2>

<pre>
| type  | impact | target | description                                           | core | antispoof | api | sdk | status |
|-------|--------|--------|-------------------------------------------------------|------|-----------|-----|-----|--------|
| infra | Y      | 2.2.0  | one-command local check                               | [x]  | [x]       | [x] | [x] | [x]    |
| infra | Y      | 2.2.0  | one-command release preparation                       | [x]  | [x]       | [x] | [x] | [x]    |
| infra | Y      | 2.2.0  | update-all script                                     | [x]  | [x]       | [x] | [x] | [x]    |
| infra | Y      | 2.2.0  | check-all script                                      | [x]  | [x]       | [x] | [x] | [x]    |
| infra | Y      | 2.2.0  | automatic release tagging from metadata after main CI | [x]  | [x]       | [x] | [x] | [x]    |
| infra | Y      | 2.2.0  | tag-triggered GitHub release workflow                 | [x]  | [x]       | [x] | [x] | [x]    |
| infra | Y      | 2.2.0  | tag-triggered Docker image workflow                   | [x]  | [x]       | [x] | -   | [x]    |
| infra | Y      | 2.2.0  | tag-triggered npm publish workflow                    | -    | -         | -   | [x] | [x]    |
| infra | Y      | 2.2.0  | block push on CI-equivalent failures                  | [x]  | [x]       | [x] | [x] | [x]    |
| docs  | Z      | 2.2.0  | automate docs generation                              | [x]  | [x]       | [x] | [x] | [x]    |
| docs  | Z      | 2.2.0  | enforce generated blocks                              | [x]  | [x]       | [x] | [x] | [x]    |
| infra | Z      | 2.2.0  | test project.json version consistency                 | [x]  | [x]       | [x] | [x] | [x]    |
| infra | Z      | 2.2.0  | test package.json version consistency                 | -    | -         | -   | [x] | [x]    |
| infra | Z      | 2.2.0  | test release tag against metadata                     | [x]  | [x]       | [x] | [x] | [x]    |
</pre>

<hr>

<h2>Completed in v2.2.1</h2>

<pre>
| type  | impact | target | description                                                   | core | antispoof | api | sdk | status |
|-------|--------|--------|---------------------------------------------------------------|------|-----------|-----|-----|--------|
| infra | Y      | 2.2.1  | pre-commit hooks                                              | [x]  | [x]       | [x] | [x] | [x]    |
| infra | Y      | 2.2.1  | pre-push validation                                           | [x]  | [x]       | [x] | [x] | [x]    |
| infra | Y      | 2.2.1  | Docker-first local validation                                 | [x]  | [x]       | [x] | [x] | [x]    |
| infra | Y      | 2.2.1  | one-command auto-fix pipeline                                 | [x]  | [x]       | [x] | [x] | [x]    |
| infra | Y      | 2.2.1  | one-command CI-equivalent validation                          | [x]  | [x]       | [x] | [x] | [x]    |
| infra | Z      | 2.2.1  | single source of truth configuration via project.json         | [x]  | [x]       | [x] | [x] | [x]    |
| infra | Z      | 2.2.1  | generated runtime / compose environment                       | [x]  | [x]       | [x] | -   | [x]    |
| infra | Z      | 2.2.1  | package.json metadata synchronization                         | -    | -         | -   | [x] | [x]    |
| infra | Z      | 2.2.1  | compatibility.json auto-synchronization                       | [x]  | [x]       | [x] | [x] | [x]    |
| infra | Z      | 2.2.1  | test project metadata consistency                             | [x]  | [x]       | [x] | [x] | [x]    |
| infra | Z      | 2.2.1  | test package metadata consistency                             | -    | -         | -   | [x] | [x]    |
| infra | Z      | 2.2.1  | test Docker image metadata consistency                        | [x]  | [x]       | [x] | -   | [x]    |
| infra | Z      | 2.2.1  | dynamic Docker OCI labels from project metadata               | [x]  | [x]       | [x] | -   | [x]    |
| infra | Z      | 2.2.1  | integration Docker image version synchronization              | -    | -         | -   | [x] | [x]    |
| docs  | Z      | 2.2.1  | prevent manual documentation drift                            | [x]  | [x]       | [x] | [x] | [x]    |
| docs  | Z      | 2.2.1  | simplify contributor documentation                            | [x]  | [x]       | [x] | [x] | [x]    |
| docs  | Z      | 2.2.1  | remove static .env workflow from documentation                | [x]  | [x]       | [x] | -   | [x]    |
| docs  | Z      | 2.2.1  | document generated configuration policy                       | [x]  | [x]       | [x] | [x] | [x]    |
| chore | Z      | 2.2.1  | remove duplicated local configuration files                   | [x]  | [x]       | [x] | -   | [x]    |
| chore | Z      | 2.2.1  | reduce manual command surface for contributors                | [x]  | [x]       | [x] | [x] | [x]    |
</pre>

<hr>

<h2>Completed in v2.2.2 – Release and package hygiene</h2>

<pre>
| type  | impact | target | description                                                    | core | antispoof | api | sdk | status |
|-------|--------|--------|----------------------------------------------------------------|------|-----------|-----|-----|--------|
| infra | Z      | 2.2.2  | inject changelog content into release description              | [x]  | [x]       | [x] | [x] | [x]    |
| docs  | Z      | 2.2.2  | generate changelog sections automatically                      | [x]  | [x]       | [x] | [x] | [x]    |
| infra | Z      | 2.2.2  | prevent Docker image publication from pull request workflows   | [x]  | [x]       | [x] | -   | [x]    |
| infra | Z      | 2.2.2  | publish Docker images only from version tags                   | [x]  | [x]       | [x] | -   | [x]    |
| infra | Z      | 2.2.2  | delete existing untagged Docker package versions               | [x]  | [x]       | [x] | -   | [x]    |
| infra | Z      | 2.2.2  | add untagged Docker package cleanup workflow                   | [x]  | [x]       | [x] | -   | [x]    |
| infra | Z      | 2.2.2  | validate one tagged Docker image per released version          | [x]  | [x]       | [x] | -   | [x]    |
| infra | Z      | 2.2.2  | ensure SDK npm publication remains tag-only                    | -    | -         | -   | [x] | [x]    |
</pre>

<hr>

<h2>Completed in v2.2.3 – Documentation restructuring</h2>

<pre>
| type | impact | target | description                                      | core | antispoof | api | sdk | status |
|------|--------|--------|--------------------------------------------------|------|-----------|-----|-----|--------|
| docs | Z      | 2.2.3  | enforce documentation boundaries                 | [ ]  | [ ]       | [ ] | [ ] | [ ]    |
| docs | Z      | 2.2.3  | remove cross-repository duplication              | [ ]  | [ ]       | [ ] | [ ] | [ ]    |
| docs | Z      | 2.2.3  | normalize repository README scope                | [ ]  | [ ]       | [ ] | [ ] | [ ]    |
| docs | Z      | 2.2.3  | normalize CONTRIBUTING to local workflows        | [ ]  | [ ]       | [ ] | [ ] | [ ]    |
| docs | Z      | 2.2.3  | normalize SECURITY and COMPATIBILITY scope       | [ ]  | [ ]       | [ ] | [ ] | [ ]    |
| docs | Z      | 2.2.3  | enforce absolute GitHub documentation linking    | [ ]  | [ ]       | [ ] | [ ] | [ ]    |
| docs | Z      | 2.2.3  | centralize global documentation in age-decision  | [ ]  | [ ]       | [ ] | [ ] | [ ]    |
</pre>
<hr>

<h2>v2.3.0 – Public contract governance</h2>

<pre>
| type  | impact | target | description                                      | core | antispoof | api | sdk | status |
|-------|--------|--------|--------------------------------------------------|------|-----------|-----|-----|--------|
| feat  | Y      | 2.3.0  | stable status contract                           | [ ]  | [ ]       | [ ] | [ ] | [ ]    |
| feat  | Y      | 2.3.0  | standardized error code and message model        | [ ]  | [ ]       | [ ] | [ ] | [ ]    |
| feat  | Y      | 2.3.0  | normalized request validation                    | [ ]  | [ ]       | [ ] | [ ] | [ ]    |
| feat  | Y      | 2.3.0  | typed SDK error mapping                          | -    | -         | -   | [ ] | [ ]    |
| test  | Y      | 2.3.0  | public contract regression tests                 | [ ]  | [ ]       | [ ] | [ ] | [ ]    |
</pre>

<hr>

<h2>v2.3.1 – Deprecation and contract documentation</h2>

<pre>
| type  | impact | target | description                                      | core | antispoof | api | sdk | status |
|-------|--------|--------|--------------------------------------------------|------|-----------|-----|-----|--------|
| docs  | Z      | 2.3.1  | deprecation policy                               | [ ]  | [ ]       | [ ] | [ ] | [ ]    |
| docs  | Z      | 2.3.1  | error model documentation                        | [ ]  | [ ]       | [ ] | [ ] | [ ]    |
| docs  | Z      | 2.3.1  | status contract documentation                    | [ ]  | [ ]       | [ ] | [ ] | [ ]    |
</pre>

<hr>

<h2>v2.4.0 – Production guardrails</h2>

<pre>
| type  | impact | target | description                                      | core | antispoof | api | sdk | status |
|-------|--------|--------|--------------------------------------------------|------|-----------|-----|-----|--------|
| feat  | Y      | 2.4.0  | payload size limits                              | [ ]  | [ ]       | [ ] | [ ] | [ ]    |
| feat  | Y      | 2.4.0  | request timeout policy                           | [ ]  | [ ]       | [ ] | [ ] | [ ]    |
| feat  | Y      | 2.4.0  | API authentication                               | -    | -         | [ ] | [ ] | [ ]    |
| feat  | Y      | 2.4.0  | API rate limiting                                | -    | -         | [ ] | [ ] | [ ]    |
| test  | Y      | 2.4.0  | security and limits regression tests             | [ ]  | [ ]       | [ ] | [ ] | [ ]    |
</pre>

<hr>

<h2>v2.4.1 – Production documentation</h2>

<pre>
| type  | impact | target | description                                      | core | antispoof | api | sdk | status |
|-------|--------|--------|--------------------------------------------------|------|-----------|-----|-----|--------|
| docs  | Z      | 2.4.1  | production security guide                        | [ ]  | [ ]       | [ ] | [ ] | [ ]    |
| docs  | Z      | 2.4.1  | deployment configuration guide                   | [ ]  | [ ]       | [ ] | -   | [ ]    |
| docs  | Z      | 2.4.1  | SDK authentication usage guide                   | -    | -         | -   | [ ] | [ ]    |
</pre>

<hr>

<h2>v2.5.0 – Internal architecture refactoring</h2>

<pre>
| type  | impact | target | description                                      | core | antispoof | api | sdk | status |
|-------|--------|--------|--------------------------------------------------|------|-----------|-----|-----|--------|
| test  | Y      | 2.5.0  | freeze public contracts before refactoring       | [ ]  | [ ]       | [ ] | [ ] | [ ]    |
| arch  | Y      | 2.5.0  | introduce clean architecture boundaries          | [ ]  | -         | -   | -   | [ ]    |
| arch  | Y      | 2.5.0  | introduce pipeline-oriented architecture         | -    | [ ]       | -   | -   | [ ]    |
| arch  | Y      | 2.5.0  | introduce hexagonal orchestration architecture   | -    | -         | [ ] | -   | [ ]    |
| arch  | Y      | 2.5.0  | restructure SDK into layered architecture        | -    | -         | -   | [ ] | [ ]    |
| chore | Y      | 2.5.0  | isolate domain logic from framework code         | [ ]  | [ ]       | [ ] | -   | [ ]    |
| chore | Y      | 2.5.0  | introduce application use cases                  | [ ]  | [ ]       | [ ] | -   | [ ]    |
| chore | Y      | 2.5.0  | move technical adapters to infrastructure layer  | [ ]  | [ ]       | [ ] | -   | [ ]    |
| test  | Y      | 2.5.0  | split tests into unit, integration and contract  | [ ]  | [ ]       | [ ] | [ ] | [ ]    |
| docs  | Z      | 2.5.0  | document repository architecture                 | [ ]  | [ ]       | [ ] | [ ] | [ ]    |
</pre>

<hr>

<h2>v2.5.x – Post-refactoring stabilization</h2>

<pre>
| type  | impact | target | description                                      | core | antispoof | api | sdk | status |
|-------|--------|--------|--------------------------------------------------|------|-----------|-----|-----|--------|
| fix   | Z      | 2.5.1  | fix regressions introduced by architecture split | [ ]  | [ ]       | [ ] | [ ] | [ ]    |
| test  | Z      | 2.5.1  | increase contract coverage after refactoring     | [ ]  | [ ]       | [ ] | [ ] | [ ]    |
| docs  | Z      | 2.5.1  | align usage docs with new internal structure     | [ ]  | [ ]       | [ ] | [ ] | [ ]    |
| infra | Z      | 2.5.2  | enforce architecture boundaries in CI            | [ ]  | [ ]       | [ ] | [ ] | [ ]    |
| infra | Z      | 2.5.2  | detect forbidden imports across layers           | [ ]  | [ ]       | [ ] | -   | [ ]    |
</pre>

<hr>

<h2>v2.6.0 – Model lifecycle and transparency</h2>

<pre>
| type  | impact | target | description                                      | core | antispoof | api | sdk | status |
|-------|--------|--------|--------------------------------------------------|------|-----------|-----|-----|--------|
| feat  | Y      | 2.6.0  | model validation                                 | [ ]  | [ ]       | -   | -   | [ ]    |
| feat  | Y      | 2.6.0  | model versioning                                 | [ ]  | [ ]       | -   | -   | [ ]    |
| feat  | Y      | 2.6.0  | model metadata inspection                        | [ ]  | [ ]       | [ ] | [ ] | [ ]    |
| docs  | Z      | 2.6.0  | dataset transparency                             | [ ]  | [~]       | -   | -   | [~]    |
| docs  | Z      | 2.6.0  | benchmark methodology                            | [~]  | [~]       | -   | -   | [~]    |
| infra | Y      | 2.6.0  | reproducible benchmark workflow                  | [ ]  | [~]       | -   | -   | [~]    |
</pre>

<hr>

<h2>v2.7.0 – Deployment and scalability</h2>

<pre>
| type  | impact | target | description                                      | core | antispoof | api | sdk | status |
|-------|--------|--------|--------------------------------------------------|------|-----------|-----|-----|--------|
| feat  | Y      | 2.7.0  | production Docker Compose stack                  | [ ]  | [ ]       | [ ] | -   | [ ]    |
| feat  | Y      | 2.7.0  | Kubernetes deployment manifests                  | [ ]  | [ ]       | [ ] | -   | [ ]    |
| feat  | Y      | 2.7.0  | service resource limits documentation            | [ ]  | [ ]       | [ ] | -   | [ ]    |
| infra | Z      | 2.7.1  | deployment smoke tests                           | [ ]  | [ ]       | [ ] | [ ] | [ ]    |
| docs  | Z      | 2.7.1  | deployment guide                                 | [ ]  | [ ]       | [ ] | -   | [ ]    |
</pre>

<hr>

<h2>v2.8.0 – Advanced ML lifecycle</h2>

<pre>
| type  | impact | target | description                                      | core | antispoof | api | sdk | status |
|-------|--------|--------|--------------------------------------------------|------|-----------|-----|-----|--------|
| feat  | Y      | 2.8.0  | multi-model support                              | [ ]  | [ ]       | -   | -   | [ ]    |
| feat  | Y      | 2.8.0  | model reproducibility                            | [ ]  | [ ]       | -   | -   | [ ]    |
| feat  | Y      | 2.8.0  | calibration workflow                             | [ ]  | [ ]       | -   | -   | [ ]    |
| docs  | Z      | 2.8.0  | advanced model lifecycle documentation           | [ ]  | [ ]       | [ ] | -   | [ ]    |
</pre>

<hr>

<h2>v3.0.0 – Temporal and video-based verification</h2>

<pre>
| type | impact | target | description                                      | core | antispoof | api | sdk | status |
|------|--------|--------|--------------------------------------------------|------|-----------|-----|-----|--------|
| feat | X      | 3.0.0  | image sequence input                             | [ ]  | [ ]       | [ ] | [ ] | [ ]    |
| feat | X      | 3.0.0  | video liveness                                   | [ ]  | [ ]       | [ ] | [ ] | [ ]    |
| feat | X      | 3.0.0  | temporal scoring                                 | [ ]  | [ ]       | [ ] | [ ] | [ ]    |
| feat | X      | 3.0.0  | replay attack resistance                         | [ ]  | [ ]       | [ ] | [ ] | [ ]    |
</pre>

<hr>

<h2>Release policy</h2>

<pre>
- pull requests validate quality, metadata, generated documentation and tests
- pull requests must never publish Docker images, npm packages or releases
- only main branch can trigger version tag creation
- version is read from project.json / package.json
- tag vX.Y.Z is created automatically after successful CI on main
- tag triggers:
  - GitHub release
  - Docker image publication for core, antispoof and api
  - npm publication for SDK

- Docker images must be published only from version tags
- Docker package versions without tags must be deleted
- each released version must produce one version-tagged Docker package per Dockerized repository
- release description should be generated from CHANGELOG.md
- CHANGELOG.md should become the single source of truth for release notes
</pre>

<hr>

<h2>Notes</h2>

<pre>
- patch versions are strictly internal fixes
- minor versions introduce backward-compatible features
- major versions introduce breaking changes
- internal architecture refactoring can be released as a minor version when public contracts remain compatible
- badges are visual indicators only; metadata files remain the source of truth
- roadmap reflects actual implementation state
- cross-repo alignment must respect compatibility metadata
- SDK must remain a client only
- API must remain an orchestration gateway
- Core owns age decision scoring
- AntiSpoof owns presentation attack scoring
</pre>
