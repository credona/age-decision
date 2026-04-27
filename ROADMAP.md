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

repos:
- core
- antispoof
- api
- sdk

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
| model documentation                      | [x]  | [x]       |  -  |  -  | [x]    |
| model binary policy                      | [x]  | [x]       | [x] | [x] | [x]    |
| OpenAPI / contract tests                 | [x]  | [x]       | [x] | [x] | [x]    |
| ZK-ready / proof-ready structure         | [x]  | -         | [x] | [x] | [x]    |
</pre>

<hr>

<h2>Versioning and compatibility</h2>

<pre>
| type  | impact | target | description                        | core | antispoof | api | sdk | status |
|-------|--------|--------|------------------------------------|------|-----------|-----|-----|--------|
| infra | Y      | v2.1.0 | compatibility matrix CI            | [~]  | [~]       | [~] | [~] | [~]    |
| infra | Y      | v2.2.0 | cross-repo integration tests       | [ ]  | [ ]       | [ ] | [ ] | [ ]    |
| infra | Y      | v2.3.0 | regression compatibility CI        | [ ]  | [ ]       | [ ] | [ ] | [ ]    |
| docs  | Z      | v2.x.x | compatibility policy documentation | [~]  | [~]       | [~] | [~] | [~]    |
</pre>

<hr>

<h2>API governance</h2>

<pre>
| type  | impact | target | description                  | core | antispoof | api | sdk | status |
|-------|--------|--------|------------------------------|------|-----------|-----|-----|--------|
| chore | Z      | v2.1.0 | API versioning strategy      | -    | -         | [~] | -   | [~]    |
| chore | Z      | v2.2.0 | deprecation policy           | -    | -         | [ ] | -   | [ ]    |
| chore | Z      | v2.2.0 | backward compatibility rules | [ ]  | [ ]       | [ ] | [ ] | [ ]    |
</pre>

<hr>

<h2>Security baseline</h2>

<pre>
| type  | impact | target | description          | core | antispoof | api | sdk | status |
|-------|--------|--------|----------------------|------|-----------|-----|-----|--------|
| feat  | Y      | v2.2.0 | request validation   | [ ]  | [ ]       | [ ] | -   | [ ]    |
| feat  | Y      | v2.2.0 | rate limiting        | -    | -         | [ ] | -   | [ ]    |
| feat  | Y      | v2.3.0 | payload limits       | -    | -         | [ ] | -   | [ ]    |
| feat  | Y      | v2.3.0 | API authentication   | -    | -         | [ ] | [ ] | [ ]    |
| infra | Y      | v2.3.0 | security test suite  | [ ]  | [ ]       | [ ] | -   | [ ]    |
</pre>

<hr>

<h2>Code quality and tooling</h2>

<pre>
| type  | impact | target | description        | core | antispoof | api | sdk | status |
|-------|--------|--------|--------------------|------|-----------|-----|-----|--------|
| chore | Z      | v2.1.0 | coding standards   | [~]  | [~]       | [~] | [~] | [~]    |
| infra | Z      | v2.1.0 | linters            | [~]  | [~]       | [~] | [~] | [~]    |
| infra | Z      | v2.1.0 | formatters         | [~]  | [~]       | [~] | [~] | [~]    |
| infra | Z      | v2.2.0 | pre-commit hooks   | [ ]  | [ ]       | [ ] | [ ] | [ ]    |
</pre>

<hr>

<h2>Machine learning lifecycle</h2>

<pre>
| type  | impact | target | description              | core | antispoof | api | sdk | status |
|-------|--------|--------|--------------------------|------|-----------|-----|-----|--------|
| feat  | Y      | v2.2.0 | model validation         | [ ]  | [ ]       | -   | -   | [ ]    |
| feat  | Y      | v2.3.0 | model versioning         | [ ]  | [ ]       | -   | -   | [ ]    |
| feat  | Y      | v2.4.0 | multi-model support      | [ ]  | [ ]       | -   | -   | [ ]    |
| feat  | Y      | v2.4.0 | model reproducibility    | [ ]  | [ ]       | -   | -   | [ ]    |
| feat  | Y      | v2.5.0 | calibration              | [ ]  | [ ]       | -   | -   | [ ]    |
</pre>

<hr>

<h2>Scientific transparency</h2>

<pre>
| type  | impact | target | description               | core | antispoof | api | sdk | status |
|-------|--------|--------|---------------------------|------|-----------|-----|-----|--------|
| docs  | Z      | v2.3.0 | dataset transparency      | [ ]  | [~]       | -   | -   | [~]    |
| docs  | Z      | v2.4.0 | benchmark methodology     | [~]  | [~]       | -   | -   | [~]    |
| infra | Y      | v2.5.0 | reproducible benchmarks   | [ ]  | [~]       | -   | -   | [~]    |
</pre>

<hr>

<h2>Infrastructure and deployment</h2>

<pre>
| type  | impact | target | description          | core | antispoof | api | sdk | status |
|-------|--------|--------|----------------------|------|-----------|-----|-----|--------|
| feat  | Y      | v2.4.0 | Kubernetes support   | [ ]  | [ ]       | [ ] | -   | [ ]    |
| docs  | Z      | v2.5.0 | production guide     | [ ]  | [ ]       | [ ] | -   | [ ]    |
</pre>

<hr>

<h2>Developer experience</h2>

<pre>
| type  | impact | target | description            | core | antispoof | api | sdk | status |
|-------|--------|--------|------------------------|------|-----------|-----|-----|--------|
| docs  | Z      | v2.0.0 | SDK usage examples     | -    | -         | -   | [x] | [x]    |
| docs  | Z      | v2.0.0 | API usage examples     | -    | -         | [x] | [x] | [x]    |
</pre>

<hr>

<h2>Trust and proof layer</h2>

<pre>
| type     | impact | target | description                 | core | antispoof | api | sdk | status |
|----------|--------|--------|-----------------------------|------|-----------|-----|-----|--------|
| feat     | X      | v2.0.0 | proof-ready structure       | [x]  | -         | [x] | [x] | [x]    |
| research | X      | TBD    | verifiable claims format    | [~]  | -         | [ ] | [ ] | [ ]    |
| research | X      | TBD    | ZKP feasibility             | -    | -         | [ ] | -   | [ ]    |
| research | X      | TBD    | ZKP prototype               | -    | -         | [ ] | -   | [ ]    |
</pre>

<hr>

<h2>Temporal and liveness evolution</h2>

<pre>
| type  | impact | target | description                    | core | antispoof | api | sdk | status |
|-------|--------|--------|--------------------------------|------|-----------|-----|-----|--------|
| feat  | X      | v3.x.x | image sequence input           | [~]  | [ ]       | [ ] | [ ] | [ ]    |
| feat  | X      | v3.x.x | video liveness                 | [~]  | [ ]       | [ ] | [ ] | [ ]    |
| feat  | X      | v3.x.x | replay resistance              | [~]  | [ ]       | [ ] | [ ] | [ ]    |
| feat  | Y      | v3.x.x | temporal consistency scoring   | [~]  | [ ]       | [ ] | [ ] | [ ]    |
</pre>

<hr>

<h2>Historical context</h2>

<pre>
v1.x.x:
- initial services
- docker setup
- CI/CD
- early SDK
- initial API contract

v2.0.0:
- contract stabilization
- privacy-first design
- score normalization
- ZK-ready architecture
</pre>

<hr>

<h2>Notes</h2>

- priorities may evolve based on feedback and contributors
- roadmap reflects actual implementation state
- cross-repo alignment may trigger coordinated releases
