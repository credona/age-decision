<h1>Contributing</h1>

Thank you for your interest in contributing to Age Decision.

This repository contains global documentation and project-level coordination.

Code contributions should usually be made in the relevant technical repository.

<hr>

<h2>Repositories</h2>

- Core: age estimation and decision policy
- AntiSpoof: still-image anti-spoofing
- API: public gateway and orchestration
- JS SDK: TypeScript and JavaScript client

<hr>

<h2>Contribution principles</h2>

All contributions should follow these principles:

- privacy-first design
- no unnecessary data persistence
- explicit API contracts
- reproducible behavior
- transparent model and benchmark documentation
- no hidden claims about legal or certified identity verification

<hr>

<h2>Documentation rules</h2>

Documentation should be placed where it belongs:

- global concepts belong in this repository
- repository-specific usage belongs in the related repository
- model details belong in the repository using the model
- benchmark details belong in the repository running the benchmark
- changelogs belong in each technical repository

Avoid duplicating the same explanation across repositories.

<hr>

<h2>Pull request guidelines</h2>

- keep changes focused
- explain why the change is needed
- update documentation when behavior changes
- avoid large unrelated edits
- use clear commit messages

<hr>

<h2>Commit conventions</h2>

Use concise commit messages:

```text
docs: update scoring documentation
feat: add proof-friendly claim format
fix: correct repository link
refactor: simplify documentation structure
chore: update project metadata
```

<hr>

<h2>Scientific and model references</h2>

When adding model, dataset or benchmark claims:

- cite the source
- mention the model or dataset license when known
- separate project validation from upstream benchmark claims
- document limitations clearly

<hr>

<h2>Security and privacy</h2>

Do not publish:

- real user images
- biometric templates
- private datasets
- credentials
- API keys
- internal logs containing sensitive data
