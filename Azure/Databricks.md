# Databricks

### Definition

Databricks is **a cloud-based "Data Intelligence Platform" designed to help organizations manage, process, and analyze massive amounts of data**. Founded by the original creators of Apache Spark, it is best known for pioneering the Data Lakehouse architecture, which combines the low-cost storage of a data lake with the high-performance features of a data warehouse.
<hr>

### Securing data access between Databricks and Azure Data Lake (ADLS Gen2)

- **Unity Catalog (Recommended):** Provides centralized governance and fine-grained access control.
- **Managed Identities:** Using a System-Assigned or User-Assigned Managed Identity so Databricks can authenticate to ADLS without storing hardcoded secrets or Service Principal keys in the code.
- **Azure Key Vault:** Storing secrets and referencing them via Databricks Secret Scopes.
