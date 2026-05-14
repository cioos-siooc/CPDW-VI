
---
hide:
  - navigation
  - toc
---

# CPDW 2026 — OBIS Developer Workshop

<div class="cioos-hero" markdown>

## From Observations to Ocean Data Systems

**Developer Workflows for OBIS Access, Validation, and Publishing**

A developer-focused working session at the **CIOOS Pacific Data Workshop
2026** — three short presentations, each paired with a hands-on Jupyter
notebook, covering the practical mechanics of moving Darwin Core
biodiversity data through the OBIS ecosystem.

[Open the notebooks →](notebooks/index.md){ .md-button }
[View on GitHub →](https://github.com/cioos-siooc/CPDW-VI){ .md-button }

</div>

## About the session

Darwin Core provides a shared vocabulary for biodiversity records, enabling
interoperable data exchange across biodiversity and ocean data systems. The
**Ocean Biodiversity Information System (OBIS)** relies on Darwin Core–aligned
datasets to support the integration, discovery, and reuse of marine
biodiversity observations.

This working session presents a developer-focused walkthrough of practical
workflows for **accessing, transforming, validating, and publishing**
biodiversity data within the OBIS ecosystem and related ocean data
infrastructures.

Intended for **developers, data managers, and technical practitioners**
interested in building reproducible workflows for biodiversity data
transformation, validation, and publication across ocean data systems.

## The three presentations

| # | Presentation | Tool | Notebook |
|---|---|---|---|
| 01 | Transforming OBIS datasets for CIOOS discovery | `OBIS2CIOOS` | [see notebooks ↓](#01-obis2cioos) |
| 02 | Programmatic publishing to OBIS via the IPT | `pyIPT` | `02_pyipt_publishing.ipynb` *(coming soon)* |
| 03 | Validating Darwin Core datasets before publication | `Pyobistools` | `03_pyobistools_validation.ipynb` *(coming soon)* |

### 01 — OBIS2CIOOS

A set of translation tools that transform OBIS datasets into formats suitable
for discovery through the **Canadian Integrated Ocean Observing System
(CIOOS)**. The hands-on portion is split across three notebooks, one per
API the OBIS2CIOOS pipeline depends on:

- [**01 — OBIS REST API**](notebooks/01_obis_rest_api.ipynb) — `/v3/dataset`,
  `/v3/occurrence`, `/v3/facet`; cursor pagination; the `country=` /
  `geometry=` quirks.
- [**02 — Parquet + DuckDB**](notebooks/02_obis_parquet_duckdb.ipynb) — the
  [`iobis/obis-open-data`](https://github.com/iobis/obis-open-data) S3
  exports queried directly with DuckDB.
- [**03 — WoRMS + pyworms**](notebooks/03_worms_pyworms.ipynb) — resolving
  `scientificName` strings to authoritative AphiaIDs and full classifications
  via the [World Register of Marine Species](https://www.marinespecies.org/).

### 02 — pyIPT

A Python module that enables programmatic dataset publishing to OBIS via the
**Integrated Publishing Toolkit (IPT)** using standard web requests.

### 03 — Pyobistools

A Python toolkit supporting **validation and quality control** of Darwin
Core datasets prior to publication.

## Hosts

- **TBD** — Ocean Tracking Network
- **TBD** — St. Lawrence Global Observatory
- **Simon Beauvillier** and **Richard Kelly** — CIOOS Coordination Office

## Get started

- New to the workshop? Read the [**overview**](workshop/overview.md).
- Want to run the notebooks locally? See [**setup**](workshop/setup.md).
- Curious about the demo dataset? See [**demo dataset**](workshop/dataset.md).
