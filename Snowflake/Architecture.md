# Snowflake Architecture

### Difference from a Traditional Database

Snowflake uses a **multi-cluster, shared-data architecture**.

- **Storage:** Centralized on cloud storage (S3/Azure Blob) in a proprietary columnar format.
- **Compute:** "Virtual Warehouses" are independent MPP (Massively Parallel Processing) clusters.
- **Result:** You can scale compute up (for speed) or out (for concurrency) without ever copying or moving the data.
