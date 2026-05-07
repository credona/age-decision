# Machine Characteristics

Benchmark results are meaningful only when the execution environment is documented.

## Required metadata

Every benchmark report must include:

- CPU model
- RAM in GB
- GPU model, or empty string if none
- hosting provider
- operating system
- Docker version

## Runtime metadata

Reports should include:

- Docker image name
- Docker image digest, if available
- deterministic seed
- exact benchmark command

## Why this is required

Latency, throughput, and reproducibility depend on the execution environment.

Two benchmark reports should not be compared unless the machine metadata is identical or explicitly discussed.

## Docker

Benchmarks should run through Docker whenever possible.

The preferred execution mode is a documented command such as:

cd ../age-decision-benchmark && scripts/server/run_all_service_contract_benchmarks_local.sh

or a benchmark-specific Docker Compose command.

## Restrictions

Machine metadata must not expose secrets, local private paths, tokens, usernames, or host-specific sensitive information.
