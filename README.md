# repo-template

This repository is the default starter template for projects in the `SaagarPatelOne` organization.

It is intentionally language-agnostic and includes a practical baseline:

- a concise project README structure
- contribution and security guidance
- a CODEOWNERS file
- editor and file hygiene defaults
- Dependabot for GitHub Actions
- a minimal CI workflow
- a dedicated secret scanning workflow
- local pre-commit checks

## When to choose this template

Use this template when the repository does not clearly belong to one of the more specific starters:

- `service-template` for apps, APIs, and runtime services
- `library-template` for reusable packages and shared modules
- `infra-template` for infrastructure, environments, and operations automation

## How to use this template

1. Create a new repository from this template.
2. Replace this README with project-specific documentation.
3. Update `.gitignore` if your stack needs more ignores.
4. Adjust CI once the project language and test tooling are chosen.

If a repository is created outside the ideal path, reconcile it with the baseline using:

- `bootstrap-gh-repo <repo-name> --template SaagarPatelOne/repo-template`
- `harden-gh-repo SaagarPatelOne/<repo-name>`

## Baseline expectations

- Keep the default branch as `main`.
- Prefer pull requests for non-trivial changes.
- Keep workflows low-permission by default.
- Do not commit secrets. Use `.env.example` files instead of real credentials.
