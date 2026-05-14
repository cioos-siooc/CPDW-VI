# Notebooks

Three notebooks, one per API. Each is self-contained and runs in Google Colab
or locally — see [setup](../workshop/setup.md).

## 01 — OBIS REST API

The request-level view of OBIS — `/v3/dataset`, `/v3/occurrence`, `/v3/facet`,
cursor pagination, and the `country=`/`geometry=` quirks. The path everything
higher-level eventually lands on.

[Open notebook](01_obis_rest_api.ipynb){ .md-button .md-button--primary }
[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/cioos-siooc/CPDW-VI/blob/main/docs/notebooks/01_obis_rest_api.ipynb)

---

## 02 — Parquet + DuckDB

Query OBIS's full per-dataset Parquet exports
([`iobis/obis-open-data`](https://github.com/iobis/obis-open-data)) on S3
directly with DuckDB — no download, no pagination, SQL-native.

[Open notebook](02_obis_parquet_duckdb.ipynb){ .md-button .md-button--primary }
[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/cioos-siooc/CPDW-VI/blob/main/docs/notebooks/02_obis_parquet_duckdb.ipynb)

---

## 03 — WoRMS + pyworms

Resolve `scientificName` strings to authoritative AphiaIDs, accepted names,
and full classification trees via the [World Register of Marine
Species](https://www.marinespecies.org/) REST API and the
[`pyworms`](https://github.com/iobis/pyworms) wrapper.

[Open notebook](03_worms_pyworms.ipynb){ .md-button .md-button--primary }
[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/cioos-siooc/CPDW-VI/blob/main/docs/notebooks/03_worms_pyworms.ipynb)
