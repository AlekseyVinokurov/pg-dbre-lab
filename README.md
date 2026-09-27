# pg-dbre-lab

**PostgreSQL Reliability & Performance Engineering Lab**

A hands-on engineering repository for studying PostgreSQL from query execution and storage internals to failure analysis, recovery, replication, and production-style diagnostics.

This is not a collection of solved SQL exercises. Each completed lab is documented as an engineering experiment:

**problem → reproducible stand → measurements → analysis → change → result → internal mechanics**

## Focus areas

- PostgreSQL storage layout, pages, tuples, TOAST, alignment and bloat
- Query planner, cardinality estimation and join algorithms
- B-Tree, BRIN, GIN, partial and covering indexes
- MVCC, locks, deadlocks and transaction isolation
- Memory behaviour: shared buffers, work_mem and OS page cache
- WAL, checkpoints, backup, restore and point-in-time recovery
- Streaming replication, replication lag and failover concepts
- Connection management and resource limits
- Linux-level diagnostics: CPU, memory pressure, I/O and wait states
- Production-style incident investigation

## Lab roadmap

| Area | Status |
| --- | --- |
| 01 — Storage layout & DDL | In progress |
| 02 — Query planner & joins | Planned |
| 03 — Aggregation & window functions | Planned |
| 04 — Index architecture | Planned |
| 05 — MVCC, transactions & locks | Planned |
| 06 — Memory, WAL & Linux | Planned |
| 07 — Operations, recovery & replication | Planned |
| Incidents — failure simulations | Planned |

## Repository structure

```text
pg-dbre-lab/
├── labs/           # focused experiments
├── incidents/      # production-style failure investigations
├── scripts/        # reusable stand/data generators and helpers
├── docs/           # architecture notes and learning roadmap
└── templates/      # lab and incident report templates
```

## Evidence standard

A lab is not considered complete until the repository contains enough evidence to reproduce and explain the result. Depending on the topic, that may include:

- exact PostgreSQL and OS environment
- schema and synthetic data generator
- baseline query or failure condition
- `EXPLAIN (ANALYZE, BUFFERS)`
- relevant PostgreSQL statistics and wait events
- before/after timings and buffer activity
- explanation of *why* PostgreSQL behaved that way
- cleanup procedure

Performance numbers are treated as local measurements, not universal targets. Hardware, cache state, concurrency, dataset distribution and PostgreSQL configuration are recorded when they materially affect the result.

## Data and security

All public experiments use synthetic or intentionally non-sensitive data.

Production environments, customer infrastructure, addresses, credentials, network details and operational data are **not** published in this repository.

## Current work

The first track focuses on physical storage and row layout: PostgreSQL pages, tuple overhead, NULL bitmap, type alignment, padding and TOAST.

See [labs/01-storage-layout](labs/01-storage-layout/README.md).

## Author

**Aleksey Vinokurov**  
Systems & Integration Engineer

PostgreSQL · Linux · Networking · Python · Automation · Systems Integration · AI
