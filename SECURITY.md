# Security Policy

Bomly is security-sensitive software. It scans dependency trees, evaluates
policy, generates SBOMs, and reports findings that downstream systems may rely
on. We take vulnerabilities in Bomly projects seriously and appreciate private,
responsible reports.

## Reporting a Vulnerability

Please do not open a public issue for security vulnerabilities.

Use GitHub Private Vulnerability Reporting from the affected repository's
Security tab. If that channel is unavailable, email <contact@bomly.dev> instead.

When reporting, please include:

- A description of the vulnerability and its impact.
- Steps to reproduce, including a minimal project, command line, workflow
  snippet, or affected input when possible.
- The affected Bomly repository, version, release tag, action ref, or commit.
- Your platform and any relevant sanitized logs.
- Suggested remediation, if you have one.

## What to Expect

- Acknowledgement within 3 business days.
- Initial assessment within 7 business days, including severity and planned
  handling.
- Coordinated fix and disclosure when a vulnerability is confirmed.
- Reporter credit when desired and appropriate.

## Scope

In scope:

- Bomly CLI, SDK, GitHub Action, plugin examples, release artifacts, and
  workflows published by the `bomly-dev` organization.
- Vulnerabilities that allow incorrect trust decisions, unsafe execution,
  credential exposure, artifact tampering, or misleading security output.

Out of scope:

- Vulnerabilities in third-party dependencies; report those upstream unless
  Bomly's handling creates an additional vulnerability.
- Findings produced about your dependencies by a Bomly scan; those describe your
  software, not necessarily a flaw in Bomly.
- Issues that require a compromised local machine or a malicious build of Bomly.
- Test fixture repositories under `examples/` when they intentionally contain
  vulnerable or unusual dependencies for scanner coverage.

## Supported Versions

Security fixes target the latest released version or latest supported major tag
for the affected project unless that repository documents a stricter support
policy. Please upgrade to the most recent release before reporting if you can do
so safely, in case the issue has already been fixed.
