<h1>Privacy</h1>

Age Decision is designed around privacy-first processing.

This does not mean the system removes all risk. It means the architecture avoids unnecessary persistence and keeps sensitive data handling explicit.

<hr>

<h2>Privacy goals</h2>

- avoid storing raw images
- avoid storing biometric templates
- avoid logging image contents
- avoid exposing downstream internals by default
- keep processing ephemeral where possible
- make response metadata explicit

<hr>

<h2>Data handling model</h2>

Uploaded images are intended to be processed in memory by the relevant service.

The API gateway orchestrates requests and should not persist uploaded content.

Technical repositories may expose privacy metadata to make this behavior visible to integrators.

<hr>

<h2>What the system does not do</h2>

Age Decision does not provide:

- identity verification
- face recognition
- document verification
- legal age proof
- certified KYC workflow

<hr>

<h2>Logging policy</h2>

Logs should contain operational metadata only.

Allowed examples:

- request_id
- correlation_id
- decision
- score values
- rejection reason
- latency
- service name

Forbidden examples:

- raw image bytes
- base64 payloads
- biometric embeddings
- private file paths
- full downstream exception traces in public responses

<hr>

<h2>Integrator responsibility</h2>

Deployers must ensure that reverse proxies, object storage, external logs and monitoring systems do not persist sensitive user data unintentionally.
