### Definition

It’s a data design pattern used to organize data in a Lakehouse.

- **Bronze:** Raw ingestion (often as-is from source).

- **Silver:** Cleansed, filtered, and augmented data. This is the "source of truth" for many downstream processes.

- **Gold:** Business-level aggregates (Star Schema) ready for BI.

Unlike traditional warehouses, it provides **lineage**, **ACID transactions** (via Delta Lake), and the ability to reprocess data from "raw" if business logic changes.
