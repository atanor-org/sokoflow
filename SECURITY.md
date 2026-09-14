# Security Policy

SokoFlow handles **fiscal documents and financial data**. Security is not a
feature — it is the product. Purely deterministic, auditable software, and we
expect nobody to cut corners here.

## Supported versions

| "Product version | Supported |
|---|---|
| 0.x (pre-release / MVP) | Not supported — pre-production |
| 1.x and above | Supported |

We are pre-1.0. Until the first certified stable release, treat SokoFlow as
**not for use with real fiscal data** without an explicit go-live from the
maintainers.

## Reporting a vulnerability

Please do **not** open a public issue for security problems.

Report privately:

- GitHub private vulnerability reporting:
  **https://github.com/atanor-org/sokoflow/security/advisories/new**
- Or email the maintainers via a GitHub security advisory / private note

We commit to:

- Acknowledging all reports within 48 hours
- Keeping reporters informed about fixes and disclosure timing
- Coordinated disclosure — no public disclosure until a fix is released

## Scope

This reporting policy covers the `sokoflow` repository and its released
artifacts. Anything related to real tax-authority integrations (RRA EBM,
KRA eTIMS, URA EFRIS) is especially in scope — if you can see a way a billed
transaction could be processed, transmitted, or logged incorrectly, we want
to hear about it.