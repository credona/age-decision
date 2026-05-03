<h1>Scoring</h1>

Age Decision uses separate public scores for separate responsibilities.

Scores are public decision support signals. They are not legal proof, identity proof, biometric proof, or certified compliance results.

<hr>

<h2>Score ownership</h2>

<h3>cred_decision_score</h3>

Produced by Age Decision Core.

It represents the public credibility of the age threshold decision.

It is derived from a versioned scoring policy using public-safe factors such as signal quality category and threshold separation category.

It must not expose:

- estimated age
- raw confidence
- raw model scores
- threshold distance
- internal thresholds

<h3>cred_antispoof_score</h3>

Produced by Age Decision AntiSpoof.

It represents the public credibility of the still-image presentation attack decision.

It is derived from a versioned scoring policy and calibration method.

It must not expose:

- raw logits
- spoof score
- liveness score
- heuristic internals
- internal threshold
- raw calibration details

<h3>cred_global_score</h3>

Produced by Age Decision API.

It represents the public global score after downstream checks are normalized.

The v2.5 policy is conservative:

<pre>
cred_global_score = min(cred_decision_score, cred_antispoof_score)
</pre>

This means the weakest required public signal determines the global score.

<hr>

<h2>Versioned scoring policies</h2>

Each scoring policy must have a stable policy identifier.

Current policy identifiers:

<pre>
credona.age.threshold-margin.v1
credona.antispoof.fusion-threshold.v1
credona.api.global-min-score.v1
</pre>

Policy configuration belongs to domain scoring policy code, not public runtime configuration.

<hr>

<h2>Interpretation</h2>

A high score means the public decision signal is stronger.

A low score means the decision should be treated with caution or routed to a stricter verification flow.

The score should never be used alone.

Recommended inputs for integrators:

- public decision
- public reason
- public score
- privacy metadata
- local regulatory requirements

<hr>

<h2>Removed aliases</h2>

The legacy field <code>cred_score</code> is not part of the public v2.5 contract.

Integrations must use explicit score names:

- <code>cred_decision_score</code>
- <code>cred_antispoof_score</code>
- <code>cred_global_score</code>
