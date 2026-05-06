# Enterprise-Database-Analytics-Platform
# World Cup Data Platform (OLTP → Warehouse → Spark)

## Overview
This project builds an end-to-end data pipeline using FIFA World Cup data. It starts with a normalized OLTP database, transforms it into a star schema data warehouse, and performs scalable analysis in Databricks using Spark and Python.

------

## Tech Stack
- SQL (Oracle + Spark SQL)  
- Python (PySpark)  
- Databricks (PySpark + Visualization Tools)
- Apache Spark  
- ETL & Data Warehousing
- Draw.io

---

## Phase 1 — OLTP (Oracle + PL/SQL)
- Built a normalized (3NF) database for tournaments, teams, matches, and stats  
- Created PL/SQL packages for business logic:
  - Recording match results  
  - Advancing teams through stages  
  - Generating reports  
- Implemented validation, calculations, and error handling  

---

## Phase 2 — Data Warehouse (SQL + ETL)
- Designed a star schema:
  - Fact: `FACT_MATCH_TEAM_PERFORMANCE`  
  - Dimensions: `DIM_TEAM`, `DIM_MATCH`, `DIM_STAGE`, `DIM_DATE`, `DIM_TOURNAMENT`  
- Built ETL procedures to transform OLTP data into analytical format  
- Ran analytical queries using:
  - `GROUP BY`, `ROLLUP`, `CUBE`  
  - `RANK()` and `CASE`  

---

## Phase 3 — Big Data (Databricks + Spark + Python)
- Exported warehouse tables to CSV and loaded into Databricks  
- Recreated analysis using **Spark SQL**  
- Built additional logic using **PySpark (Python DataFrames)**  
- Created visualizations and dashboard components  

### Key Analysis
- Total goals by team and stage  
- Team rankings and performance trends  
- Multi-dimensional analysis (team vs stage)  
- Custom matchup difficulty score (PySpark)  

---

## Cross-Platform Insights
- **Oracle SQL** → structured, transactional queries  
- **Spark SQL** → similar syntax, but runs on distributed data  
- **PySpark (Python)** → flexible, programmatic analysis  

---

## Scalability
Oracle runs on a single machine and is optimized for transactions.  
Spark distributes data across multiple nodes, allowing efficient processing of very large datasets.
