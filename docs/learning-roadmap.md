# PostgreSQL / DBRE Learning Roadmap

This roadmap combines PostgreSQL internals with operational reliability.

## 1. Storage and DDL

Heap pages, tuple headers, NULL bitmap, alignment, padding, TOAST, catalogs and physical relation size.

## 2. Planner and joins

Cardinality estimation, statistics, Nested Loop, Hash Join, Merge Join, LATERAL and plan instability caused by skew or stale statistics.

## 3. Aggregation and analytics

HashAggregate, GroupAggregate, sort behaviour, window functions and memory/disk spill analysis.

## 4. Index architecture

B-Tree internals, page splits, bloat, INCLUDE, Index Only Scan, partial and functional indexes, GIN and BRIN.

## 5. MVCC and concurrency

xmin/xmax, VACUUM, freezing, isolation levels, row locks, SKIP LOCKED, deadlocks and contention analysis.

## 6. Memory, WAL and Linux

shared_buffers, work_mem, maintenance_work_mem, OS page cache, checkpoints, WAL, I/O latency, memory pressure and Linux observability.

## 7. Operations and reliability

pg_stat_activity, pg_stat_statements, wait events, timeouts, connection management, zero-downtime schema changes and partitioning.

## 8. Backup and recovery

Logical vs physical backup, WAL archiving, restore procedures and point-in-time recovery.

## 9. Replication and high availability

Streaming replication, replication slots, lag, synchronous/asynchronous replication, switchover/failover concepts, RPO and RTO.

## 10. Incident response

Diagnosis from symptoms: lock contention, bad plans, disk pressure, connection storms, replication lag and recovery failures.
