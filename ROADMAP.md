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
- sec: security hardening

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
- Docs: https://github.com/credona/age-decision

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
| type | impact | target | description                                       | core | antispoof | api | sdk | status |
|------|--------|--------|---------------------------------------------------|------|-----------|-----|-----|--------|
| docs | Z      | 2.2.3  | enforce documentation boundaries                  | [x]  | [x]       | [x] | [x] | [x]    |
| docs | Z      | 2.2.3  | remove cross-repository duplication               | [x]  | [x]       | [x] | [x] | [x]    |
| docs | Z      | 2.2.3  | normalize repository README scope                 | [x]  | [x]       | [x] | [x] | [x]    |
| docs | Z      | 2.2.3  | normalize CONTRIBUTING to local workflows         | [x]  | [x]       | [x] | [x] | [x]    |
| docs | Z      | 2.2.3  | normalize SECURITY and COMPATIBILITY scope        | [x]  | [x]       | [x] | [x] | [x]    |
| docs | Z      | 2.2.3  | enforce absolute GitHub documentation linking     | [x]  | [x]       | [x] | [x] | [x]    |
| docs | Z      | 2.2.3  | centralize global documentation in age-decision   | [x]  | [x]       | [x] | [x] | [x]    |
| docs | Z      | 2.2.3  | adapt docs generation to concise README structure | [x]  | [x]       | [x] | [x] | [x]    |
</pre>

<hr>

<h2>Completed in v2.3.0 – Public contract governance</h2>

<pre>
| type  | impact | target | description                               | core | antispoof | api | sdk | status |
|-------|--------|--------|-------------------------------------------|------|-----------|-----|-----|--------|
| feat  | Y      | 2.3.0  | stable status contract                    | [x]  | [x]       | [x] | [x] | [x]    |
| feat  | Y      | 2.3.0  | standardized error code and message model | [x]  | [x]       | [x] | [x] | [x]    |
| feat  | Y      | 2.3.0  | normalized request validation             | [x]  | [x]       | [x] | [x] | [x]    |
| feat  | Y      | 2.3.0  | typed SDK error mapping                   | -    | -         | -   | [x] | [x]    |
| test  | Y      | 2.3.0  | public contract regression tests          | [x]  | [x]       | [x] | [x] | [x]    |
| docs  | Z      | 2.3.0  | deprecation policy                        | [x]  | [x]       | [x] | [x] | [x]    |
| docs  | Z      | 2.3.0  | error model documentation                 | [x]  | [x]       | [x] | [x] | [x]    |
| docs  | Z      | 2.3.0  | status contract documentation             | [x]  | [x]       | [x] | [x] | [x]    |
</pre>

<hr>

<h2>Completed in v2.4.0 – Internal architecture refactoring</h2>

<pre>
| type  | impact | target | description                                            | core | antispoof | api | sdk | status |
|-------|--------|--------|--------------------------------------------------------|------|-----------|-----|-----|--------|
| test  | Y      | 2.4.0  | freeze public contracts before refactoring             | [x]  | [x]       | [x] | [x] | [x]    |
| arch  | Y      | 2.4.0  | introduce clean architecture boundaries                | [x]  | -         | -   | -   | [x]    |
| arch  | Y      | 2.4.0  | introduce pipeline-oriented architecture               | -    | [x]       | -   | -   | [x]    |
| arch  | Y      | 2.4.0  | introduce hexagonal orchestration architecture         | -    | -         | [x] | -   | [x]    |
| arch  | Y      | 2.4.0  | restructure SDK into layered architecture              | -    | -         | -   | [x] | [x]    |
| chore | Y      | 2.4.0  | isolate domain logic from framework code               | [x]  | [x]       | [x] | -   | [x]    |
| chore | Y      | 2.4.0  | introduce application use cases                        | [x]  | [x]       | [x] | -   | [x]    |
| chore | Y      | 2.4.0  | move technical adapters to infrastructure layer        | [x]  | [x]       | [x] | -   | [x]    |
| chore | Y      | 2.4.0  | replace legacy public names with neutral terminology   | [x]  | [x]       | [x] | [x] | [x]    |
| chore | Y      | 2.4.0  | centralize public decision constants                   | [x]  | [x]       | [x] | [x] | [x]    |
| test  | Y      | 2.4.0  | split tests into unit, integration and contract        | [x]  | [x]       | [x] | [x] | [x]    |
| docs  | Z      | 2.4.0  | document repository architecture                       | [x]  | [x]       | [x] | [x] | [x]    |
| test  | Y      | 2.4.0  | enforce privacy-safe logs coverage                     | [x]  | [x]       | [x] | -   | [x]    |
| test  | Y      | 2.4.0  | reject unsupported input types deterministically       | [x]  | [x]       | [x] | [x] | [x]    |
| sec   | Y      | 2.4.0  | prevent raw downstream responses from public outputs   | [x]  | [x]       | [x] | [x] | [x]    |
| chore | Y      | 2.4.0  | prepare public input model for v3 multi-input support  | [x]  | [x]       | [x] | [x] | [x]    |
</pre>

