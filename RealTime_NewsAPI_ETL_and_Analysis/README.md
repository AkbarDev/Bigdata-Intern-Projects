# Real-Time NewsAPI ETL & Analysis

## Project Overview

This project implements a real-time **ETL (Extract, Transform, Load)** pipeline that fetches live news data from the **NewsAPI**, processes it using **Python (Pandas)**, and stores it in a **PostgreSQL** database for analysis.

The goal is to demonstrate how to consume external APIs, handle JSON data, and build a persistent data store for downstream analytics.

---

## Tech Stack

| Component | Technology | Description |
|---|---|---|
| **Data Source** | NewsAPI | REST API for breaking news and headlines. |
| **ETL Engine** | Python (Pandas) | Data fetching, cleaning, and transformation. |
| **Database** | PostgreSQL | Relational storage for structured news data. |
| **Visualization** | Matplotlib / Seaborn | Visualizing trends (e.g., top sources, publication times). |
| **Driver** | SQLAlchemy / psycopg2 | Database connectivity. |

---

## Workflow

```mermaid
graph LR
    A[NewsAPI] -->|JSON Response| B[Python Script (Extract)]
    B -->|Pandas DataFrame| C[Data Cleaning (Transform)]
    C -->|SQL Insert| D[PostgreSQL (Load)]
    D -->|SQL Query| E[Analysis & Visualization]
```

---

## Setup & Installation

### 1. Prerequisites
- Python 3.8+
- PostgreSQL Database
- [NewsAPI Key](https://newsapi.org/) (Free tier available)

### 2. Environment Configuration
Copy the template and fill in your credentials:
```bash
cp .env.template .env
```
Edit `.env` with your details:
- `NEWS_API_KEY`: Your API key from newsapi.org
- `DB_HOST`, `DB_PORT`, `DB_NAME`, `DB_USER`, `DB_PASS`

### 3. Install Dependencies
```bash
pip install requests pandas sqlalchemy psycopg2-binary matplotlib seaborn
```

---

## Usage

Open `RealTime_NewsAPI_ETL_and_Analysis.ipynb` in Jupyter Notebook.

1.  **Configure**: Ensure `.env` is set up.
2.  **Run Pipeline**: Execute cells to fetch, clean, and load data.
3.  **Analyze**: View charts showing:
    - Top 10 Tech News Sources
    - News Publication Frequency by Hour

---

## Key Skills Demonstrated

- **API Integration**: Consuming RESTful APIs with authentication.
- **Data Transformation**: Flattening nested JSON structures (dictionaries) into tabular format.
- **ETL Pipeline**: Automating the flow of data from source to storage.
- **SQL Analysis**: Querying time-series and categorical data.

---

## Contact

**Author:** Akbar Basha
**GitHub:** [@AkbarDev](https://github.com/AkbarDev)
