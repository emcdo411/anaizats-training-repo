# 🌟 North Star Project 2: Azure Data Pipeline to RShiny

## 🎯 Objective:
Learn how to move data securely and efficiently from a **SQL Server database** to a **cloud storage environment** using **Azure Data Factory**, and then visualize it in a **RShiny dashboard**.

This helps bridge local development skills with scalable, cloud-ready solutions — essential for roles in cloud data engineering or full-stack analytics.

---

## 🧠 Prompt:

I want you to act as a Cloud Data Engineer and AI Mentor. I’m ready to step into the cloud space and want a beginner-friendly project that gives me hands-on experience using **Azure Data Factory (ADF)**.

Here’s my goal:

> Use Azure Data Factory to extract data from a SQL Server database, load it into Azure Blob Storage or Data Lake, and connect that data to an **RShiny dashboard** for analysis.

Please walk me through:

1. A simple **cloud architecture diagram** that includes:
   - SQL Server as source
   - ADF as ETL
   - Azure Blob or Data Lake Storage
   - RShiny or RMarkdown consuming the cloud data

2. **Azure setup steps** with links or tips:
   - Resource group, storage account, Data Factory creation

3. **Beginner-friendly ADF pipeline steps**:
   - Linked service
   - Dataset setup
   - Pipeline with Copy Activity
   - Data validation

4. A **sample dataset schema** for testing the pipeline

5. R code snippet to **connect to Azure Blob** or download the file using `AzureStor`, `httr`, or `curl`

6. RShiny code that:
   - Reads the downloaded cloud file
   - Builds a basic visual (bar plot or time trend)

7. Bonus: Tips on **automating this process**, setting up **email alerts**, or **rescheduling pipelines** in ADF

---

## 🧰 Tools & Skills Introduced:
- Azure Data Factory basics
- ETL logic
- Blob Storage navigation
- RShiny integration with remote/cloud data
- Resume-ready cloud project structure

---

## ✅ Ideal Output:
- Deployed ADF pipeline that runs successfully
- Cloud-hosted `.csv` or `.json` file from SQL data
- R code that fetches and analyzes cloud data
- Optional GitHub repo with:
  - `/etl/` folder for Azure config JSONs
  - `/rshiny/` folder with app UI + server code
  - `README.md` summarizing tools and learning

---

## 🚀 Project 3 Suggestion (Next Step):
> Build a minimal **AI prediction model** in R that uses the cloud data and deploys via **Plumber API** or RShiny — moving toward ML deployment.

