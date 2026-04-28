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
- core
- antispoof
- api
- sdk

current versions:
- core: 2.1.1
- antispoof: 2.1.0
- api: 2.1.0
- sdk: 2.1.0

status:
- [ ] planned
- [~] in progress / partial
- [x] completed
- [!] blocked
- -   not applicable
</pre>

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

<h2>v2.2.0 – Developer workflow and release automation</h2>

<pre>
| type  | impact | target | description                                          | core | antispoof | api | sdk | status |
|-------|--------|--------|------------------------------------------------------|------|-----------|-----|-----|--------|
| infra | Y      | 2.2.0  | one-command local check                              | [ ]  | [ ]       | [ ] | [ ] | [ ]    |
| infra | Y      | 2.2.0  | one-command release preparation                      | [ ]  | [ ]       | [ ] | [ ] | [ ]    |
| infra | Y      | 2.2.0  | pre-commit hooks                                     | [ ]  | [ ]       | [ ] | [ ] | [ ]    |
| infra | Y      | 2.2.0  | pre-push validation                                  | [ ]  | [ ]       | [ ] | [ ] | [ ]    |
| infra | Y      | 2.2.0  | update-all script                                    | [ ]  | [ ]       | [ ] | [ ] | [ ]    |
| infra | Y      | 2.2.0  | check-all script                                     | [ ]  | [ ]       | [ ] | [ ] | [ ]    |
| infra | Y      | 2.2.0  | automatic release tagging from metadata after main CI| [ ]  | [ ]       | [ ] | [ ] | [ ]    |
| infra | Y      | 2.2.0  | tag-triggered GitHub release workflow                | [ ]  | [ ]       | [ ] | [ ] | [ ]    |
| infra | Y      | 2.2.0  | tag-triggered Docker image workflow                  | [ ]  | [ ]       | [ ] | -   | [ ]    |
| infra | Y      | 2.2.0  | tag-triggered npm publish workflow                   | -    | -         | -   | [ ] | [ ]    |
| infra | Y      | 2.2.0  | block push on CI-equivalent failures                 | [ ]  | [ ]       | [ ] | [ ] | [ ]    |
</pre>

<hr>

<h2>v2.2.x – Documentation and changelog automation</h2>

<pre>
| type | impact | target | description                                      | core | antispoof | api | sdk | status |
|------|--------|--------|--------------------------------------------------|------|-----------|-----|-----|--------|
| docs | Z      | 2.2.1  | automate docs generation                         | [ ]  | [ ]       | [ ] | [ ] | [ ]    |
| docs | Z      | 2.2.1  | enforce generated blocks                         | [ ]  | [ ]       | [ ] | [ ] | [ ]    |
| docs | Z      | 2.2.2  | prevent manual drift                             | [ ]  | [ ]       | [ ] | [ ] | [ ]    |
| docs | Z      | 2.2.2  | generate changelog sections automatically        | [ ]  | [ ]       | [ ] | [ ] | [ ]    |
| infra| Z      | 2.2.2  | inject changelog content into release description| [ ]  | [ ]       | [ ] | [ ] | [ ]    |
</pre>

<hr>

<h2>v2.2.x – Metadata and package validation</h2>

<pre>
| type  | impact | target | description                                      | core | antispoof | api | sdk | status |
|-------|--------|--------|--------------------------------------------------|------|-----------|-----|-----|--------|
| infra | Z      | 2.2.1  | test project.json version consistency            | [ ]  | [ ]       | [ ] | [x] | [~]    |
| infra | Z      | 2.2.1  | test package.json version consistency            | -    | -         | -   | [ ] | [ ]    |
| infra | Z      | 2.2.1  | test pyproject metadata consistency              | [ ]  | [ ]       | [ ] | -   | [ ]    |
| infra | Z      | 2.2.2  | test Docker image metadata consistency           | [ ]  | [ ]       | [ ] | -   | [ ]    |
| infra | Z      | 2.2.2  | test release tag against metadata                | [ ]  | [ ]       | [ ] | [ ] | [ ]    |
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
| chore | Z      | 2.3.1  | deprecation policy                    | [ ]  | [ ]       | [ ] | [ ] | [ ]    |
</pre>

<hr>

<h2>v2.4.0 – Model lifecycle and transparency</h2>

<pre>
| type  | impact | target | description              | core | antispoof | api | sdk | status |
|-------|--------|--------|--------------------------|------|-----------|-----|-----|--------|
| feat  | Y      | 2.4.0  | model validation         | [ ]  | [ ]       | -   | -   | [ ]    |
| feat  | Y      | 2.4.0  | model versioning         | [ ]  | [ ]       | -   | -   | [ ]    |
| docs  | Z      | 2.4.1  | dataset transparency     | [ ]  | [~]       | -   | -   | [~]    |
| docs  | Z      | 2.4.1  | benchmark methodology    | [~]  | [~]       | -   | -   | [~]    |
</pre>

<hr>

<h2>v2.5.0 – Advanced ML lifecycle</h2>

<pre>
| type  | impact | target | description              | core | antispoof | api | sdk | status |
|-------|--------|--------|--------------------------|------|-----------|-----|-----|--------|
| feat  | Y      | 2.6.0  | multi-model support      | [ ]  | [ ]       | -   | -   | [ ]    |
| feat  | Y      | 2.6.0  | model reproducibility    | [ ]  | [ ]       | -   | -   | [ ]    |
| feat  | Y      | 2.6.0  | calibration              | [ ]  | [ ]       | -   | -   | [ ]    |
| infra | Y      | 2.6.0  | reproducible benchmarks  | [ ]  | [~]       | -   | -   | [~]    |
</pre>

<hr>

<h2>v2.6.0 – Deployment and scalability</h2>

<pre>
| type  | impact | target | description             | core | antispoof | api | sdk | status |
|-------|--------|--------|-------------------------|------|-----------|-----|-----|--------|
| feat  | Y      | 2.5.0  | payload limits          | -    | -         | [ ] | -   | [ ]    |
| feat  | Y      | 2.5.0  | API authentication      | -    | -         | [ ] | [ ] | [ ]    |
| feat  | Y      | 2.5.0  | Kubernetes deployment   | [ ]  | [ ]       | [ ] | -   | [ ]    |
| docs  | Z      | 2.5.1  | production guide        | [ ]  | [ ]       | [ ] | -   | [ ]    |
</pre>

<hr>

<h2>v3.0.0 – Breaking evolution</h2>

<pre>
| type  | impact | target | description              | core | antispoof | api | sdk | status |
|-------|--------|--------|--------------------------|------|-----------|-----|-----|--------|
| feat  | X      | 3.0.0  | image sequence input     | [ ]  | [ ]       | [ ] | [ ] | [ ]    |
| feat  | X      | 3.0.0  | video liveness           | [ ]  | [ ]       | [ ] | [ ] | [ ]    |
| feat  | X      | 3.0.0  | temporal scoring         | [ ]  | [ ]       | [ ] | [ ] | [ ]    |
| feat  | X      | 3.0.0  | replay attack resistance | [ ]  | [ ]       | [ ] | [ ] | [ ]    |
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

- release description must be automatically generated from CHANGELOG.md
- CHANGELOG.md must be the single source of truth for release notes
</pre>

<hr>

<h2>Notes</h2>

- patch versions are strictly internal fixes
- minor versions introduce backward-compatible features
- major versions introduce breaking changes
- roadmap reflects actual implementation state
- cross-repo alignment must respect compatibility metadata
