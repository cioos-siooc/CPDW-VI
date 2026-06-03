# CPDW 2026 — OBIS Developer Workshop

**From Observations to Ocean Data Systems — developer workflows for OBIS
access, validation, and publishing.**

A developer-focused working session at the **CIOOS Pacific Data Workshop
2026**: three short presentations, each paired with hands-on Jupyter
notebooks, covering the practical mechanics of moving Darwin Core
biodiversity data through the OBIS ecosystem.

Workshop site: <https://cioos-siooc.github.io/CPDW-VI/>

## The three presentations

| # | Presentation | Tool | Focus |
| --- | --- | --- | --- |
| 01 | Transforming OBIS datasets for CIOOS discovery | `OBIS2CIOOS` | Pulling OBIS data and reshaping it for CIOOS metadata catalogues |
| 02 | Programmatic publishing to OBIS via the IPT | `pyIPT` | Automating dataset publication through the Integrated Publishing Toolkit |
| 03 | Validating Darwin Core datasets before publication | `Pyobistools` | QC and Darwin Core validation prior to publishing |

OBIS2CIOOS (01) and Pyobistools (03) are runnable today; the pyIPT
notebook (02) is still in progress.

## Run in Google Colab

Each notebook has a Colab-aware setup cell at the top — run it first and it
will `pip install` the deps on a fresh Colab runtime (and is a no-op when
run locally).

> **Note:** this repo is currently private. Colab badges only work for
> users signed in to a GitHub account with access to `cioos-siooc/CPDW-VI`.

### 01 — OBIS2CIOOS

| Notebook | Open in Colab |
| --- | --- |
| `01_obis_rest_api.ipynb` — OBIS REST + cursor pagination | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/cioos-siooc/CPDW-VI/blob/main/docs/notebooks/01_obis_rest_api.ipynb) |
| `02_obis_parquet_duckdb.ipynb` — S3 Parquet via DuckDB | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/cioos-siooc/CPDW-VI/blob/main/docs/notebooks/02_obis_parquet_duckdb.ipynb) |
| `03_worms_pyworms.ipynb` — WoRMS REST + pyworms | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/cioos-siooc/CPDW-VI/blob/main/docs/notebooks/03_worms_pyworms.ipynb) |

Slides: [`docs/presentations/OBIS2CIOOS.pptx`](docs/presentations/OBIS2CIOOS.pptx)

### 02 — pyIPT

Programmatic dataset publishing to OBIS via the Integrated Publishing
Toolkit (IPT) using standard web requests. *Notebook coming soon.*

### 03 — Pyobistools

| Notebook | Open in Colab |
| --- | --- |
| `workshop_validate_biodiversity_data.ipynb` — Darwin Core validation with `pyobistools` | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/cioos-siooc/CPDW-VI/blob/main/docs/notebooks/workshop_validate_biodiversity_data.ipynb) |

Six validation functions — `check_fields`,
`check_occurrence_core_and_extension`, `check_eventids`,
`check_measurementids`, `check_scientificname_and_ids`, and `check_onland`
— applied to synthetic Darwin Core datasets with intentional errors. Each
block pairs a task with a collapsible solution.

Slides: [`docs/presentations/CPDW_Pyobistools_CIOOS.pptx`](docs/presentations/CPDW_Pyobistools_CIOOS.pptx)

## Layout

```
CPDW-VI/
├── pyproject.toml                 # uv-managed environment
├── mkdocs.yml                     # workshop site config
└── docs/
    ├── index.md                       # site landing page
    ├── workshop/                      # overview / setup / dataset
    ├── presentations/                 # slide decks (.pptx)
    └── notebooks/
        ├── 01_obis_rest_api.ipynb                     # OBIS REST + cursor pagination
        ├── 02_obis_parquet_duckdb.ipynb               # S3 Parquet via DuckDB
        ├── 03_worms_pyworms.ipynb                     # WoRMS REST + pyworms
        ├── workshop_validate_biodiversity_data.ipynb  # Darwin Core validation (pyobistools)
        └── workshop_ex_*.csv                          # synthetic DwC sample data
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

A single OBIS dataset UUID is reused across the OBIS2CIOOS notebooks so
attendees see the same data through each lens:

- **Primary**: `d895e645-a98d-4720-b6fb-332929190f36` (Maritimes Spring RV
  Surveys — rich eMoF + taxonomy)
- **Backup**: `4b5e4ccb-cf66-44e4-8890-fa68f8404c3f` (small dataset for
  quick API/parquet comparisons)

## Hosts

- **TBD** — Ocean Tracking Network
- **TBD** — St. Lawrence Global Observatory
- **Simon Beauvillier** and **Richard Kelly** — CIOOS Coordination Office
