# Demo dataset

The **OBIS2CIOOS** block reuses a single OBIS dataset UUID across all
three of its notebooks so attendees see the same data through each lens
(REST, Parquet, WoRMS).

The **pyIPT** and **Pyobistools** blocks may use different fixtures
(e.g. a draft IPT resource, or a deliberately invalid Darwin Core file
to surface validation errors) — those will be documented alongside their
notebooks when added.

## Primary (OBIS2CIOOS)

**Maritimes Spring RV Surveys** — `d895e645-a98d-4720-b6fb-332929190f36`

Rich extended Measurement or Fact (eMoF) data and full taxonomy — a good
showcase for everything the OBIS2CIOOS notebooks do.

## Backup

`4b5e4ccb-cf66-44e4-8890-fa68f8404c3f`

A smaller dataset, useful for quick API/parquet comparisons if the network
is slow during the workshop.

## Why one dataset across all OBIS2CIOOS notebooks?

Reusing the same UUID lets attendees compare:

- the raw REST records (notebook 01),
- the Parquet snapshot rows (notebook 02), and
- the WoRMS-resolved taxonomy for its top species (notebook 03)

…of the **same underlying data**.
