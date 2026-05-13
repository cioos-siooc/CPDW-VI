# Setup

You have two options: **Google Colab** (zero install) or **local with uv**.

## Option A — Google Colab (recommended for the workshop)

Each notebook has a Colab-aware setup cell at the top. Open any notebook
via its Colab badge on the [notebooks page](../notebooks/index.md), and run
the first cell — it will `pip install` the dependencies on the Colab runtime
(and is a no-op when run locally).

!!! note "Repo access"
    The repo is currently private. Colab badges only work for users signed in
    to a GitHub account with access to `cioos-siooc/CPDW-VI`.

## Option B — Local with uv

```bash
git clone https://github.com/cioos-siooc/CPDW-VI.git
cd CPDW-VI
uv sync
uv run python -m ipykernel install --user \
    --name obis-presentation \
    --display-name "OBIS presentation"
```

Then open `docs/notebooks/` in JupyterLab / VS Code and pick the
**OBIS presentation** kernel.

!!! tip "cioos-metadata-conversion"
    Notebook 04 uses `cioos-metadata-conversion`, which is not on PyPI. The
    `pyproject.toml` wires it as a path install to
    `../../cioos-metadata-conversion` (relative to this directory). Adjust if
    your workspace layout differs. The Colab setup cell pulls it directly
    from `github.com/cioos-siooc/cioos-metadata-conversion`.
