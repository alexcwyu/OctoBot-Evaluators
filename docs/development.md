# Development

<!-- current-documentation-provenance -->
Documentation reviewed: 2026-10-13 · Git source base: `e622bb6586e74b031efef7b25c6018f214fe9f90` · [Current architecture and feature guide](ayu-develop.md).
Historical execution commands/results below retain their original dates and scope; this metadata update is not a new application test run.
<!-- /current-documentation-provenance -->


## uv maintenance workflow (2026-10-12)

Selected complete environment: Python 3.15.0; build backend `hatchling.build`. The workspace uses uv 0.13.0. The complete latest-source native build and original repository suite are verified; exact results are recorded in [validation](validation.md).

```sh
export UV_PYTHON_PREFERENCE=only-managed
uv python install 3.15.0
uv lock --upgrade
uv sync --all-extras --python 3.15.0
uv build --python 3.15.0
uv run --frozen --all-extras python -m compileall -q src/octobot_evaluators
uv run --frozen --all-extras python -m pytest tests
```

Keep source resources inside their package and preserve the repository's existing src layout. Rebuild after source/native/asset changes. Use the locked environment for final verification. Commands above are the standard workflow, not a promise that every existing suite currently passes; consult validation for exact outcomes and unresolved compatibility issues.

## Compatible manager source

The local uv source in [vendor/tentacles-manager](../vendor/tentacles-manager/PROVENANCE.md) preserves the LGPL upstream 2.10.0 API used by this release. The source closes `os.scandir` iterators even when discovery returns early and uses `packaging.version` instead of the removed `distutils.version`. Its declared full dependencies resolve current compatible releases. OctoBot-Trading shares this source through its workspace-relative uv path; keep the repositories beside one another for locked synchronization.

## Current native indicator source

The top-level uv source explicitly selects [the adjacent licensed Tulipy 0.4.11b13 source](../../OctoBot/vendor/octobot-tulipy/PROVENANCE.md), retaining NumPy 2.4.2 and the original indicator formulas. Strict native multiply/add compiler flags preserve original RSI arithmetic. This resolves the missing Python 3.15 release wheel through a genuine current-source build. This repository’s own original suite, source distribution, wheel and strict source compilation pass in an isolated Python 3.15 control before selecting that interpreter. No host-package suite substitutes for the standalone cases.
