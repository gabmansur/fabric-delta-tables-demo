# Fabric Delta Tables Demo  

This repo is a hands-on, step-by-step demo of Delta Tables in Microsoft Fabric using Apache Spark.  
It follows the spirit of the [MS Learn Delta Lake lab](https://microsoftlearning.github.io/mslearn-fabric/Instructions/Labs/03-delta-lake.html), but is structured around DP-700 exam skills.  

Dataset used: [`products.csv`](https://github.com/MicrosoftLearning/dp-data/raw/main/products.csv)  


## Purpose  

- Practice the skills tested in DP-700: Implementing Analytics Solutions Using Microsoft Fabric.  
- Learn how Delta Tables work in Fabric (batch + streaming).  
- Build intuition about transaction logs, ACID guarantees, schema evolution, and time travel.  
- Provide a didactic, notebook-by-notebook narrative you can follow and reuse.  


## What You’ll Learn  

- Batch ingestion into Lakehouse (bronze → silver).  
- Difference between Parquet vs Delta (transaction log, ACID).  
- Managed vs external tables in Fabric.  
- How to query Delta with SparkSQL and see table history.  
- How to handle real-time ingestion with Structured Streaming.  
- How to apply updates, merges, schema evolution, and time travel.  


## Project Structure  

### 1. `01_setup_workspace_and_lakehouse.ipynb`  
- Initialize Spark session and lakehouse.  
- Create base directories, databases, check environment.  
- **Exam link:** Configure Fabric/Spark workspace, OneLake structure.  

### 2. `02_batch_create_delta_from_files.ipynb`  
- Ingest `products.csv` into a Lakehouse.  
- Create managed and external Delta tables.  
- Compare table storage and metadata.  
- **Exam link:** Ingest and transform data, managed vs unmanaged storage.  

### 3. `03_sql_query_delta.ipynb`  
- Query Delta tables with SparkSQL.  
- Run basic queries (`SELECT`, `GROUP BY`).  
- Use `DESCRIBE HISTORY` to see Delta logs.  
- **Exam link:** Query with SQL endpoints, monitor metadata.  

### 4. `04_streaming_to_delta.ipynb`  
- Simulate real-time ingestion with JSON events.  
- Write stream → Delta with checkpointing.  
- Validate streaming output and schema enforcement.  
- **Exam link:** Implement streaming ingestion, data freshness.  

### 5. `05_updates_history_time_travel.ipynb`  
- Perform `UPDATE`, `DELETE`, and `MERGE`.  
- Use time travel (`VERSION AS OF`, `TIMESTAMP AS OF`).  
- Show rollback to previous states.  
- **Exam link:** Lifecycle management, updates, auditing.  

### 6. `06_schema_evolution.ipynb`  
- Ingest new data with extra columns.  
- Enable schema evolution, check logs.  
- Demonstrate schema enforcement vs evolution.  
- **Exam link:** Handle schema drift, evolving models.  

## Skills Practiced  

- PySpark DataFrame API  
- Managed vs external Delta tables  
- SparkSQL queries and history logs  
- Structured Streaming (with checkpoints)  
- Updates, deletes, and merges in Delta  
- Time travel and rollback  
- Schema enforcement and evolution  



## Next Steps (not implemented here, but exam-relevant)  

- **Security & Governance:** Row-level security, column masking, data lineage in Purview.  
- **Optimization:** Partitioning strategies, Z-ordering, caching.  
- **Monitoring:** Query performance metrics, Fabric monitoring tools.  


---

 This repo is designed as a training playground**:  
Open each notebook in order, follow along, and map what you do back to DP-700 skills.  
