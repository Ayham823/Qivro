# Source-release readiness checklist

Qivro's public repository is a **showcase of engineering work**, not a source-code release. Do not flip any source repository from private to public simply because this checklist exists.

## Before publishing any source repository

- [ ] Confirm current tree **and full reachable Git history** are free from API keys, access tokens, certificates, private `.env` files, backup exports, logs, credentials, student/customer data, and copyrighted third-party files.
- [ ] Run a dedicated secret scanner on the entire commit history (for example, Gitleaks or git-secrets). Revoke/rotate anything ever exposed; rewriting history alone is insufficient.
- [ ] Check dependency vulnerabilities and license obligations; remove unnecessary generated assets and oversized binaries.
- [ ] Verify that public screenshots use synthetic users/listings, redact IDs and location/identity data if needed.
- [ ] Add a safe `.env.example` and documented local setup; do not point to private infrastructure or internal credentials.
- [ ] Ensure `README.md` matches current code, commands, service names, and ports.
- [ ] Run available lint, typecheck, tests, build, and local smoke checks against the **exact release commit**.
- [ ] Identify modules that are implemented, mocked, provider-dependent, or planned.
- [ ] Review admin/backend authorization, default credentials, data access, rate limiting, and externally accessible endpoints.
- [ ] Decide on a license intentionally; do not assume the showcase license covers future code releases.
- [ ] Publish only after human review and approval, and link from this showcase to the actual public repository.

## Portfolio alternatives while source is private

The public [screenshots](screenshots/), [architecture](ARCHITECTURE.md), and [implementation status](PROJECT_STATUS.md) provide verifiable documentation without exposing sensitive source files. A sanitized short video of the local environment would improve the portfolio; no such recording is claimed here.
