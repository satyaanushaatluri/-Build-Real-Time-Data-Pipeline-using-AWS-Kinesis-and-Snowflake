# 🚀 Build Real-Time Data Pipeline with API, Lambda, and Snowflake

This project demonstrates how to design and implement a **real-time data pipeline** using:
- **API integration** for data ingestion
- **AWS Lambda** for event-driven processing
- **Snowflake** for scalable data storage & transformation
- **Power BI** for dashboarding and analytics

---

## 📌 Architecture
![Architecture](docs/architecture.png)

---

## 📂 Repository Structure

---

## ⚙️ Technologies Used
- **AWS Lambda** → serverless function for pipeline automation  
- **Snowflake** → cloud data warehouse for storage & queries  
- **Power BI** → dashboard and visualization  
- **Python** → API fetch, ETL scripts, notebooks  
- **GitHub Desktop** → version control  

---

## 🚀 How It Works
1. **API Data Fetch** → scripts in `code/Fetch_data_from_API.ipynb` fetch data from an external API.  
2. **Lambda Processing** → `code/lambda_function.py` handles real-time data ingestion.  
3. **Snowflake Storage** → data is loaded into Snowflake tables for analytics.  
4. **Visualization** → Power BI dashboard (`code/snowflake-dashboard.pbix`) shows insights.  

---

## 📑 Documentation
- [Solution Methodology (PDF)](docs/Solution-Methodology.pdf)

---

## ⚠️ Dataset Notice
The full dataset (`total_data.csv`) is **not included** in this repository due to GitHub’s 100 MB file size limit.  
👉 Use your own dataset or download from the original source/S3 bucket.  

---

## ✨ Author
**Satya Anusha Atluri**
