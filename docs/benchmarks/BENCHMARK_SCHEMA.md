# Benchmark Report Schema

Benchmark reports are public artifacts.

They must be deterministic, sanitized, and schema-validated.

## Schema location

The canonical schema is:

schemas/benchmark-report.schema.json

## Required fields

A benchmark report must include:

- benchmark_id
- benchmark_version
- generated_at
- service
- service_version
- contract_version
- benchmark_target
- dataset
- machine
- runtime
- metrics
- privacy

## Services

Allowed service values:

- core
- antispoof
- api

Decision distributions must follow the public decision vocabulary of the benchmarked service.

## Benchmark targets

Allowed benchmark_target values:

- model
- service
- end_to_end

## Dataset metadata

Dataset metadata must describe the benchmark input set without embedding the dataset.

Required fields:

- name
- version
- split
- sample_count
- license
- source_reference

Allowed split values:

- calibration
- test
- validation

## Machine metadata

Machine metadata must describe the execution environment.

Required fields:

- CPU
- RAM in GB
- GPU, or empty string if none
- hosting provider
- OS
- Docker version

## Runtime metadata

Runtime metadata must describe how the benchmark was executed.

Required fields:

- Docker image
- Docker image digest, if available
- deterministic seed
- command

## Metrics

Metrics must be aggregate-only.

Required fields:

- average latency in milliseconds
- p95 latency in milliseconds
- throughput in requests per second
- public decision distribution using service-specific public decisions

## Privacy metadata

The privacy object must explicitly confirm that the report contains no sensitive or internal data.

The following values must always be false:

- contains_sensitive_data
- contains_raw_inputs
- contains_internal_scores
- contains_internal_thresholds

## Forbidden data

Benchmark reports must not include:

- estimated_age
- confidence
- raw_scores
- thresholds
- model_path
- image
- payload
- downstream_response

The schema forbids unknown fields through additionalProperties=false at every object level.
