# 🚀 Real-Time Data Pipeline with API, AWS Lambda, and Snowflake

This project demonstrates how to design and implement a **real-time data pipeline** using:

- **API integration** for data ingestion  
- **AWS Lambda** for event-driven processing  
- **Snowflake** for scalable data storage & transformation  
- **Power BI** for dashboarding and analytics  

---

## 📌 Architecture

![Architecture](folder/Screenshot%202025-09-30%20125932.png)

The pipeline flow:

1. **API → Lambda** → Fetch & validate data.  
2. **Lambda → S3 Raw Zone** → Store data in JSONL/CSV.  
3. **Snowpipe → Snowflake RAW schema** → Auto-ingest from S3.  
4. **Streams/Tasks → Snowflake CORE schema** → ELT transformations.  
5. **Power BI** → Visualization and analytics.  

---

## 📂 Repository Structure

---

## ⚙️ Technologies Used

- **AWS Lambda** → serverless ingestion & automation  
- **Amazon S3** → raw storage layer  
- **Snowflake** → cloud data warehouse for ELT & analytics  
- **Power BI** → dashboard & visualization  
- **Python** → API fetch, ETL scripts  
- **GitHub Desktop** → version control  

---

## 🚀 How It Works

1. **API Data Fetch**  
   - `Fetch_data_from_API.ipynb` tests API endpoints.  
   - Lambda (`lambda_function.py`) pulls live data from the API.  

2. **Lambda Processing**  
   - Validates & stores JSONL/CSV in S3 (`raw/` prefix).  

3. **Snowflake Ingestion**  
   - `RAW` schema ingests via **Snowpipe**.  
   - Data transformations handled via **Streams** & **Tasks** into `CORE`.  

4. **Visualization**  
   - Power BI connects to `CORE` schema in Snowflake.  
   - Dashboards update automatically via DirectQuery or scheduled refresh.  

---

## 📑 Documentation

- [Solution Methodology (PDF)](folder/Solution%20Methodology%202.pdf)

---

## ⚠️ Dataset Notice

The full dataset (`total_data.csv`) is **not included** in this repository due to GitHub’s 100 MB file size limit.  
👉 Use your own dataset or download from the original source/S3 bucket.  
👉 A small sample (`sample_data/sample_1k.jsonl`) is included for testing.  

---

## 🛠️ Deployment Steps

### 1. Snowflake Setup
- Run `code/snowflake/00_roles_warehouses.sql` → create roles/warehouse.  
- Run `10_raw_objects.sql` → DB, schemas, stage.  
- Run `40_snowpipe.sql` → create pipe, connect to S3 notifications.  

### 2. AWS Setup
- Create S3 bucket (e.g., `rt-pipeline-raw`).  
- Deploy Lambda with environment variables:  

