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

## How to use this template

1. Create a new repository from this template.
2. Replace this README with project-specific documentation.
3. Update `.gitignore` if your stack needs more ignores.
4. Adjust CI once the project language and test tooling are chosen.

## Baseline expectations

- Keep the default branch as `main`.
- Prefer pull requests for non-trivial changes.
- Keep workflows low-permission by default.
- Do not commit secrets. Use `.env.example` files instead of real credentials.
