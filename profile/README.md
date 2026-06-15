# Bomly

Bomly builds open source tools for understanding dependency risk before it
lands in production.

## Projects

- [Bomly CLI](https://github.com/bomly-dev/bomly-cli) scans source trees,
  SBOMs, Git refs, and container images; generates SPDX and CycloneDX SBOMs;
  enriches packages with vulnerability and license data; evaluates policy; and
  diffs dependency state across refs.
- [Bomly Guard](https://github.com/bomly-dev/bomly-guard) is the official
  GitHub Action for pull request dependency review. It wraps `bomly diff`,
  writes job summaries, can comment on pull requests, uploads SARIF when
  supported, and fails checks when policy is not met.
- Example plugin repositories show how to extend Bomly with external detectors,
  matchers, and auditors without forking the CLI.

## Get Started

Install the CLI:

```bash
go install github.com/bomly-dev/bomly-cli/cmd/bomly@latest
```

Scan a project:

```bash
bomly scan --path . --enrich --audit
```

Add Bomly Guard to a workflow:

```yaml
- uses: bomly-dev/bomly-guard@v1
  with:
    fail-on: high
```

## Learn More

- CLI docs: [github.com/bomly-dev/bomly-cli/tree/main/docs](https://github.com/bomly-dev/bomly-cli/tree/main/docs)
- Guard action: [github.com/marketplace/actions/bomly-guard](https://github.com/marketplace/actions/bomly-guard)
- Project site and docs: [bomly.dev](https://bomly.dev)

Issues, feature requests, and contributions are welcome. Please read the shared
[contributing guide](https://github.com/bomly-dev/.github/blob/main/CONTRIBUTING.md)
and report security issues privately through the affected repository's Security
tab.
