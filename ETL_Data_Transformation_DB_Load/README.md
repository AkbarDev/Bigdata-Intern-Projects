# ETL Data Transformation & DB Load

## Project Overview

This project implements a classic **ETL (Extract, Transform, Load)** pipeline using the **Titanic dataset**. It demonstrates how to ingest raw data, perform essential data cleaning and transformation tasks using **Pandas**, and persist the results into a **PostgreSQL** database.

The project highlights the transition from raw, messy data to structured, query-ready tables.

---

## Tech Stack

| Component | Technology | Description |
|---|---|---|
| **Data Processing** | Python (Pandas) | Library for data manipulation and analysis. |
| **Database** | PostgreSQL | Relational database for storing processed data. |
| **ORM** | SQLAlchemy | Toolkit for SQL operations and object-relational mapping. |
| **Dataset** | Seaborn (Titanic) | Built-in dataset used for demonstration purposes. |

---

## Workflow

```mermaid
graph LR
    A[Raw Data (Titanic)] -->|Extract| B[Pandas DataFrame]
    B -->|Transform| C[Clean & Aggregate]
    C -->|Load| D[PostgreSQL Database]
    D -->|Query| E[Final Analysis]
```

---

## Setup & Installation

### 1. Prerequisites
- Python 3.8+
- PostgreSQL Database

### 2. Environment Configuration
Copy the template and fill in your credentials:
```bash
cp .env.template .env
```
Edit `.env` with your details:
- `DB_HOST`, `DB_PORT`, `DB_NAME`, `DB_USER`, `DB_PASS`

### 3. Install Dependencies
```bash
pip install pandas sqlalchemy psycopg2-binary seaborn
```

---

## Usage

Open `ETL_Data_Transformation_DB_Load.ipynb` in Jupyter Notebook.

1.  **Configure**: Ensure `.env` is set up.
2.  **Run Pipeline**: Execute cells to load, clean, and save data.
3.  **Verify**: The notebook includes SQL queries to verify the data was loaded correctly.

---

## Key Skills Demonstrated

- **Data Cleaning**: Handling missing values (imputation) and normalizing column names.
- **Transformation**: Creating pivot tables and aggregations for insights.
- **Database Engineering**: Designing schemas and loading data programmatically.
- **ETL Architecture**: Building a sequential pipeline from source to destination.

---

## Contact

**Author:** Akbar Basha
**GitHub:** [@AkbarDev](https://github.com/AkbarDev)
