# 🚲 NYC CitiBike Real-Time ETL Pipeline

A **real-time ETL pipeline** that ingests **NYC CitiBike data** using **Apache Kafka**, processes it with **Apache Spark Streaming**, and stores analytics-ready data in a **PostgreSQL data warehouse**. The system includes **data quality checks**, **anomaly detection** (e.g., trips < 60 sec), and a **dashboard** to visualize real-time **trip analytics** and **popular stations**.


## 📌 Features

- **Kafka-based Ingestion**: Real-time ingestion of NYC CitiBike trip data via Kafka producers and consumers.
- **Spark Streaming**: Low-latency, distributed data processing with real-time analytics logic.
- **PostgreSQL Data Warehouse**: Optimized schema for storing and querying cleaned and aggregated data.
- **Data Quality Checks**:
  - Filter incomplete or malformed records
  - Validate timestamp and geolocation fields
- **Anomaly Detection**:
  - Detect trips shorter than 60 seconds
  - Identify invalid station IDs or GPS drift
- **Dashboard Visualization**:
  - Live metrics: trip counts, average durations, and station activity
  - Heatmaps of popular start and end stations
- **Scalable Architecture**:
  - Modular components for scaling ingestion, transformation, and storage layers
- **Monitoring and Logging**:
  - Logging of ingestion rates and processing metrics
  - Error alerting for failed pipeline components
- **Unit and Integration Tests** for pipeline components (Kafka, Spark, and DB)
- **Dockerized Setup**: Containers for Kafka, Spark, PostgreSQL, and the dashboard (optional via Docker Compose)

---

## 🛠️ Tech Stack

- **Data Ingestion**: Apache Kafka
- **Stream Processing**: Apache Spark Streaming
- **Storage**: PostgreSQL
- **Dashboard**: Streamlit / Grafana (configurable)
- **Orchestration**: Apache Airflow (optional)
- **Containerization**: Docker, Docker Compose

---

## 🚀 Getting Started

### Prerequisites

- Docker & Docker Compose
- Python 3.8+
- Java 8+
- Apache Spark installed (if running locally)
- PostgreSQL client (psql)

### Quickstart with Docker

```bash
git clone https://github.com/your-username/nyc-citibike-etl.git
cd nyc-citibike-etl
docker-compose up --build
