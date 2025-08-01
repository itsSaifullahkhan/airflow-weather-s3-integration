# 🌦️ Weather ETL Pipeline with Apache Airflow, RDS & S3 on AWS

This project implements a real-time ETL pipeline using **Apache Airflow**, hosted on an **EC2 instance**, to integrate and process weather data from the **OpenWeather API** and files from **Amazon S3**. The data is stored in **Amazon RDS (PostgreSQL)**, joined, and the final output is exported back to S3.

---

## 📊 Architecture

Below is the architecture of the pipeline:

![Architecture](./Project%20Architecture.png)

---

## ⚙️ How It Works

1. **Apache Airflow (on EC2)** triggers the pipeline.
2. Weather data is fetched from **OpenWeather API**, transformed via Python, and loaded into **RDS PostgreSQL**.
3. Simultaneously, structured data (e.g., `.csv` or `.json`) is read from an **S3 bucket** and stored into another RDS table.
4. Both tables are then **joined (INNER JOIN)** to enrich the dataset.
5. The final joined data is exported back into a designated folder in the **S3 bucket**.

---

## 🧰 Tech Stack

- **Apache Airflow** – DAG orchestration
- **AWS EC2** – Host for Airflow
- **AWS S3** – Source and final destination
- **AWS RDS (PostgreSQL)** – Relational data store
- **OpenWeather API** – Real-time weather source
- **Python** – Transformation logic

---

## 🗂️ Project Structure

