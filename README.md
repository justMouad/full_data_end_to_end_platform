# Real-Time Application Metrics Dashboard

An end-to-end real-time data engineering project that demonstrates how to ingest, process, store, and visualize application metrics using Apache Kafka, Apache Spark, PostgreSQL, and Plotly Dash.

The project simulates an application monitoring environment in which metric events are continuously generated, streamed through Kafka, processed by Spark Structured Streaming, and stored in PostgreSQL for real-time visualization.

## Architecture Overview

The system follows a streaming data pipeline architecture:

1. **Data Generation:** Simulated application metrics are generated and published as events.
2. **Data Ingestion:** Apache Kafka receives and buffers incoming metric events through dedicated topics.
3. **Stream Processing:** Apache Spark consumes Kafka messages, processes incoming events, and performs aggregations.
4. **Data Storage:** Processed metrics are persisted in PostgreSQL for querying and analysis.
5. **Visualization:** Plotly Dash retrieves the processed data and presents it through an interactive real-time dashboard.

## Technology Stack

| Technology | Role |
|---|---|
| Apache Kafka | Distributed event streaming and message buffering |
| Apache Spark | Real-time stream processing and aggregations |
| PostgreSQL | Persistent storage for processed application metrics |
| Plotly Dash | Interactive dashboard and data visualization |
| Docker | Containerization of application services |
| Docker Compose | Multi-container infrastructure orchestration |

## Key Features

- **Real-Time Data Processing:** Ingest and process streaming application metrics using Kafka and Spark.
- **Interactive Dashboard:** Visualize application metrics through dynamic charts and interactive components using Plotly Dash.
- **Modular Architecture:** Separate data generation, ingestion, processing, storage, and visualization components.
- **Persistent Storage:** Store processed metrics in PostgreSQL for historical analysis and querying.
- **Containerized Infrastructure:** Run the entire environment using Docker and Docker Compose.
- **Extensible Design:** Adapt the pipeline to different application monitoring and observability use cases.

## System Architecture

```text
       Application Metrics Generator
                    |
                    v
             Apache Kafka
                    |
                    v
          Apache Spark Streaming
                    |
                    v
               PostgreSQL
                    |
                    v
              Plotly Dash
                    |
                    v
          Interactive Dashboard