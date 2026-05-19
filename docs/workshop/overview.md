# Workshop overview

This workshop is part of the **CIOOS Pacific Data Workshop (CPDW) 2026**.
It runs as three short presentations — each paired with hands-on Jupyter
material — covering the practical mechanics of moving Darwin Core
biodiversity data through the OBIS ecosystem.

## The three presentations

| # | Presentation | Tool | What it covers |
| --- | --- | --- | --- |
| 01 | Transforming OBIS datasets for CIOOS discovery | `OBIS2CIOOS` | Pulling OBIS data via REST and Parquet, resolving taxonomy via WoRMS, reshaping records for CIOOS |
| 02 | Programmatic publishing to OBIS via the IPT | `pyIPT` | Automating dataset publication through the Integrated Publishing Toolkit |
| 03 | Validating Darwin Core datasets before publication | `Pyobistools` | QC and Darwin Core validation prior to publishing |

The **OBIS2CIOOS** block runs against three notebooks (one per upstream
API). The **pyIPT** and **Pyobistools** notebooks are in progress.

## Format

| Block | Content |
|---|---|
| Talks | Three short presentations, one per tool |
| Hands-on notebooks | OBIS2CIOOS notebooks 01 → 03 (pyIPT / Pyobistools to follow) |
| Q&A | Discussion |

## Audience

Intended for **developers, data managers, and technical practitioners**
building reproducible workflows for biodiversity data — access,
transformation, validation, and publication across ocean data systems.

The workshop assumes basic Python familiarity and some exposure to
scientific data formats (CSV, Parquet, NetCDF). No prior OBIS or CIOOS
experience required.

## What you'll need

- A Google account (for Colab) **or** a local Python ≥ 3.11 environment
- A web browser
- Run the first setup cell of each notebook ahead of time so dependencies
  are cached on your Colab runtime

See [**setup**](setup.md) for details on running locally.
