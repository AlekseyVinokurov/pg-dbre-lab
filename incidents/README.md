# Incidents

Production-style PostgreSQL failure simulations live here.

The goal is not to collect dramatic outages. The goal is to practice diagnosis from symptoms and evidence.

Each incident should answer:

1. What was the user-visible symptom?
2. What changed?
3. Which subsystem was actually saturated or blocked?
4. Which evidence isolated the root cause?
5. What restored service?
6. What would prevent recurrence?

Examples of future scenarios include lock contention, deadlocks, connection storms, disk pressure, checkpoint/WAL pressure, stale statistics, bad cardinality estimates, replication lag and recovery exercises.

Real customer incidents and sensitive infrastructure data are not published here.