<hr>

<h2>v2.5.0 – Model lifecycle, scoring methodology and configuration simplification</h2>

<pre>
| type  | impact | target | description                                           | core | antispoof | api | sdk | docs | status |
|-------|--------|--------|-------------------------------------------------------|------|-----------|-----|-----|------|--------|
| feat  | Y      | 2.5.0  | model metadata schema                                 | [ ]  | [ ]       | [ ] | [ ] | [ ]  | [ ]    |
| feat  | Y      | 2.5.0  | exact model registry schema                           | [ ]  | [ ]       | [ ] | [ ] | [ ]  | [ ]    |
| feat  | Y      | 2.5.0  | model validation                                      | [ ]  | [ ]       | -   | -   | -    | [ ]    |
| feat  | Y      | 2.5.0  | model versioning                                      | [ ]  | [ ]       | [ ] | [ ] | [ ]  | [ ]    |
| feat  | Y      | 2.5.0  | model registry abstraction                            | [ ]  | [ ]       | -   | -   | -    | [ ]    |
| feat  | Y      | 2.5.0  | deterministic model selection policy                  | [ ]  | [ ]       | [ ] | -   | -    | [ ]    |
| feat  | Y      | 2.5.0  | model reproducibility metadata                        | [ ]  | [ ]       | [ ] | -   | [ ]  | [ ]    |
| feat  | Y      | 2.5.0  | minimal multi-model configuration                     | [ ]  | [ ]       | [ ] | -   | [ ]  | [ ]    |
| feat  | Y      | 2.5.0  | replace model paths with model identifiers            | [ ]  | [ ]       | [ ] | [ ] | [ ]  | [ ]    |
| chore | Z      | 2.5.0  | simplify project.json runtime structure               | [ ]  | [ ]       | [ ] | [ ] | [ ]  | [ ]    |
| chore | Z      | 2.5.0  | remove dev/prod runtime duplication                   | [ ]  | [ ]       | [ ] | [ ] | [ ]  | [ ]    |
| chore | Z      | 2.5.0  | remove low-level model path configuration             | [ ]  | [ ]       | [ ] | [ ] | [ ]  | [ ]    |
| chore | Z      | 2.5.0  | remove non-deterministic runtime flags                | [ ]  | [ ]       | [ ] | [ ] | [ ]  | [ ]    |
| chore | Z      | 2.5.0  | enforce privacy-first runtime invariants              | [ ]  | [ ]       | [ ] | [ ] | [ ]  | [ ]    |
| feat  | Y      | 2.5.0  | public scoring methodology                            | [ ]  | [ ]       | [ ] | [ ] | [ ]  | [ ]    |
| feat  | Y      | 2.5.0  | mathematical definition of cred_decision_score        | [ ]  | -         | [ ] | [ ] | [ ]  | [ ]    |
| feat  | Y      | 2.5.0  | mathematical definition of cred_antispoof_score       | -    | [ ]       | [ ] | [ ] | [ ]  | [ ]    |
| feat  | Y      | 2.5.0  | mathematical definition of cred_global_score          | -    | -         | [ ] | [ ] | [ ]  | [ ]    |
| feat  | Y      | 2.5.0  | calibration methodology                               | [ ]  | [ ]       | [ ] | -   | [ ]  | [ ]    |
| feat  | Y      | 2.5.0  | scoring policy abstraction                            | [ ]  | [ ]       | [ ] | -   | [ ]  | [ ]    |
| feat  | Y      | 2.5.0  | move thresholds to model scoring policy               | [ ]  | [ ]       | [ ] | -   | [ ]  | [ ]    |
| feat  | Y      | 2.5.0  | remove threshold logic from runtime config            | [ ]  | [ ]       | [ ] | [ ] | [ ]  | [ ]    |
| test  | Y      | 2.5.0  | score bounds and monotonicity tests                   | [ ]  | [ ]       | [ ] | [ ] | -    | [ ]    |
| test  | Y      | 2.5.0  | score stability tests                                 | [ ]  | [ ]       | [ ] | [ ] | -    | [ ]    |
| test  | Y      | 2.5.0  | score privacy regression tests                        | [ ]  | [ ]       | [ ] | [ ] | -    | [ ]    |
| test  | Y      | 2.5.0  | model contract and metadata tests                     | [ ]  | [ ]       | [ ] | [ ] | -    | [ ]    |
| docs  | Z      | 2.5.0  | model registry documentation                          | [ ]  | [ ]       | [ ] | [ ] | [ ]  | [ ]    |
| docs  | Z      | 2.5.0  | scoring methodology documentation                     | [ ]  | [ ]       | [ ] | [ ] | [ ]  | [ ]    |
| docs  | Z      | 2.5.0  | dataset transparency                                  | [ ]  | [ ]       | -   | -   | [ ]  | [ ]    |
| docs  | Z      | 2.5.0  | benchmark methodology                                 | [ ]  | [ ]       | -   | -   | [ ]  | [ ]    |
</pre>

