# OBIS → CIOOS: Notebook Demos

Jupyter notebook examples (~45 min) on retrieving data from OBIS (Ocean
Biodiversity Information System) and how those flows feed CIOOS pipelines.

## Run in Google Colab

Each notebook has a Colab-aware setup cell at the top — run it first and it
will `pip install` the deps on a fresh Colab runtime (and is a no-op when run
locally).

> **Note:** this repo is currently private. Colab badges only work for
> users signed in to a GitHub account with access to `cioos-siooc/CPDW-VI`.

| Notebook | Open in Colab |
| --- | --- |
| `01_pyobis_quickstart.ipynb` | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/cioos-siooc/CPDW-VI/blob/main/notebooks/01_pyobis_quickstart.ipynb) |
| `02_obis_rest_api.ipynb` | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/cioos-siooc/CPDW-VI/blob/main/notebooks/02_obis_rest_api.ipynb) |
| `03_obis_parquet_duckdb.ipynb` | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/cioos-siooc/CPDW-VI/blob/main/notebooks/03_obis_parquet_duckdb.ipynb) |
| `04_obis_to_cioos_metadata.ipynb` | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/cioos-siooc/CPDW-VI/blob/main/notebooks/04_obis_to_cioos_metadata.ipynb) |

Notebook 04 uses `cioos-metadata-conversion`, which is not on PyPI — its
setup cell installs it from
`github.com/cioos-siooc/cioos-metadata-conversion`.

## Layout

```
obis-presentation/
├── pyproject.toml                 # uv-managed environment
└── notebooks/
    ├── 01_pyobis_quickstart.ipynb     # ~10 min — pyobis high-level client
    ├── 02_obis_rest_api.ipynb         # ~10 min — raw REST + cursor pagination
    ├── 03_obis_parquet_duckdb.ipynb   # ~15 min — S3 Parquet via DuckDB
    └── 04_obis_to_cioos_metadata.ipynb # ~10 min — cioos-metadata-conversion
```

## Setup

```bash
cd obis-presentation
uv sync
# Launch the kernel from this env in your existing Jupyter:
uv run python -m ipykernel install --user --name obis-presentation --display-name "OBIS presentation"
# Then open notebooks/ in JupyterLab / Notebook / VS Code and pick the
# "OBIS presentation" kernel.
```

(If you prefer everything in one env, `uv add jupyterlab` will pull it in
— note `cffconvert` from `cioos-metadata-conversion` clashes with recent
`jupyterlab`, so you may need `uv add 'jupyterlab<4' notebook` or use a
separate Jupyter env and the kernel install above.)

The `cioos-metadata-conversion` dependency is wired as a path install to
`../../cioos-metadata-conversion` (relative to this directory) — adjust
`pyproject.toml` if your workspace layout differs.

## Demo dataset

A single OBIS dataset UUID is reused across all four notebooks so attendees
see the same data through each lens:

- **Primary**: `d895e645-a98d-4720-b6fb-332929190f36` (Maritimes Spring RV Surveys —
  rich eMoF + taxonomy)
- **Backup**: `4b5e4ccb-cf66-44e4-8890-fa68f8404c3f` (small dataset for
  quick API/parquet comparisons)
