# Calibration Reporting

Calibration reporting describes how public scores behave on documented datasets.

It does not expose raw model outputs, internal thresholds, score components, or calibration internals.

## Purpose

Calibration reports help evaluate whether public scores are stable, monotonic, and interpretable across benchmark datasets.

## Dataset separation

Calibration and test data must remain separated.

The calibration split is used to define or validate calibration behavior.

The test split is used to report final benchmark behavior.

A report must clearly state which split was used.

## Public score reporting

Only public scores that belong to the public contract may be reported.

For v2.6.0, reports may cover:

- cred_decision_score
- cred_antispoof_score
- cred_global_score

Reports must use aggregate statistics only.

## Monotonicity

A calibration report should verify that stronger model evidence does not produce a weaker public score.

The report must not expose the raw model evidence used to perform this validation.

## Stability

A calibration report should measure whether small input variations produce bounded public score changes.

Examples:

- resize variation
- compression variation
- lighting variation
- deterministic repeated execution

Only aggregate stability metrics may be published.

## Distribution

Reports may include public score distributions.

Allowed examples:

- histogram buckets
- mean
- median
- p95
- public decision distribution

Forbidden examples:

- raw per-sample score list
- raw model outputs
- internal score components
- private thresholds

## Limitations

Every calibration report must describe:

- dataset limitations
- known demographic bias risks
- sample count
- dataset license
- machine characteristics
- benchmark version
- service version
- contract version

## Privacy

Calibration reports must never include images, base64 payloads, raw downstream responses, model paths, internal thresholds, or raw model scores.
