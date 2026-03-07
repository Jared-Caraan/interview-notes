# Delta Lake

### Definition

Delta Lake is the optimized, open-source storage layer that serves as the foundation for the Databricks Lakehouse platform. It adds ACID transactions, scalable metadata handling, and time travel (data versioning) to existing cloud storage (S3, ADLS, GCS), enabling reliable batch and streaming data processing. It is the default, high-performance table format for all data operations in Databricks.
<hr>

### Difference between `OPTIMIZE` and `VACUUM`

`OPTIMIZE` compacts small files into larger ones (the "Small File Problem") and can include **Z-Ordering** to co-locate related data for faster retrieval. `VACUUM` deletes files that are no longer referenced by the Delta table (older than the retention period, usually 7 days). Be careful: running this prevents you from using Time Travel to access those specific older versions.