<hr>

<h2>v2.6.0 – Benchmark, calibration reporting and reproducibility</h2>

<pre>
| type  | impact | target | description                                         | core | antispoof | api | sdk | docs | status |
|-------|--------|--------|-----------------------------------------------------|------|-----------|-----|-----|------|--------|
| infra | Y      | 2.6.0  | core model benchmark execution scripts              | [ ]  | -         | -   | -   | -    | [ ]    |
| infra | Y      | 2.6.0  | antispoof model benchmark execution scripts         | -    | [ ]       | -   | -   | -    | [ ]    |
| infra | Y      | 2.6.0  | core service benchmark execution scripts            | [ ]  | -         | -   | -   | -    | [ ]    |
| infra | Y      | 2.6.0  | antispoof service benchmark execution scripts       | -    | [ ]       | -   | -   | -    | [ ]    |
| infra | Y      | 2.6.0  | end-to-end API benchmark execution scripts          | -    | -         | [ ] | [ ] | -    | [ ]    |
| infra | Y      | 2.6.0  | benchmark report generation                         | [ ]  | [ ]       | [ ] | -   | [ ]  | [ ]    |
| docs  | Z      | 2.6.0  | calibration report                                  | [ ]  | [ ]       | [ ] | -   | [ ]  | [ ]    |
| docs  | Z      | 2.6.0  | cred_decision_score benchmark report                | [ ]  | -         | [ ] | -   | [ ]  | [ ]    |
| docs  | Z      | 2.6.0  | cred_antispoof_score benchmark report               | -    | [ ]       | [ ] | -   | [ ]  | [ ]    |
| docs  | Z      | 2.6.0  | cred_global_score benchmark report                  | -    | -         | [ ] | -   | [ ]  | [ ]    |
| docs  | Z      | 2.6.0  | benchmark machine characteristics                   | [ ]  | [ ]       | [ ] | -   | [ ]  | [ ]    |
| docs  | Z      | 2.6.0  | dataset usage and limitation documentation          | [ ]  | [ ]       | -   | -   | [ ]  | [ ]    |
| docs  | Z      | 2.6.0  | model comparison report                             | [ ]  | [ ]       | [ ] | -   | [ ]  | [ ]    |
| test  | Y      | 2.6.0  | benchmark reproducibility tests                     | [ ]  | [ ]       | [ ] | -   | -    | [ ]    |
| test  | Y      | 2.6.0  | benchmark output schema tests                       | [ ]  | [ ]       | [ ] | -   | -    | [ ]    |
</pre>

<hr>

<h2>v2.7.0 – Production guardrails</h2>

