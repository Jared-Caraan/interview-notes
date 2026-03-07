# Dynamic Tables

### Definition

Snowflake **Dynamic Tables** are a declarative way to define the desired final state of a data pipeline using standard SQL, with Snowflake automatically managing the refresh and orchestration to keep the results up-to-date. They are a core building block for continuous data pipelines, simplifying the process of materializing query results without manual coding or scheduling.

### Difference with Streams and Tasks

**Streams and Tasks** are an imperative way to build pipelines (manual Change Data Capture). **Dynamic Tables** are declarative. You define the target state (the SQL query), and Snowflake handles the incremental refresh automatically to meet your Target Freshness (Lag). This simplifies ETL significantly.
