# Model Comparison

Model comparison must be deterministic, reproducible, and privacy-safe.

## Comparison rules

Models may be compared only when the report declares:

- same benchmark_version
- same contract_version
- same dataset or documented dataset difference
- same dataset split
- same machine or documented machine difference
- same benchmark target
- same deterministic seed policy

## Comparable metrics

Allowed metrics include:

- latency
- throughput
- public decision distribution
- aggregate public score distribution
- stability metrics
- calibration metrics
- reproducibility status

## Forbidden metrics

Reports must not expose:

- raw model scores
- confidence
- estimated_age
- internal thresholds
- internal margins
- score components
- model paths
- downstream raw responses

## Model identifiers

Reports may use stable model identifiers.

Reports must not expose runtime model paths.

## Interpretation

A faster model is not automatically better.

A model comparison must distinguish:

- latency
- stability
- calibration behavior
- public decision consistency
- documented dataset limitations

## Public communication

Model comparison reports must avoid absolute claims.

Age Decision produces probabilistic decisions, not legal age proof.
