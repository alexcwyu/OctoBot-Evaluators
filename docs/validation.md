# OctoBot-Evaluators: final Python 3.15 verification

Selected runtime: **managed Python 3.15.0**, uv **0.13.0**; source commit `da572a53894520bd41a49418c25e228057be8252`. Its own existing repository suite passed: **57 passed in 1.99s**. This is the original standalone repository suite, separately executed from the newer host's package suites. Source distribution and wheel builds, frozen synchronization and strict source compilation passed. No test cases, golden values or formulas changed.

[Development and native prerequisites](development.md) · [Portable exact commands](maintenance/index.md) · [Machine-readable evidence](maintenance/verification.json). The locked adjacent licensed source and supported system-library configuration are explicit in the project metadata and development guide.

## Historical verification attempts


Recorded 2026-10-12T01:32:44.003848+08:00. Branch `feature/ayu_develop`; upstream default `upstream/master` is merged: **true**. Branch/tag synchronization records are retained in the workspace maintenance evidence. Feature branch publication is coordinated separately.

Runtime: **CPython 3.14.8**, uv **0.13.0**, build backend `hatchling.build`. Tulipy 0.4.11b13 has no Python 3.15 distribution; Python 3.14.8 is selected.

Existing suite: **57 passed in 0.98s** (exit `0`). Existing evaluator suite passes with the LGPL manager 2.10.0 compatibility source: directory iterators close on early matches, and packaging.version replaces removed distutils. See vendor/tentacles-manager/PROVENANCE.md.

No test cases were added. Existing assertions and strict warning behavior remain active; repaired fixtures own their loops, sessions, files and configuration paths. Existing upstream platform skips and configured deselections are reported exactly.

## Final build commands

| Check | Exact command | Exit | Seconds |
| --- | --- | ---: | ---: |
| lock | `uv lock --upgrade` | 0 | 0.41 |
| sync | `uv sync --all-extras --frozen --python 3.14.8` | 0 | 0.56 |
| build | `uv build --python 3.14.8` | 0 | 0.89 |
| compile | `.venv/bin/python -m compileall -q src` | 0 | 0.07 |

## Existing test and compatibility evidence

| Check | Exact command | Exit | Result |
| --- | --- | ---: | --- |
| lock-3.15 | `uv lock --upgrade --python 3.15` | 0 | Check completed; see exact exit code. |
| sync-3.15 | `uv sync --all-extras --python 3.15` | 2 | Check completed; see exact exit code. |
| tests | `/Users/alex/workspaces/trading/OctoBot-Evaluators/.venv/bin/python -m pytest tests` | 2 | 7 errors in 1.57s |
| tests-2 | `.venv/bin/python -m pytest tests` | 1 | 52 passed, 5 errors in 6.78s |
| tests-3 | `.venv/bin/python -m pytest tests` | 2 | 7 errors in 1.37s |
| tests-4 | `.venv/bin/python -m pytest tests` | 2 | 7 errors in 1.37s |
| tests-5 | `.venv/bin/python -m pytest tests` | 2 | 7 errors in 1.24s |
| tests-6 | `.venv/bin/python -m pytest tests` | 1 | 52 passed, 5 errors in 2.50s |
| final-existing-tests | `.venv/bin/python -m pytest tests` | 2 | 7 errors in 0.72s |
| final-existing-tests-2 | `.venv/bin/python -m pytest tests` | 0 | 57 passed in 0.98s |

Raw logs remain in the workspace maintenance evidence directory. The [portable verification record](maintenance/verification.json) retains exact command arrays, exits, timing, runtime inventory and log filenames. Earlier failed attempts remain recorded and are not treated as successful final validation.

## Installed dependency versions

This is the selected environment after locked synchronization; isolated wheel build dependencies are resolved by the build backend and recorded in build output.

| Distribution | Version |
| --- | --- |
| aioboto3 | 15.5.0 |
| aiobotocore | 2.25.1 |
| aiofiles | 25.1.0 |
| aiohappyeyeballs | 2.7.1 |
| aiohttp | 3.14.5 |
| aioitertools | 0.13.0 |
| aiosignal | 1.4.0 |
| aiosqlite | 0.22.1 |
| async_channel | 2.2.2 |
| attrs | 26.1.0 |
| boto3 | 1.40.61 |
| botocore | 1.40.61 |
| certifi | 2026.7.22 |
| cffi | 2.1.1 |
| charset-normalizer | 3.5.2 |
| coverage | 7.16.2 |
| cryptography | 50.0.2 |
| Cython | 3.3.0 |
| execnet | 2.1.2 |
| frozenlist | 1.8.0 |
| idna | 3.20 |
| iniconfig | 2.3.1 |
| Jinja2 | 3.1.6 |
| jmespath | 1.1.0 |
| jsonschema | 4.26.0 |
| jsonschema-specifications | 2025.9.1 |
| MarkupSafe | 3.0.4 |
| mock | 5.2.0 |
| multidict | 6.9.1 |
| numpy | 2.5.4 |
| octobot-commons | 1.10.6 |
| octobot-evaluators | 1.10.1 |
| octobot-tentacles-manager | 2.10.0+ayu.1 |
| OctoBot-Tulipy | 0.4.11b13 |
| packaging | 26.3 |
| pluggy | 1.6.0 |
| propcache | 0.5.4 |
| psutil | 7.2.2 |
| pycparser | 3.11 |
| Pygments | 2.21.0 |
| pytest | 9.1.1 |
| pytest-asyncio | 1.4.0 |
| pytest-cov | 7.1.0 |
| pytest-timeout | 2.4.0 |
| pytest-xdist | 3.8.0 |
| python-dateutil | 2.9.0.post0 |
| PyYAML | 6.0.3 |
| referencing | 0.37.0 |
| requests | 2.34.2 |
| rpds-py | 2026.9.1 |
| ruff | 0.17.0 |
| s3transfer | 0.14.0 |
| six | 1.17.0 |
| sortedcontainers | 2.4.0 |
| urllib3 | 2.8.0 |
| wrapt | 1.17.3 |
| yarl | 1.25.1 |

See [architecture](ayu-develop.md) for source-linked component/sequence/workflow diagrams and [development](development.md) for reproducible uv commands.
