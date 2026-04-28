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

<h2>v2.2.x – Post-release improvements</h2>

<pre>
| type  | impact | target | description                                       | core | antispoof | api | sdk | status |
|-------|--------|--------|---------------------------------------------------|------|-----------|-----|-----|--------|
| infra | Y      | 2.2.1  | pre-commit hooks                                  | [ ]  | [ ]       | [ ] | [ ] | [ ]    |
| infra | Y      | 2.2.1  | pre-push validation                               | [ ]  | [ ]       | [ ] | [ ] | [ ]    |
| infra | Z      | 2.2.1  | test pyproject metadata consistency               | [~]  | [~]       | [~] | -   | [~]    |
| infra | Z      | 2.2.1  | test Docker image metadata consistency            | [ ]  | [ ]       | [ ] | -   | [ ]    |
| docs  | Z      | 2.2.2  | prevent manual drift                              | [ ]  | [ ]       | [ ] | [~] | [~]    |
| docs  | Z      | 2.2.2  | generate changelog sections automatically         | [ ]  | [ ]       | [ ] | [ ] | [ ]    |
| infra | Z      | 2.2.2  | inject changelog content into release description | [ ]  | [ ]       | [ ] | [ ] | [ ]    |
</pre>

<hr>

<h2>v2.3.0 – API governance and security</h2>

<pre>
| type  | impact | target | description                           | core | antispoof | api | sdk | status |
|-------|--------|--------|---------------------------------------|------|-----------|-----|-----|--------|
| feat  | Y      | 2.3.0  | stable status contract                | [ ]  | [ ]       | [ ] | [ ] | [ ]    |
| feat  | Y      | 2.3.0  | standardized error code/message model | [ ]  | [ ]       | [ ] | [ ] | [ ]    |
| feat  | Y      | 2.3.0  | request validation                    | [ ]  | [ ]       | [ ] | -   | [ ]    |
| feat  | Y      | 2.3.0  | rate limiting                         | -    | -         | [ ] | -   | [ ]    |
</pre>

<hr>

<h2>v2.3.1 – Maintenance</h2>

<pre>
| type  | impact | target | description        | core | antispoof | api | sdk | status |
|-------|--------|--------|--------------------|------|-----------|-----|-----|--------|
| chore | Z      | 2.3.1  | deprecation policy | [ ]  | [ ]       | [ ] | [ ] | [ ]    |
</pre>

<hr>

<h2>v2.4.0 – Model lifecycle and transparency</h2>

<pre>
| type  | impact | target | description           | core | antispoof | api | sdk | status |
|-------|--------|--------|-----------------------|------|-----------|-----|-----|--------|
| feat  | Y      | 2.4.0  | model validation      | [ ]  | [ ]       | -   | -   | [ ]    |
| feat  | Y      | 2.4.0  | model versioning      | [ ]  | [ ]       | -   | -   | [ ]    |
| docs  | Z      | 2.4.1  | dataset transparency  | [ ]  | [~]       | -   | -   | [~]    |
| docs  | Z      | 2.4.1  | benchmark methodology | [~]  | [~]       | -   | -   | [~]    |
</pre>

<hr>

<h2>v2.5.0 – Deployment and scalability</h2>

<pre>
| type  | impact | target | description           | core | antispoof | api | sdk | status |
|-------|--------|--------|-----------------------|------|-----------|-----|-----|--------|
| feat  | Y      | 2.5.0  | payload limits        | -    | -         | [ ] | -   | [ ]    |
| feat  | Y      | 2.5.0  | API authentication    | -    | -         | [ ] | [ ] | [ ]    |
| feat  | Y      | 2.5.0  | Kubernetes deployment | [ ]  | [ ]       | [ ] | -   | [ ]    |
| docs  | Z      | 2.5.1  | production guide      | [ ]  | [ ]       | [ ] | -   | [ ]    |
</pre>

<hr>

<h2>v2.6.0 – Advanced ML lifecycle</h2>

<pre>
| type  | impact | target | description             | core | antispoof | api | sdk | status |
|-------|--------|--------|-------------------------|------|-----------|-----|-----|--------|
| feat  | Y      | 2.6.0  | multi-model support     | [ ]  | [ ]       | -   | -   | [ ]    |
| feat  | Y      | 2.6.0  | model reproducibility   | [ ]  | [ ]       | -   | -   | [ ]    |
| feat  | Y      | 2.6.0  | calibration             | [ ]  | [ ]       | -   | -   | [ ]    |
| infra | Y      | 2.6.0  | reproducible benchmarks | [ ]  | [~]       | -   | -   | [~]    |
</pre>

<hr>

<h2>v3.0.0 – Breaking evolution</h2>

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
- only main branch can trigger releases
- version is read from project.json / package.json
- tag vX.Y.Z is created automatically after successful CI on main
- tag triggers:
  - GitHub release
  - Docker image publication
  - npm publication (SDK)

- release description should be generated from CHANGELOG.md
- CHANGELOG.md should become the single source of truth for release notes
</pre>

<hr>

<h2>Notes</h2>

<pre>
- patch versions are strictly internal fixes
- minor versions introduce backward-compatible features
- major versions introduce breaking changes
- badges are visual indicators only; metadata files remain the source of truth
- roadmap reflects actual implementation state
- cross-repo alignment must respect compatibility metadata
</pre>
