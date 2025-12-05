# PostgreSQL Data Transformation & Analysis

## Project Overview

This project demonstrates an end-to-end **ETL (Extract, Transform, Load)** and **Data Analysis** workflow using **PostgreSQL** and **Python**. It showcases how to programmatically interact with a relational database, generate synthetic data, load it into tables, and perform analytical queries and visualizations.

The project simulates an airline passenger data scenario, providing insights into passenger demographics and flight patterns.

---

## Tech Stack

| Component | Technology | Description |
|---|---|---|
| **Database** | PostgreSQL | Robust, open-source relational database system. |
| **ORM/Driver** | SQLAlchemy / psycopg2 | Python SQL toolkit and adapter for database communication. |
| **Data Manipulation** | Pandas | Library for data structures, cleaning, and analysis. |
| **Visualization** | Matplotlib / Seaborn | Tools for creating static and interactive plots. |
| **Language** | Python 3.12 | Core programming language. |

---

## Workflow

```mermaid
graph LR
    A[Start] --> B[Connect to DB (SQLAlchemy)]
    B --> C[Generate Synthetic Data (Pandas)]
    C --> D[Load Data to PostgreSQL (to_sql)]
    D --> E[Execute Analytical Queries (read_sql)]
    E --> F[Visualize Results (Seaborn)]
    F --> G[End]
```

---

## Setup & Installation

### 1. Prerequisites
- Python 3.8+
- A running PostgreSQL instance (local or remote)
- Database credentials

### 2. Environment Configuration
Copy the template and fill in your credentials:
```bash
cp .env.template .env
```
Edit `.env` with your details:
- `DB_HOST`, `DB_PORT`, `DB_NAME`, `DB_USER`, `DB_PASS`

### 3. Install Dependencies
```bash
pip install pandas sqlalchemy psycopg2-binary matplotlib seaborn
```

---

## Usage

Open `PostgreSQL_Data_Transformation_Analysis.ipynb` in Jupyter Notebook.

1.  **Run Cells**: Execute the notebook sequentially.
2.  **Verify Data**: Check your PostgreSQL database to see the `aero_passengers` table populated with 100 rows.
3.  **View Insights**: The notebook will display charts for:
    - Average Passenger Age by Travel Class
    - Top 5 Flight Destinations

---

## Key Skills Demonstrated

- **Database Engineering**: Designing schemas and loading data efficiently.
- **Python-SQL Integration**: Using SQLAlchemy engines for seamless DataFrame persistence.
- **Data Analysis**: Writing SQL aggregations (`GROUP BY`, `AVG`, `COUNT`) and visualizing results.
- **Best Practices**: Managing credentials securely via environment variables.

---

## Contact

**Author:** Akbar Basha
**GitHub:** [@AkbarDev](https://github.com/AkbarDev)