<pre>
| type  | impact | target | description                          | core | antispoof | api | sdk | status |
|-------|--------|--------|--------------------------------------|------|-----------|-----|-----|--------|
| feat  | Y      | 2.7.0  | payload size limits                  | [ ]  | [ ]       | [ ] | [ ] | [ ]    |
| feat  | Y      | 2.7.0  | request timeout policy               | [ ]  | [ ]       | [ ] | [ ] | [ ]    |
| feat  | Y      | 2.7.0  | API authentication                   | -    | -         | [ ] | [ ] | [ ]    |
| feat  | Y      | 2.7.0  | API rate limiting                    | -    | -         | [ ] | [ ] | [ ]    |
| sec   | Y      | 2.7.0  | privacy-safe audit event policy      | [ ]  | [ ]       | [ ] | -   | [ ]    |
| test  | Y      | 2.7.0  | security and limits regression tests | [ ]  | [ ]       | [ ] | [ ] | [ ]    |
</pre>

<hr>

<h2>v2.7.1 – Production documentation</h2>

<pre>
| type | impact | target | description                    | core | antispoof | api | sdk | docs | status |
|------|--------|--------|--------------------------------|------|-----------|-----|-----|------|--------|
| docs | Z      | 2.7.1  | production security guide      | [ ]  | [ ]       | [ ] | [ ] | [ ]  | [ ]    |
| docs | Z      | 2.7.1  | deployment configuration guide | [ ]  | [ ]       | [ ] | -   | [ ]  | [ ]    |
| docs | Z      | 2.7.1  | SDK authentication usage guide | -    | -         | -   | [ ] | [ ]  | [ ]    |
| docs | Z      | 2.7.1  | operational privacy guide      | [ ]  | [ ]       | [ ] | -   | [ ]  | [ ]    |
</pre>

<hr>

<h2>v2.8.0 – Deployment and scalability</h2>

<pre>
| type  | impact | target | description                           | core | antispoof | api | sdk | docs | status |
|-------|--------|--------|---------------------------------------|------|-----------|-----|-----|------|--------|
| feat  | Y      | 2.8.0  | production Docker Compose stack       | [ ]  | [ ]       | [ ] | -   | -    | [ ]    |
| feat  | Y      | 2.8.0  | Kubernetes deployment manifests       | [ ]  | [ ]       | [ ] | -   | -    | [ ]    |
| feat  | Y      | 2.8.0  | service resource limits documentation | [ ]  | [ ]       | [ ] | -   | [ ]  | [ ]    |
| infra | Z      | 2.8.0  | deployment smoke tests                | [ ]  | [ ]       | [ ] | [ ] | -    | [ ]    |
| docs  | Z      | 2.8.0  | deployment guide                      | [ ]  | [ ]       | [ ] | -   | [ ]  | [ ]    |
</pre>

<hr>

<h2>v2.9.0 – Advanced ML lifecycle and recalibration</h2>

<pre>
| type  | impact | target | description                                      | core | antispoof | api | sdk | docs | status |
|-------|--------|--------|--------------------------------------------------|------|-----------|-----|-----|------|--------|
| feat  | Y      | 2.9.0  | recalibration workflow                           | [ ]  | [ ]       | [ ] | -   | -    | [ ]    |
| feat  | Y      | 2.9.0  | recalibration dataset policy                     | [ ]  | [ ]       | [ ] | -   | [ ]  | [ ]    |
| feat  | Y      | 2.9.0  | recalibration validation gates                   | [ ]  | [ ]       | [ ] | -   | [ ]  | [ ]    |
| feat  | Y      | 2.9.0  | model ensemble strategy                          | [ ]  | [ ]       | [ ] | -   | -    | [ ]    |
| feat  | Y      | 2.9.0  | model drift monitoring preparation               | [ ]  | [ ]       | [ ] | -   | [ ]  | [ ]    |
| feat  | Y      | 2.9.0  | score drift monitoring preparation               | [ ]  | [ ]       | [ ] | -   | [ ]  | [ ]    |
| feat  | Y      | 2.9.0  | offline evaluation pipeline                      | [ ]  | [ ]       | [ ] | -   | [ ]  | [ ]    |
| feat  | Y      | 2.9.0  | model rollback policy                            | [ ]  | [ ]       | [ ] | -   | [ ]  | [ ]    |
| test  | Y      | 2.9.0  | recalibration regression tests                   | [ ]  | [ ]       | [ ] | -   | -    | [ ]    |
| test  | Y      | 2.9.0  | drift detection policy tests                     | [ ]  | [ ]       | [ ] | -   | -    | [ ]    |
| docs  | Z      | 2.9.0  | advanced model lifecycle documentation           | [ ]  | [ ]       | [ ] | -   | [ ]  | [ ]    |
| docs  | Z      | 2.9.0  | recalibration methodology documentation          | [ ]  | [ ]       | [ ] | -   | [ ]  | [ ]    |
</pre>

