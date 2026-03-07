### Definition

Data skew happens when one partition is much larger than others, causing some executors to finish quickly while others take forever.
<hr>

### Solution

- **Salting:** Adding a random "salt" (prefix) to the join key to distribute data more evenly across partitions.

- **Adaptive Query Execution (AQE):** Enabling spark.sql.adaptive.enabled so Spark automatically optimizes skew at runtime.

- **Broadcast Joins:** If one table is small (e.g., <10MB), broadcast it to all executors to avoid a shuffle entirely.
