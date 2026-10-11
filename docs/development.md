# Development

## uv maintenance workflow (2026-10-12)

Selected complete environment: Python 3.14.8; build backend `hatchling.build`. The workspace uses uv 0.13.0. Python 3.15 was attempted before any fallback; the actual failure and selected runtime are recorded in [validation](validation.md).

```sh
export UV_PYTHON_PREFERENCE=only-managed
uv python install 3.14.8
uv lock --upgrade
uv sync --all-extras --python 3.14.8
uv build --python 3.14.8
uv run --frozen --all-extras python -m compileall -q src/octobot_evaluators
uv run --frozen --all-extras python -m pytest tests
```

Keep source resources inside their package and preserve the repository's existing src layout. Rebuild after source/native/asset changes. Use the locked environment for final verification. Commands above are the standard workflow, not a promise that every existing suite currently passes; consult validation for exact outcomes and unresolved compatibility issues.

## Compatible manager source

The local uv source in [vendor/tentacles-manager](../vendor/tentacles-manager/PROVENANCE.md) preserves the LGPL upstream 2.10.0 API used by this release. The source closes `os.scandir` iterators even when discovery returns early and uses `packaging.version` instead of the removed `distutils.version`. Its declared full dependencies resolve current compatible releases. OctoBot-Trading shares this source through its workspace-relative uv path; keep the repositories beside one another for locked synchronization.
