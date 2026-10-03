# echorec-startup

**An Echorec sample repository for team shape B — ship-daily startup.** Echorec's acceptance suite
runs that shape's flows against this repository: its agents open pull requests here, CI checks
them, and a human code owner approves every merge.

The code is deliberately small: `stockroom`, a stock ledger in `src/stockroom/`.

## Commands

- tests: `pytest -q`
- lint: `ruff check . && ruff format --check .`
- security scan: `bandit -q -r src`

The same commands run in CI (workflow `ci`) and in Echorec's run sandbox, built from
`.echorec/Dockerfile` (non-root; `.devcontainer/devcontainer.json` uses the same file).

## Rules

- `main` is protected: a pull request, one approving review from a code owner, and passing
  `ci` checks. No force pushes.
- Nothing here is secret, and nothing secret may be added.
