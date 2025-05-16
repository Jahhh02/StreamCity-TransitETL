# StreamCity-TransitETL
A real-time ETL pipeline that ingests NYC CitiBike data using Kafka, processes it with Spark Streaming, and stores analytics-ready data in a PostgreSQL data warehouse. It includes data quality checks, anomaly detection (e.g., trips &lt; 60 sec), and a dashboard to visualize trip counts and popular stations.
