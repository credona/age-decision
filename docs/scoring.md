<h1>Scoring</h1>

Age Decision uses separate scores for separate responsibilities.

This avoids ambiguity and makes it easier to understand which part of the system produced a given trust signal.

<hr>

<h2>Score fields</h2>

<h3>cred_decision_score</h3>

Produced by Age Decision Core.

It represents the reliability of the age decision based on available model confidence and the distance from the configured threshold.

<h3>cred_antispoof_score</h3>

Produced by Age Decision AntiSpoof.

It represents the confidence that the submitted image looks like a real capture rather than a spoof attempt.

<h3>cred_global_score</h3>

Produced by Age Decision API.

It represents the final verification confidence after combining age and anti-spoof signals.

The current conservative aggregation strategy uses the weakest required score.

<hr>

<h2>Compatibility aliases</h2>

Some repositories may temporarily expose `cred_score` for backward compatibility.

New integrations should prefer explicit score names:

- `cred_decision_score`
- `cred_antispoof_score`
- `cred_global_score`

<hr>

<h2>Interpretation</h2>

Scores are not legal proof, identity proof or mathematical proof.

They are machine-readable decision support signals.

A low score means the decision should be treated with caution or routed to a stricter verification path.

<hr>

<h2>Recommended usage</h2>

Integrators should combine:

- final decision
- global score
- rejection reason
- privacy metadata
- local regulatory requirements

The score should not be used alone.
