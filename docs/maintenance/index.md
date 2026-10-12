# OctoBot-Evaluators: portable verification records

These records retain exact commands, outcomes, original-log hashes and available source snapshots. Failed, interrupted and earlier exploratory commands remain visible. A later focused pass proves only its own scope.

[Machine-readable records](verification.json) · [Validation](../validation.md) · [Engineering guide](../ayu-develop.md)

Original logs remain in the workspace maintenance evidence. Tracked source hashes exclude untracked additions and later edits, as stated in each captured snapshot.

| Check | Exit | Duration | Command |
| --- | ---: | ---: | --- |
| build | 0 | 1.04s | `uv build --python 3.14` |
| compile | 0 | 0.13s | `<workspace>/OctoBot-Evaluators/.venv/bin/python -m compileall -q src` |
| directory-resource-sync | 0 | 0.77s | `uv sync --all-extras --python 3.14.8` |
| final-build-2 | 0 | 0.89s | `uv build --python 3.14.8` |
| final-build | 0 | 1.25s | `uv build --python 3.14.8` |
| final-compile-2 | 0 | 0.07s | `.venv/bin/python -m compileall -q src` |
| final-compile | 0 | 0.07s | `.venv/bin/python -m compileall -q src` |
| final-existing-tests-2 | 0 | 1.39s | `.venv/bin/python -m pytest tests` |
| final-existing-tests | 2 | 1.13s | `.venv/bin/python -m pytest tests` |
| final-lock-2 | 0 | 0.41s | `uv lock --upgrade` |
| final-lock | 0 | 0.25s | `uv lock --upgrade` |
| final-sync-2 | 0 | 0.56s | `uv sync --all-extras --frozen --python 3.14.8` |
| final-sync | 0 | 0.08s | `uv sync --all-extras --frozen --python 3.14.8` |
| local-manager-sync | 0 | 1.85s | `uv sync --all-extras --python 3.14` |
| lock-3.14 | 0 | 0.88s | `uv lock --upgrade --python 3.14` |
| lock-3.15 | 0 | 1.37s | `uv lock --upgrade --python 3.15` |
| public-manager-sync | 0 | 1.12s | `uv sync --all-extras --python 3.14` |
| compile | 0 | 0.05s | `.venv/bin/python -Werror -m compileall -q src` |
| sync | 0 | 1.36s | `uv sync --all-extras --frozen --python 3.15.0` |
| build | 0 | 0.94s | `uv build --python 3.15.0` |
| compile | 0 | 0.13s | `/tmp/octobot-evaluators-final315-control/bin/python -Werror -m compileall -q src` |
| lock | 0 | 0.13s | `uv lock` |
| sync | 0 | 0.78s | `uv sync --all-extras --frozen --python 3.15.0` |
| tests | 0 | 3.52s | `/tmp/octobot-evaluators-final315-control/bin/python -m pytest tests --tb=short` |
| sync-3.14 | 0 | 1.37s | `uv sync --all-extras --python 3.14` |
| sync-3.15 | 2 | 0.04s | `uv sync --all-extras --python 3.15` |
| tests-2 | 1 | 8.46s | `.venv/bin/python -m pytest tests` |
| tests-3 | 2 | 2.19s | `.venv/bin/python -m pytest tests` |
| tests-4 | 2 | 2.16s | `.venv/bin/python -m pytest tests` |
| tests-5 | 2 | 2.15s | `.venv/bin/python -m pytest tests` |
| tests-6 | 1 | 3.34s | `.venv/bin/python -m pytest tests` |
| tests | 2 | 2.39s | `<workspace>/OctoBot-Evaluators/.venv/bin/python -m pytest tests` |
| updated-manager-sync | 0 | 0.61s | `uv sync --all-extras --python 3.14` |
