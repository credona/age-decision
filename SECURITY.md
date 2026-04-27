<h1>Security Policy</h1>

Age Decision handles image inputs and inference metadata.

Security and privacy issues should be treated carefully.

<hr>

<h2>Supported scope</h2>

Security reports may concern:

- image handling
- data leakage
- unsafe logging
- exposed secrets
- dependency vulnerabilities
- unsafe Docker configuration
- API error information exposure
- request tracing issues
- response contract leaks

<hr>

<h2>Privacy expectations</h2>

The system should not:

- persist uploaded images by default
- store biometric templates
- log raw images
- log base64 payloads
- expose internal exceptions to public clients
- expose downstream internals unless explicitly configured

<hr>

<h2>Reporting</h2>

Open a private security advisory on the relevant GitHub repository when possible.

If the issue affects the full ecosystem, report it from this central repository.

<hr>

<h2>Responsible disclosure</h2>

Please provide:

- affected repository
- affected endpoint or component
- reproduction steps
- expected impact
- suggested mitigation if available

Do not publish exploit details publicly before maintainers have had time to investigate.

<hr>

<h2>Dependency security</h2>

The project uses automated dependency scanning and CodeQL where applicable.

Security updates are handled in the repository affected by the dependency.
