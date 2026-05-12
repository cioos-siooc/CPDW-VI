# Notebooks

Four notebooks. Each is self-contained and runs in Google Colab or locally —
see [setup](../workshop/setup.md).

## 01 — pyobis quickstart

High-level Python client for OBIS. Search occurrences, build a `DataFrame`,
plot a quick map.

[Open notebook](01_pyobis_quickstart.ipynb){ .md-button .md-button--primary }
[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/cioos-siooc/CPDW-VI/blob/main/docs/notebooks/01_pyobis_quickstart.ipynb)

---

## 02 — OBIS REST API

Raw REST + cursor pagination. What `pyobis` is doing under the hood, and
when you'd want to drop down to it.

[Open notebook](02_obis_rest_api.ipynb){ .md-button .md-button--primary }
[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/cioos-siooc/CPDW-VI/blob/main/docs/notebooks/02_obis_rest_api.ipynb)

---

## 03 — Parquet + DuckDB

Query OBIS's full Parquet snapshot on S3 directly with DuckDB — no download,
no pagination, SQL-native.

[Open notebook](03_obis_parquet_duckdb.ipynb){ .md-button .md-button--primary }
[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/cioos-siooc/CPDW-VI/blob/main/docs/notebooks/03_obis_parquet_duckdb.ipynb)

---

## 04 — OBIS → CIOOS metadata

Convert an OBIS dataset record into CIOOS-compatible metadata using
`cioos-metadata-conversion`.

[Open notebook](04_obis_to_cioos_metadata.ipynb){ .md-button .md-button--primary }
[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/cioos-siooc/CPDW-VI/blob/main/docs/notebooks/04_obis_to_cioos_metadata.ipynb)
