# Dataset Usage

Age Decision benchmarks rely on external datasets.

Datasets are not bundled by default.

## Dataset declaration

Every benchmark report must declare:

- dataset name
- dataset version
- dataset source reference
- dataset license
- dataset split
- sample count
- known limitations

## Dataset splits

The recommended split policy is:

- calibration
- test

The calibration split is used for calibration behavior.

The test split is used for final benchmark reporting.

The same samples must not be used to both calibrate and report final results.

## Allowed usage

A dataset may be used only if its license allows the intended benchmark usage.

The benchmark report must reference the license.

## Limitations

Dataset documentation must describe known limitations, including:

- collection conditions
- image quality constraints
- demographic imbalance
- geographic bias
- device bias
- label uncertainty
- spoof presentation limits, if relevant

## Privacy

Benchmark reports must not contain dataset samples.

Forbidden content includes:

- images
- image paths when they reveal private data
- base64 payloads
- biometric data
- per-sample private records

## Reproducibility

A benchmark must provide enough dataset metadata to reproduce the evaluation, without redistributing data illegally.

When a dataset cannot be redistributed, the report must describe how an authorized evaluator can obtain it.
