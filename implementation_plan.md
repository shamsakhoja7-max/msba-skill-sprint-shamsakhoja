# Implementation Plan – ETL Pipeline


## Goal:
This project demonstrates how a batch ETL (Extract, Transform, Load) pipeline works.

It automatically:
1. Pulls raw source data
2. Cleans and structures the data
3. Loads the results into a SQLite database file

After the pipeline runs, the database contains analytics-ready tables that can be used for reporting, dashboards, or machine learning.


## Using this at a real company may require:

Several upgrades would be required for production use.

### 1. Data Sources
Instead of small demo datasets, a company would pull data from:
- CRM systems
- billing platforms
- product usage logs
- marketing systems
- APIs or cloud storage

### 2. Database
SQLite is good for learning, but companies typically load into:
- Snowflake
- BigQuery
- SQL Server or Postgres

### 3. Automation & Scheduling
The job would run automatically (daily or weekly) using tools such as:
- Airflow
- Prefect
- cloud schedulers (Google Cloud Scheduler, AWS EventBridge,Azure Logic Apps)

### 4. Monitoring
We would add:
- row count validation
- missing value checks
- failure alerts
- logging

### 5. Business Outputs
The resulting tables would feed:
- churn models
- marketing campaigns
- executive dashboards
- customer health metrics


## My Execution:

I successfully installed dependencies and executed the pipeline.

The run produced a database file named:
`db.sqlite`

Inside the database, the pipeline created tables such as:
- population
- unemployment

I also queried the tables and confirmed records exist.

Please see the screenshots in the `/screenshots` folder for evidence of:
1. Repository cloned  
2. Requirements installed  
3. Pipeline execution  
4. Tables and rows present in SQLite  
