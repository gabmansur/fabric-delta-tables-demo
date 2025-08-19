# Fabric Delta Tables Demo

This repo follows the **MS Learn Fabric Delta Lake Lab** ([link](https://microsoftlearning.github.io/mslearn-fabric/Instructions/Labs/03-delta-lake.html))  
Dataset: [`products.csv`](https://github.com/MicrosoftLearning/dp-data/raw/main/products.csv)


## Purpose

This project is a hands-on demo of Delta Tables in Microsoft Fabric using Apache Spark.
The goal is to:

- Practice DP-700 exam skills (data ingestion, transformation, monitoring, optimization).
- Understand how Delta Lake works in Fabric (batch + streaming).
- Document step-by-step what happens behind the scenes, so it’s didactic

## What You’ll Learn

- The difference between Delta Tables vs Parquet (transaction log, ACID guarantees).
- How to ingest data into a Lakehouse.
- How to use PySpark to create and manipulate Delta Tables.
- How to query Delta Tables with SQL endpoints.
- How to implement table versioning and time travel.
- How to extend Delta Tables for streaming analytics.

## Structure

- **notebooks/**
  - `01_setup_workspace_and_lakehouse.ipynb` → init paths, create DBs.
  - `02_create_delta_from_files.ipynb` → managed vs external Delta tables.
  - `03_delta_sql_queries.ipynb` → query Delta tables with SparkSQL.
  - `04_updates_and_time_travel.ipynb` → update rows, check history, time travel.
  - `05_schema_evolution_and_time_travel.ipynb` → evolve schema, revisit history.
  - `90_optional_streaming_to_delta.ipynb` → bonus: ingest IoT events with streaming.
- **sql/**
  - `queries_delta_basics.sql` → sample queries (SELECT, GROUP BY).
  - `queries_time_travel.sql` → versioned queries and history checks.

## Skills Practiced
- PySpark DataFrame API  
- Managed vs external Delta tables  
- Spark SQL queries and views  
- Updates, history, and time travel  
- Schema evolution  
- (Optional) Streaming into Delta