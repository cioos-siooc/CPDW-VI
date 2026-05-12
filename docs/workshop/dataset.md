# Demo dataset

A single OBIS dataset UUID is reused across all four notebooks so attendees
see the same data through each lens.

## Primary

**Maritimes Spring RV Surveys** — `d895e645-a98d-4720-b6fb-332929190f36`

Rich extended Measurement or Fact (eMoF) data and full taxonomy — a good
showcase for everything the notebooks do.

## Backup

`4b5e4ccb-cf66-44e4-8890-fa68f8404c3f`

A smaller dataset, useful for quick API/parquet comparisons if the network
is slow during the workshop.

## Why one dataset across all notebooks?

Reusing the same UUID lets attendees compare:

- the high-level `pyobis` view (notebook 01),
- the raw REST records (notebook 02),
- the Parquet snapshot rows (notebook 03), and
- the CIOOS metadata representation (notebook 04)

…of the **same underlying data**.
