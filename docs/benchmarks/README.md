# Benchmarks

Age Decision v2.6.0 introduces benchmark, calibration reporting, and reproducibility documentation.

The goal is to make model and service behavior measurable without exposing sensitive data or internal implementation details.

## Scope

Benchmarks cover:

- core model execution
- antispoof model execution
- core service execution
- antispoof service execution
- end-to-end API execution
- report generation
- reproducibility validation

## Privacy rules

Benchmark outputs must never expose:

- estimated age
- confidence
- raw scores
- internal thresholds
- score components
- raw images
- base64 payloads
- biometric data
- downstream raw responses
- model paths
- calibration internals

Benchmark reports may expose only sanitized aggregate metrics.

## Benchmark targets

### Model benchmark

A model benchmark measures inference behavior outside the HTTP service layer.

It may measure:

- execution latency
- deterministic output stability
- public decision distribution
- aggregate score distribution only when part of the public contract

### Service benchmark

A service benchmark measures the full service pipeline.

It may include:

- input validation
- image decoding
- preprocessing
- inference
- public decision generation
- response filtering

### End-to-end benchmark

An end-to-end benchmark measures the public API flow.

Expected path:

SDK client → API → core and antispoof → public response

The benchmark must validate that no internal field is propagated.

## Reproducibility

Every benchmark report must include:

- benchmark version
- service version
- contract version
- dataset reference
- dataset split
- machine characteristics
- Docker runtime metadata
- deterministic seed
- exact command used

## Output format

Benchmark reports must follow:

schemas/benchmark-report.schema.json

Reports that do not match the schema must be rejected.
