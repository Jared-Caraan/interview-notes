# Micropartitions

### Definition

**Micro-partitions** are the physical storage units in Snowflake. Every table is automatically divided into these small, contiguous units of storage, typically ranging from **50 MB to 500 MB** of uncompressed data.

Unlike traditional data warehouses (like Hive or SQL Server), micro-partitions in Snowflake are **automatically managed**. There is no need to define partition keys or perform manual maintenance — it’s "zero-management" partitioning.
<hr>

### 3 Technical Must-Haves

- **Columnar Storage:** Within each micro-partition, data is stored columnarly. This allows Snowflake to read only the specific columns needed for a query, drastically reducing I/O.

- **Immutable & Versioned:** Micro-partitions are immutable (they never change). When data is updated or deleted, Snowflake creates new micro-partitions, which is what enables features like **Time Travel** and **Zero-Copy Cloning**.

- **Automatic Metadata:** Snowflake automatically tracks the range of values (Min/Max), the number of distinct values, and other statistics for every column within each micro-partition.
<hr>

### Data Pruning

The most important benefit to mention is **Data Pruning**. Because Snowflake knows the Min/Max values of every micro-partition via metadata, it can "prune" (skip) entire files that don't match your query's `WHERE` clause. This allows it to scan a few megabytes instead of terabytes.
