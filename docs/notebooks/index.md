# Notebooks

The workshop is built around three presentations — **OBIS2CIOOS**,
**pyIPT**, and **Pyobistools** — each backed by hands-on notebooks. Every
notebook is self-contained and runs in Google Colab or locally (see
[setup](../workshop/setup.md)).

Today, the OBIS2CIOOS block is fully runnable; pyIPT and Pyobistools
notebooks are in progress.

## 01 — OBIS2CIOOS

Transforming OBIS datasets into formats suitable for discovery through
CIOOS. Split across three notebooks, one per upstream API the OBIS2CIOOS
pipeline depends on.

### OBIS REST API

The request-level view of OBIS — `/v3/dataset`, `/v3/occurrence`, `/v3/facet`,
cursor pagination, and the `country=`/`geometry=` quirks. The path everything
higher-level eventually lands on.

[Open notebook](01_obis_rest_api.ipynb){ .md-button .md-button--primary }
[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/cioos-siooc/CPDW-VI/blob/main/docs/notebooks/01_obis_rest_api.ipynb)

### Parquet + DuckDB

Query OBIS's full per-dataset Parquet exports
([`iobis/obis-open-data`](https://github.com/iobis/obis-open-data)) on S3
directly with DuckDB — no download, no pagination, SQL-native.

[Open notebook](02_obis_parquet_duckdb.ipynb){ .md-button .md-button--primary }
[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/cioos-siooc/CPDW-VI/blob/main/docs/notebooks/02_obis_parquet_duckdb.ipynb)

### WoRMS + pyworms

Resolve `scientificName` strings to authoritative AphiaIDs, accepted names,
and full classification trees via the [World Register of Marine
Species](https://www.marinespecies.org/) REST API and the
[`pyworms`](https://github.com/iobis/pyworms) wrapper.

[Open notebook](03_worms_pyworms.ipynb){ .md-button .md-button--primary }
[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/cioos-siooc/CPDW-VI/blob/main/docs/notebooks/03_worms_pyworms.ipynb)

---

## 02 — pyIPT

Programmatic dataset publishing to OBIS via the **Integrated Publishing
Toolkit (IPT)** using standard web requests — authenticating, uploading
a Darwin Core archive, triggering a publish, and inspecting the result.

*Notebook coming soon.*

---

## 03 — Pyobistools

**Validation and quality control** of Darwin Core datasets prior to
publication — required-term checks, vocabulary conformance, coordinate
sanity, and surfacing the most common publishing-blockers before they
reach the IPT.

### Validate biodiversity data

Six validation functions from `pyobistools` — `check_fields`, `check_occurrence_core_and_extension`,
`check_eventids`, `check_measurementids`, `check_scientificname_and_ids`, and `check_onland` —
applied to synthetic Darwin Core datasets with intentional errors. Each block includes a task
and a collapsible solution.

[Open notebook](workshop_validate_biodiversity_data.ipynb){ .md-button .md-button--primary }
[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/cioos-siooc/CPDW-VI/blob/main/docs/notebooks/workshop_validate_biodiversity_data.ipynb)
