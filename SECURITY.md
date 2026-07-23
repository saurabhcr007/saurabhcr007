# Security Policy

## Supported Versions

This is a GitHub Profile README repository. There is no application code, versioned releases, or deployed services. The security policy applies to the repository content itself.

## Reporting a Security Concern

If you discover any of the following in this repository, please report it immediately:

- **Exposed credentials** — API keys, tokens, passwords, or secrets accidentally committed
- **Personal Information leaks** — email addresses, phone numbers, or private data that should not be public
- **Malicious content** — SVGs, HTML, or JavaScript that could be used for XSS or tracking
- **Supply chain risks** — third-party actions or scripts with compromised dependencies

## How to Report

**Do NOT open a public GitHub Issue** for security concerns.

Instead, use one of the following:

1. **GitHub Private Vulnerability Reporting** — Use the [Security tab → Report a vulnerability](../../security/advisories/new) on this repository
2. **Email** — Contact the maintainer directly via the email in the GitHub profile

## Response Timeline

| Step | Timeline |
|------|----------|
| Acknowledgement | Within 48 hours |
| Initial assessment | Within 5 business days |
| Fix & disclosure | Within 14 days (for minor issues) |

## Security Best Practices Applied in This Repository

- ✅ No secrets, API keys, or tokens committed
- ✅ No executable code (scripts are documentation-only)
- ✅ GitHub Actions use pinned versions (`@v3`, `@v4`, `@latest`)
- ✅ All external SVG services use HTTPS
- ✅ No tracking pixels or hidden analytics
- ✅ No third-party JavaScript embedded
- ✅ `METRICS_TOKEN` stored as encrypted GitHub Secret (not in code)

## Dependency Security

GitHub Actions dependencies:
- `actions/checkout@v4` — Official GitHub action
- `Platane/snk@v3` — CNCF-listed, widely audited contribution snake generator
- `lowlighter/metrics@latest` — Popular open-source metrics generator
- `stefanzweifel/git-auto-commit-action@v5` — Widely used auto-commit action

All actions are reviewed before use. Pin to specific commit SHAs for production-hardened setups.