<hr>

<h2>v2.10.0 – Documentation website, demo and developer experience</h2>

<pre>
| type  | impact | target | description                                 | core | antispoof | api | sdk | docs | status |
|-------|--------|--------|---------------------------------------------|------|-----------|-----|-----|------|--------|
| feat  | Y      | 2.10.0 | public demo playground on credona.dev        | [ ]  | [ ]       | [ ] | [ ] | [ ]  | [ ]    |
| feat  | Y      | 2.10.0 | documentation website on docs.credona.dev    | -    | -         | -   | -   | [ ]  | [ ]    |
| feat  | Y      | 2.10.0 | guided capture UX                           | [ ]  | [ ]       | [ ] | [ ] | [ ]  | [ ]    |
| feat  | Y      | 2.10.0 | head movement challenge flow                | -    | [ ]       | [ ] | [ ] | [ ]  | [ ]    |
| feat  | Y      | 2.10.0 | front-end capture frame and visual guidance | -    | -         | [ ] | [ ] | [ ]  | [ ]    |
| feat  | Y      | 2.10.0 | SDK browser helper for capture workflow     | -    | -         | -   | [ ] | [ ]  | [ ]    |
| docs  | Z      | 2.10.0 | public getting-started documentation        | [ ]  | [ ]       | [ ] | [ ] | [ ]  | [ ]    |
| docs  | Z      | 2.10.0 | demo limitations and privacy explanation    | [ ]  | [ ]       | [ ] | [ ] | [ ]  | [ ]    |
| test  | Y      | 2.10.0 | public demo smoke tests                     | -    | -         | [ ] | [ ] | [ ]  | [ ]    |
</pre>

<hr>

<h2>v3.0.0 – Temporal and video-based verification</h2>

<pre>
| type | impact | target | description              | core | antispoof | api | sdk | status |
|------|--------|--------|--------------------------|------|-----------|-----|-----|--------|
| feat | X      | 3.0.0  | image sequence input     | [ ]  | [ ]       | [ ] | [ ] | [ ]    |
| feat | X      | 3.0.0  | video liveness           | [ ]  | [ ]       | [ ] | [ ] | [ ]    |
| feat | X      | 3.0.0  | temporal scoring         | [ ]  | [ ]       | [ ] | [ ] | [ ]    |
| feat | X      | 3.0.0  | replay attack resistance | [ ]  | [ ]       | [ ] | [ ] | [ ]    |
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
- CHANGELOG.md should be the single source of truth for release notes
</pre>

<hr>

<h2>Notes</h2>

<pre>
- patch versions are strictly internal fixes
- minor versions introduce backward-compatible features
- major versions introduce breaking changes
- production hardening must happen before public demo exposure
- public demo is treated as a production-like deployment surface
- public documentation may be prepared before demo exposure when it does not expose runtime services
- internal architecture refactoring can be released as a minor version when public contracts remain compatible
- badges are visual indicators only; metadata files remain the source of truth
- roadmap reflects actual implementation state
- cross-repo alignment must respect compatibility metadata
- SDK must remain a client only
- API must remain an orchestration gateway
- Core owns age decision scoring
- AntiSpoof owns presentation attack scoring
- API owns global score aggregation
- model paths must be resolved through model registries, not public runtime config
- thresholds must belong to scoring or calibration policies, not project.json runtime config
- privacy-first behavior must be invariant and not disabled by runtime flags
- ZK-ready / proof-ready behavior is a capability, not a runtime toggle
- docs.credona.dev owns public documentation
- credona.dev owns the public demo experience
</pre>
