### Definition

A **Snowflake Virtual Warehouse** is a cluster of compute resources (CPU, memory, and temporary storage) used to execute SQL queries and perform DML operations.

Think of it as the **"muscle"** of the Snowflake architecture, while the storage layer acts as the "brain."

Warehouses are independent, you can run a massive **ETL job** on one warehouse while **Data Analysts** run BI reports on another, ensuring there is **zero resource contention**.
<hr>

### Three Key Pillars

- **Separation of Storage and Compute:** Warehouses are completely independent of the data storage layer. You can scale your compute power up or down without ever moving or affecting the underlying data.

- **Elasticity & Scaling:** * **Scale Up (Vertical):** Increase the warehouse size (e.g., from Small to Large) for faster processing of complex queries.

  - **Scale Out (Horizontal):** Add more clusters to a warehouse to handle higher concurrency (more users/queries at once).

- **Pay-Per-Second:** Warehouses only consume credits when they are running. They can be set to "Auto-Suspend" when idle and "Auto-Resume" when a query is submitted, making them highly cost-effective.
