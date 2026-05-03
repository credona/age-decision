<h1>Privacy</h1>

Age Decision is designed around privacy-first processing.

This does not remove all risk. It means sensitive data handling is explicit, minimized, and tested.

<hr>

<h2>Privacy goals</h2>

- avoid storing raw images
- avoid storing biometric templates
- avoid logging image contents
- avoid exposing downstream internals
- keep processing ephemeral where possible
- expose only normalized public response structures
- enforce public response filtering before returning data

<hr>

<h2>Data handling model</h2>

Uploaded images are intended to be processed in memory by the relevant service.

The API gateway orchestrates requests and must not persist uploaded content.

Core and AntiSpoof own inference.

The API owns orchestration and global decision aggregation.

The SDK only consumes the public API contract.

<hr>

<h2>Public response policy</h2>

Public responses must not expose:

- estimated age
- raw confidence
- raw model scores
- internal thresholds
- threshold distance
- downstream raw responses
- raw payloads
- image bytes
- image paths
- base64 payloads

Allowed public response fields include:

- public decision
- public reason
- public Credona scores when part of the contract
- spoof_check_required
- normalized public structures
- privacy metadata
- proof-ready metadata

<hr>

<h2>Logging policy</h2>

Logs must contain operational metadata only.

Allowed log fields:

- request_id
- correlation_id
- event
- public decision
- public reason codes
- sanitized error codes

Forbidden log fields:

- raw image bytes
- image paths
- base64 payloads
- raw payloads
- estimated age
- confidence
- internal scores
- internal thresholds
- downstream raw responses
- unfiltered metadata
- full downstream exception traces

Every Python service handling sensitive data must include privacy-safe log tests.

<hr>

<h2>What the system does not do</h2>

Age Decision does not provide:

- identity verification
- face recognition
- document verification
- legal age proof
- certified KYC workflow

<hr>

<h2>Integrator responsibility</h2>

Deployers must ensure that reverse proxies, object storage, external logs, tracing tools, metrics systems, and monitoring systems do not persist sensitive user data unintentionally.
