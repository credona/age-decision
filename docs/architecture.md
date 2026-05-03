<h1>Architecture</h1>

Age Decision is built as a small ecosystem of independent services and clients.

Each repository owns a bounded responsibility.

<hr>

<h2>High-level flow</h2>

<pre>
SDK
  -> API gateway
      -> Core
      -> AntiSpoof
  -> response_filter
  -> public response
</pre>

<hr>

<h2>Repositories</h2>

<h3>Age Decision Core</h3>

Core owns:

- face detection
- internal age estimation
- threshold decision
- cred_decision_score
- model registry
- scoring policy
- proof-ready metadata
- privacy metadata

Core must not expose estimated age, raw confidence, raw model scores, or internal thresholds.

<h3>Age Decision AntiSpoof</h3>

AntiSpoof owns:

- still-image presentation attack detection
- real / spoof decision
- cred_antispoof_score
- model registry
- scoring policy
- calibration metadata
- privacy metadata

AntiSpoof must not expose raw logits, spoof score, heuristic internals, or internal threshold values.

<h3>Age Decision API</h3>

API owns:

- public /verify endpoint
- request validation
- downstream orchestration
- normalized decision_check
- normalized spoof_check
- cred_global_score
- global response filtering
- privacy and proof-ready metadata aggregation

API must not expose downstream raw responses.

<h3>Age Decision JS SDK</h3>

SDK owns:

- typed client access
- request mapping
- timeout handling
- retry handling
- standardized error mapping
- response filtering on unsafe payload casting

SDK must remain client-only.

It must not duplicate business scoring or decision logic.

<hr>

<h2>Layering rule</h2>

Python services use this structure:

<pre>
app/
  api/
  application/
  domain/
  infrastructure/
  models/
</pre>

Rules:

- api handles HTTP parsing, headers, error mapping, and response filtering
- application owns use cases and orchestration
- application depends on ports, not infrastructure implementations
- domain contains pure logic only
- infrastructure owns HTTP clients, runtime configuration, logging, and external adapters
- response_filter is the final public contract barrier

<hr>

<h2>Ports</h2>

Downstream dependencies must be expressed as ports.

Examples:

- CoreClientPort
- AntispoofClientPort
- InferenceEnginePort
- InputAnalyzerPort
- ModelRegistryPort

Ports must not contain HTTP implementation details.

<hr>

<h2>Model lifecycle in v2.5</h2>

Core and AntiSpoof use model metadata and registry abstractions.

Model selection must be deterministic.

Public runtime configuration should use stable model identifiers instead of low-level model paths.

Model metadata may include:

- model_id
- model_version
- task
- runtime
- scoring_policy_id
- reproducibility metadata

<hr>

<h2>Scoring ownership</h2>

- Core owns <code>cred_decision_score</code>
- AntiSpoof owns <code>cred_antispoof_score</code>
- API owns <code>cred_global_score</code>
- SDK consumes public scores only

Score logic belongs to versioned scoring policies.

Threshold logic must not be controlled by unsafe runtime flags.

<hr>

<h2>Privacy contract</h2>

Public responses must pass through a response filter.

Never expose:

- raw downstream responses
- internal thresholds
- raw model scores
- base64 images
- decoded image bytes
- image paths
- estimated age
- confidence
- internal exception details

<hr>

<h2>Design principles</h2>

- privacy-first
- deterministic public contract
- explicit orchestration
- strict repository boundaries
- domain purity
- Docker reproducibility
- no hidden coupling
- no duplicated normalization logic
