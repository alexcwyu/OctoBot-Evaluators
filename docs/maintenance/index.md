# OctoBot-Evaluators: portable verification records

Full raw logs are retained in the workspace maintenance evidence, not distributed here. Hashes identify those original logs. A successful build or selected test subset does not imply a full test-suite pass. Commands containing <workspace> describe the original execution environment.

[Machine-readable records](verification.json) · [Repository validation summary](../validation.md)

## Executed commands

| Check | Exit | Duration | Command | Outcomes |
| --- | ---: | ---: | --- | --- |
| build | 0 | 1.04s | `uv build --python 3.14` | Successfully built dist/octobot_evaluators-1.10.1.tar.gz<br>Successfully built dist/octobot_evaluators-1.10.1-py3-none-any.whl |
| compile | 0 | 0.13s | `<workspace>/OctoBot-Evaluators/.venv/bin/python -m compileall -q src` | See exit status; no test-count assertion. |
| directory-resource-sync | 0 | 0.77s | `uv sync --all-extras --python 3.14.8` | See exit status; no test-count assertion. |
| final-build | 0 | 1.25s | `uv build --python 3.14.8` | Successfully built dist/octobot_evaluators-1.10.1.tar.gz<br>Successfully built dist/octobot_evaluators-1.10.1-py3-none-any.whl |
| final-build-2 | 0 | 0.89s | `uv build --python 3.14.8` | Successfully built dist/octobot_evaluators-1.10.1.tar.gz<br>Successfully built dist/octobot_evaluators-1.10.1-py3-none-any.whl |
| final-compile | 0 | 0.07s | `.venv/bin/python -m compileall -q src` | See exit status; no test-count assertion. |
| final-compile-2 | 0 | 0.07s | `.venv/bin/python -m compileall -q src` | See exit status; no test-count assertion. |
| final-existing-tests | 2 | 1.13s | `.venv/bin/python -m pytest tests` | See exit status; no test-count assertion. |
| final-existing-tests-2 | 0 | 1.39s | `.venv/bin/python -m pytest tests` | 57 passed in 0.98s |
| final-lock | 0 | 0.25s | `uv lock --upgrade` | See exit status; no test-count assertion. |
| final-lock-2 | 0 | 0.41s | `uv lock --upgrade` | See exit status; no test-count assertion. |
| final-sync | 0 | 0.08s | `uv sync --all-extras --frozen --python 3.14.8` | See exit status; no test-count assertion. |
| final-sync-2 | 0 | 0.56s | `uv sync --all-extras --frozen --python 3.14.8` | See exit status; no test-count assertion. |
| local-manager-sync | 0 | 1.85s | `uv sync --all-extras --python 3.14` | See exit status; no test-count assertion. |
| lock-3.14 | 0 | 0.88s | `uv lock --upgrade --python 3.14` | See exit status; no test-count assertion. |
| lock-3.15 | 0 | 1.37s | `uv lock --upgrade --python 3.15` | See exit status; no test-count assertion. |
| public-manager-sync | 0 | 1.12s | `uv sync --all-extras --python 3.14` | See exit status; no test-count assertion. |
| sync-3.14 | 0 | 1.37s | `uv sync --all-extras --python 3.14` | See exit status; no test-count assertion. |
| sync-3.15 | 2 | 0.04s | `uv sync --all-extras --python 3.15` | See exit status; no test-count assertion. |
| tests | 2 | 2.39s | `<workspace>/OctoBot-Evaluators/.venv/bin/python -m pytest tests` | See exit status; no test-count assertion. |
| tests-2 | 1 | 8.46s | `.venv/bin/python -m pytest tests` | 52 passed, 5 errors in 6.78s |
| tests-3 | 2 | 2.19s | `.venv/bin/python -m pytest tests` | See exit status; no test-count assertion. |
| tests-4 | 2 | 2.16s | `.venv/bin/python -m pytest tests` | See exit status; no test-count assertion. |
| tests-5 | 2 | 2.15s | `.venv/bin/python -m pytest tests` | See exit status; no test-count assertion. |
| tests-6 | 1 | 3.34s | `.venv/bin/python -m pytest tests` | 52 passed, 5 errors in 2.50s |
| updated-manager-sync | 0 | 0.61s | `uv sync --all-extras --python 3.14` | See exit status; no test-count assertion. |
