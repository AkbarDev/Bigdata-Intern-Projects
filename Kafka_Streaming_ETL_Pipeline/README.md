# Real-Time Twitter Data Pipeline with Kafka, PostgreSQL, and PySpark

## Project Overview

This project implements a scalable, real-time ETL pipeline that ingests social media data (tweets), streams it through a message queue, stores it in a relational database, and performs analytical transformations using a distributed processing engine.

### Key Features
- **Real-Time Ingestion**: Fetches live tweets using the Twitter API v2.
- **Streaming Architecture**: Decouples producers and consumers using Apache Kafka.
- **Persistent Storage**: Loads raw data into PostgreSQL for reliability.
- **Batch/Stream Processing**: Uses PySpark for scalable data transformation (e.g., text normalization).
- **Secure Configuration**: Manages sensitive credentials via environment variables.

---

## Tech Stack

| Component | Technology | Description |
|---|---|---|
| **Data Source** | Twitter API v2 | Fetches tweets based on keywords (e.g., "AI"). |
| **Message Broker** | Apache Kafka | Handles high-throughput real-time data streaming. |
| **Database** | PostgreSQL | Stores raw and transformed tweet data. |
| **Processing** | PySpark | Performs distributed data transformations. |
| **Language** | Python 3.12 | Core logic for producers, consumers, and Spark jobs. |
| **Containerization** | Docker | (Optional) Hosts Kafka and PostgreSQL services. |

---

## Workflow

```mermaid
graph LR
    A[Twitter API] -->|Tweepy| B[Kafka Producer]
    B -->|Topic: tweet-crawl| C[Apache Kafka]
    C -->|Kafka Consumer| D[PostgreSQL (tweet_merge)]
    D -->|JDBC Read| E[PySpark]
    E -->|Transform| F[PostgreSQL (tweet_transformed)]
```

---

## Setup & Installation

### 1. Prerequisites
- Python 3.8+
- Docker & Docker Compose (recommended for Kafka/Postgres)
- Twitter Developer Account (Bearer Token)

### 2. Environment Configuration
Copy the template and fill in your credentials:
```bash
cp .env.template .env
```
Edit `.env` with your details:
- `TWITTER_BEARER_TOKEN`
- `DB_USER`, `DB_PASS`

### 3. Infrastructure Setup (Docker)
Start Kafka and PostgreSQL containers:
```bash
docker-compose up -d
```
*Note: Ensure you have a `docker-compose.yml` configured with Zookeeper, Kafka, and Postgres.*

### 4. Install Dependencies
```bash
pip install -r requirements.txt
```
*(Or install manually: `pip install tweepy kafka-python psycopg2-binary pyspark`)*

---

## Usage

The pipeline is contained within the Jupyter Notebook `Kafka_Streaming_ETL_Pipeline.ipynb`.

1.  **Run Producer**: Execute Part 1 to start fetching tweets and sending them to Kafka.
2.  **Run Consumer**: Execute Part 2 to consume messages and save them to the `tweet_merge` table.
3.  **Run Transformation**: Execute Part 3 to process data with Spark and save to `tweet_transformed`.

---

## Key Skills Demonstrated

- **Data Engineering**: Building end-to-end ETL pipelines.
- **Streaming Technologies**: Implementing Kafka producers and consumers.
- **Big Data Processing**: Using PySpark for data manipulation.
- **Database Management**: Integrating Python/Spark with PostgreSQL via JDBC.
- **API Integration**: Handling external data sources (Twitter).

---

## Future Enhancements

- **Sentiment Analysis**: Add an NLP model in the Spark step to classify tweets.
- **Dashboarding**: Connect Grafana or Metabase to PostgreSQL for real-time visualization.
- **Airflow Orchestration**: Schedule the Spark job to run at regular intervals.
- **Cloud Deployment**: Deploy infrastructure on AWS (MSK, RDS, EMR).

---

## Contact

**Author:** Akbar Basha
**GitHub:** [@AkbarDev](https://github.com/AkbarDev)
