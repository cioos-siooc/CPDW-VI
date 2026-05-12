---
hide:
  - navigation
  - toc
---

# CPDW 2026 — OBIS → CIOOS Workshop

<div class="cioos-hero" markdown>

## Retrieving OBIS data and feeding it into CIOOS pipelines

A short talk followed by hands-on Jupyter notebooks at the
**CIOOS Pacific Data Workshop 2026**.

[Open the notebooks →](notebooks/index.md){ .md-button }
[View on GitHub →](https://github.com/cioos-siooc/CPDW-VI){ .md-button }

</div>

## What you'll learn

- Pull occurrence data from the **Ocean Biodiversity Information System (OBIS)**
  using both the high-level `pyobis` client and the raw REST API.
- Query OBIS's full **Parquet snapshot from S3** with DuckDB — no download
  required.
- Convert OBIS dataset records into **CIOOS-compatible metadata** using
  `cioos-metadata-conversion`.

## Workshop sections

| # | Notebook | Topic |
|---|---|---|
| 01 | [pyobis quickstart](notebooks/01_pyobis_quickstart.ipynb) | High-level Python client |
| 02 | [OBIS REST API](notebooks/02_obis_rest_api.ipynb) | Raw REST + cursor pagination |
| 03 | [Parquet + DuckDB](notebooks/03_obis_parquet_duckdb.ipynb) | Snapshot on S3 via DuckDB |
| 04 | [OBIS → CIOOS metadata](notebooks/04_obis_to_cioos_metadata.ipynb) | Metadata conversion |

## Get started

- New to the workshop? Read the [**overview**](workshop/overview.md).
- Want to run the notebooks locally? See [**setup**](workshop/setup.md).
- Curious about the demo dataset? See [**demo dataset**](workshop/dataset.md).
