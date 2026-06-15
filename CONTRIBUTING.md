# Contributing to Bomly

Thanks for helping improve Bomly.

By participating in Bomly projects, you agree to follow our
[Code of Conduct](CODE_OF_CONDUCT.md). To report a security vulnerability,
follow the [Security Policy](SECURITY.md) instead of opening a public issue.

## Project Focus

- `bomly-cli` is the main command-line tool and SDK. Changes there usually need
  Go tests and user-facing docs when behavior changes.
- `bomly-guard` is the GitHub Action wrapper around `bomly diff`. Changes there
  usually need shell, JavaScript, and action behavior checks.
- `bomly-plugin-*` repositories are example extensions that show how to build
  detectors, matchers, and auditors on the public Bomly SDK.
- Repositories under `examples/` are test fixtures. They may intentionally keep
  unusual dependency state for scanner coverage.

Each repository may have a local `CONTRIBUTING.md` with setup, testing, release,
or architecture details. Follow the local guide when it exists.

## Before Opening an Issue

- Search existing issues and discussions first.
- Use security reporting for vulnerabilities or sensitive findings.
- Include the affected repository, version or commit, platform, command or
  workflow snippet, and enough detail to reproduce the behavior.
- For Bomly CLI scans, include `bomly version` and relevant sanitized output.
- For Bomly Guard, include the action ref, event type, workflow snippet, and
  sanitized action logs.

## Pull Requests

- Keep changes focused and describe the user-visible effect.
- Add or update tests for new behavior and bug fixes.
- Update docs, examples, action inputs, or generated references when behavior
  changes.
- Prefer clear Conventional Commit-style titles such as `fix: handle empty SBOM
  input`, `feat: add detector selector`, or `docs: clarify Guard permissions`.
- Do not include secrets, credentials, private logs, or customer data in issues,
  pull requests, tests, or fixtures.

## Validation

Run the checks that match the repository you changed. Common examples:

- Bomly CLI: `make test`, plus `make smoke` when detector, matcher, auditor, or
  analyzer behavior changes.
- Bomly Guard: `npm run lint:shell`, `npm run lint:js`, and `npm test`.
- Plugin examples: `go test ./...` and the repository build command.

If a check cannot run locally, note why in the pull request.

## Documentation

Bomly is a developer tool, so docs are part of the product. Update README files,
CLI docs, action examples, plugin guides, and generated references when behavior
or public interfaces change.
