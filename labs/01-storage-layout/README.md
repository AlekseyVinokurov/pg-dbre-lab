# Lab 01 — Storage layout & DDL

**Status:** In progress

## Objective

Understand how PostgreSQL physically stores rows and why column types, alignment, NULLability and TOAST can change table size and read behaviour.

This lab is intentionally about storage mechanics before query tuning.

## Questions to answer

- What is stored inside an 8 KiB PostgreSQL heap page?
- What overhead does a heap tuple carry?
- When does PostgreSQL add alignment padding between attributes?
- How does column order affect row width?
- How does a NULL bitmap change tuple layout?
- When does TOAST move or compress values?
- How do row width and page density affect total table size and buffer reads?

## Experiment workflow

1. Record the PostgreSQL and OS environment.
2. Create an isolated schema for the experiment.
3. Generate only synthetic data.
4. Measure the baseline table and index sizes.
5. Compare alternative row layouts without changing the logical dataset.
6. Inspect page/tuple behaviour using PostgreSQL-native statistics and diagnostic tools.
7. Record observations before drawing conclusions.
8. Explain the physical mechanism in your own words.
9. Drop the lab schema when the experiment is complete.

## Evidence to capture

- DDL used for each layout
- row count and data distribution
- `pg_total_relation_size` / `pg_relation_size`
- average row width where relevant
- page density / tuple observations where available
- query plans used to compare read behaviour
- exact before/after measurements

## Completion criteria

This lab is complete only when the repository contains a reproducible experiment showing at least one measurable storage-layout effect and a written explanation of the PostgreSQL mechanism that caused it.

## Files

The SQL generator, measurements and final report will be added as the experiment is performed. Results are not pre-filled so the repository reflects observed work rather than invented outcomes.
