# Azure Data Factory

### Definition

Azure Data Factory (ADF) is **a fully managed, serverless cloud ETL service for data integration, orchestration, and transformation**, allowing users to build complex hybrid data pipelines with over 100 built-in connectors. It enables scheduling and automating data movement from on-premise and cloud sources (e.g., AWS S3, SQL Server) to Azure storage, often used for data engineering, warehousing, and analytics.
<hr>

### ADF vs Databricks

- **ADF:** Best for **orchestration**, moving data (Copy Activity), and simple low-code transformations. It’s the "traffic cop."
- **Databricks:** Best for **heavy lifting**, complex business logic, machine learning, and high-performance Spark processing.
- **Typical Pattern:** Use ADF to trigger a Databricks Notebook.
