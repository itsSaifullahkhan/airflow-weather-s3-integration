# 🌦️ Weather ETL Pipeline using Apache Airflow, RDS & S3 on AWS

## 📌 Project Overview

This project demonstrates a real-time ETL pipeline built with **Apache Airflow**, hosted on an **AWS EC2 instance**, to automate data integration between the **OpenWeather API** and **Amazon S3**. It performs parallel processing, stores data in **Amazon RDS (PostgreSQL)**, and finally outputs the joined results back into S3 for further analytics or downstream consumption.

---

## 🧰 Tech Stack

- **Apache Airflow** – Workflow orchestration
- **AWS EC2** – Hosting Airflow
- **AWS S3** – Data source and export target
- **AWS RDS (PostgreSQL)** – Central data warehouse
- **OpenWeatherMap API** – Real-time weather data
- **Python** – Data transformation and scripting

---

## ⚙️ What the Pipeline Does

- Fetches weather data from OpenWeather API.
- Reads structured data from a source S3 bucket (e.g., CSV/JSON).
- Processes both data sources in **parallel**.
- Loads each dataset into **separate tables in PostgreSQL** (on RDS).
- Joins the two tables via SQL (INNER JOIN).
- Exports the final enriched dataset back to S3.

---

