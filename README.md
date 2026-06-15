# Bomly org community files

This repository provides default community-health files for public repositories
under the `bomly-dev` organization.

GitHub uses these files as fallbacks for repositories that do not define their
own local versions:

- `profile/README.md` renders on the organization profile.
- `CODE_OF_CONDUCT.md`, `CONTRIBUTING.md`, `SECURITY.md`, and `SUPPORT.md`
  describe shared project expectations.
- `ISSUE_TEMPLATE/` and `pull_request_template.md` provide default issue and
  pull request forms.

Repository-specific guidance should stay in the repository that needs it. For
example, `bomly-cli` and `bomly-guard` keep local `CONTRIBUTING.md` files for
their build, test, and release workflows, while inheriting shared conduct,
security, issue, and pull request defaults from this repository.
