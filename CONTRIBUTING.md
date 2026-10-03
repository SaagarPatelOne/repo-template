# Contributing

Thanks for contributing.

This template is meant for repositories maintained by a solo owner or a small project set, so the default process is intentionally lightweight.

## Local verification

Run from the repository root with Git and Python 3 available. Install `pre-commit` in an isolated Python environment, then run the same hygiene checks as [CI](.github/workflows/ci.yml):

```sh
python3 -m venv .venv
. .venv/bin/activate
python -m pip install --upgrade pip pre-commit
pre-commit run --files CONTRIBUTING.md --show-diff-on-failure
pre-commit run --all-files --show-diff-on-failure
```

On Windows, activate with `.venv\Scripts\Activate.ps1` in PowerShell. Replace `CONTRIBUTING.md` with the files you changed for the focused check. The first run downloads the hooks pinned in [.pre-commit-config.yaml](.pre-commit-config.yaml); an initial run needs network access. Whitespace and line-ending hooks can edit files, so inspect `git diff` and rerun after fixes. Keep the local environment out of commits.

These checks cover file hygiene and syntax, not application behavior. This template has no application test, typecheck, build, or browser suite yet; document those real commands when selecting a stack. Browser verification applies when user-facing behavior is added or changed. Report commands run, results, and any unavailable checks in your pull request.

[Secret Scan](.github/workflows/secret-scan.yml) also checks Git history in CI. With Gitleaks 8.24.2 installed and the full history available, its local equivalent is `gitleaks git --verbose --redact --no-banner .`.

## Before you open a pull request

- Keep the change focused.
- Explain the problem being solved and the expected outcome.
- Include validation notes, even if they are manual.
- Call out risks, tradeoffs, or follow-up work.

## Before you open an issue

- Search for an existing issue first.
- For bugs, include exact reproduction steps and expected behavior.
- For feature requests, explain the problem and the user value.

Repository-specific docs can override this file when a project needs more detail.
