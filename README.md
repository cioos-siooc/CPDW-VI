# OBIS / WoRMS: Notebook Demos

Three Jupyter notebooks on retrieving data from OBIS (Ocean Biodiversity
Information System) — via the REST API and the geoparquet exports — and
resolving the names to authoritative taxonomy via the World Register of
Marine Species (WoRMS).

## Run in Google Colab

Each notebook has a Colab-aware setup cell at the top — run it first and it
will `pip install` the deps on a fresh Colab runtime (and is a no-op when run
locally).

> **Note:** this repo is currently private. Colab badges only work for
> users signed in to a GitHub account with access to `cioos-siooc/CPDW-VI`.

| Notebook | Open in Colab |
| --- | --- |
| `01_obis_rest_api.ipynb` | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/cioos-siooc/CPDW-VI/blob/main/docs/notebooks/01_obis_rest_api.ipynb) |
| `02_obis_parquet_duckdb.ipynb` | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/cioos-siooc/CPDW-VI/blob/main/docs/notebooks/02_obis_parquet_duckdb.ipynb) |
| `03_worms_pyworms.ipynb` | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/cioos-siooc/CPDW-VI/blob/main/docs/notebooks/03_worms_pyworms.ipynb) |

## Layout

```
CPDW-VI/
├── pyproject.toml                 # uv-managed environment
├── mkdocs.yml                     # workshop site config
└── docs/
    ├── index.md                       # site landing page
    ├── workshop/                      # overview / setup / dataset
    └── notebooks/
        ├── 01_obis_rest_api.ipynb        # ~10 min — OBIS REST + cursor pagination
        ├── 02_obis_parquet_duckdb.ipynb  # ~15 min — S3 Parquet via DuckDB
        └── 03_worms_pyworms.ipynb        # ~15 min — WoRMS REST + pyworms
```

## Setup

```bash
cd obis-presentation
uv sync
# Launch the kernel from this env in your existing Jupyter:
uv run python -m ipykernel install --user --name obis-presentation --display-name "OBIS presentation"
# Then open docs/notebooks/ in JupyterLab / Notebook / VS Code and pick the
# "OBIS presentation" kernel.
```

(If you prefer everything in one env, `uv add jupyterlab` will pull it in.)

## Demo dataset

A single OBIS dataset UUID is reused across all three notebooks so attendees
see the same data through each lens:

- **Primary**: `d895e645-a98d-4720-b6fb-332929190f36` (Maritimes Spring RV Surveys —
  rich eMoF + taxonomy)
- **Backup**: `4b5e4ccb-cf66-44e4-8890-fa68f8404c3f` (small dataset for
  quick API/parquet comparisons)
