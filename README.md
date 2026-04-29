# Synthetic Data Analytics Project

## Project Objective

This project simulates a real-world data analytics workflow using synthetic datasets. It demonstrates the full data pipeline — from data generation and ETL processing to analytical storage and visualization.

The main goals of the project are:

* Simulate real-world data analysis scenarios using synthetic data
* Apply practical skills in Python, ETL pipelines, and data visualization
* Build an end-to-end data pipeline (Airflow → ClickHouse → Superset)
* Create interactive dashboards for data exploration

---

##  Tools & Technologies

| Category            | Tools Used                            |
| ------------------- | ------------------------------------- |
| Programming         | Python 3.8+                           |
| Data Processing     | Pandas, NumPy                         |
| Synthetic Data      | SDV, CTGAN, GaussianCopulaSynthesizer |
| ETL & Orchestration | Apache Airflow                        |
| Database            | ClickHouse                            |
| BI Dashboard        | Apache Superset                       |
| Containerization    | Docker, Docker Compose                |

---

## Dataset Description

| File                | Description                             |
| ------------------- | --------------------------------------- |
| `cks_synthetic.csv` | Family categories and filtering dataset |
| `kezekte_dummy.csv` | Social queue data of families in need   |
| `e_obr_dummy.csv`   | Government service application history  |

---

## Project Architecture

```
Synthetic Data → Python (Processing) → Airflow (ETL) 
→ ClickHouse (Storage) → Superset (Visualization)
```

---

## How to Run Locally

### 1. Clone the repository

```bash
git clone https://github.com/your-username/synthetic-project.git
cd synthetic-project
```

---

### 2. Start services

```bash
docker-compose up --build
```

---

### 3. Upload data

Place CSV files into the `/data` directory (if not already included).

---

### 4. Access services

* **Airflow** → [http://localhost:8080](http://localhost:8080)
* **Superset** → [http://localhost:8088](http://localhost:8088)
* **ClickHouse** → [http://localhost:8123](http://localhost:8123)

---

### 5. Run ETL Pipeline

* Open Airflow UI
* Run DAG: `cks_load_to_clickhouse`
* Data will be automatically loaded into ClickHouse

---

### 6. Build dashboards

* Log into Superset
* Connect to ClickHouse
* Create dashboards and visualizations

---

## Key Features

* End-to-end ETL pipeline using Airflow
* High-performance analytical storage with ClickHouse
* Synthetic data generation for safe experimentation
* Interactive dashboards in Apache Superset
* Containerized environment for easy deployment

---

## Notes

* This project uses synthetic data and does not contain real personal information
* Designed for educational and demonstration purposes
