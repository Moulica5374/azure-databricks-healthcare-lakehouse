
# Azure Databricks Healthcare Lakehouse

## Project Overview

An end-to-end production-grade batch data pipeline that processes 
CMS Medicare public claims data using Azure Databricks and Medallion 
Lakehouse architecture (Bronze → Silver → Gold).

This project mirrors real-world healthcare data engineering workflows 
similar to enterprise-scale pipelines processing millions of Medicare 
claims, beneficiary records, and prescription drug events daily.

### What it does
- Ingests raw CMS Medicare DE-SynPUF claims data (CSV) into Azure 
  Data Lake Storage Gen2
- Transforms raw data through Bronze → Silver → Gold Delta tables 
  using PySpark on Azure Databricks
- Orchestrates the full pipeline via Apache Airflow DAGs with retry 
  logic and alerting
- Governs all Delta tables using Unity Catalog for lineage and 
  access control
- Exposes Gold tables via Azure Synapse Analytics for analyst consumption

### Dataset
CMS DE-SynPUF (Data Entrepreneurs Synthetic Public Use Files) — 
synthetic Medicare claims data published by the Centers for Medicare 
& Medicaid Services. Includes inpatient claims, outpatient claims, 
beneficiary summaries, and prescription drug events spanning 2008-2010.
