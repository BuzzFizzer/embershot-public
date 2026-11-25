# Security Policy

## Local-First Security Architecture

Embershot processes all screenshots, annotations, redactions, chroma removals, Encrypted Private Vault items (`PBKDF2-SHA256` + `AES-256-GCM`), and 9-format file exports locally inside the browser under Manifest V3 Content Security Policy (`script-src 'self'; object-src 'self'`).

## Supported Versions

| Version | Supported |
| :--- | :--- |
| `1.6.x` (Latest) | Yes |
| `< 1.6.0` | Upgrade to latest release |

## Reporting a Vulnerability

Please **do not** post exploitable security vulnerabilities in public GitHub issues.

- Use GitHub's **Report a vulnerability** (Private Vulnerability Reporting) tab on [https://github.com/BuzzFizzer/embershot-public/security](https://github.com/BuzzFizzer/embershot-public/security), or open a minimal contact request without exploit details if private reporting is unavailable.
- Include affected browser/version, extension version, and clear reproduction steps. We aim to acknowledge reports within 72 hours.
