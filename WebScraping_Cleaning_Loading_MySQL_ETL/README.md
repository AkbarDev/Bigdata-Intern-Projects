# Web Scraping, Cleaning & Loading to MySQL ETL Pipeline

## Project Overview

This project implements an **ETL (Extract, Transform, Load)** pipeline that scrapes book data from a public website, cleans and structures the data using **Python (Pandas)**, and loads it into a **MySQL** database.

The goal is to demonstrate web scraping techniques, data transformation, and database integration in a unified workflow.

---

## Tech Stack

| Component | Technology | Description |
|---|---|---|
| **Source** | Books to Scrape | A sandbox website for scraping practice. |
| **Extraction** | Requests, BeautifulSoup | Fetching and parsing HTML content. |
| **Transformation** | Pandas | Cleaning data (e.g., currency conversion, binary flags). |
| **Loading** | SQLAlchemy / PyMySQL | Storing data in a MySQL database. |
| **Database** | MySQL | Relational database management system. |

---

## Workflow

```mermaid
graph LR
    A[Web Source] -->|HTML| B[Python Script (Scrape)]
    B -->|Raw Data| C[Pandas (Clean & Transform)]
    C -->|DataFrame| D[MySQL Database (Load)]
    D -->|SQL Query| E[Verification]
```

---

## Setup & Installation

### 1. Prerequisites
- Python 3.8+
- MySQL Database Server
- Internet connection (for scraping)

### 2. Environment Configuration
Copy the template and fill in your credentials:
```bash
cp .env.template .env
```
Edit `.env` with your details:
- `DB_HOST`, `DB_PORT`, `DB_NAME`, `DB_USER`, `DB_PASS`

### 3. Install Dependencies
```bash
pip install requests beautifulsoup4 pandas sqlalchemy pymysql ipython-sql
```

---

## Usage

Open `WebScraping_Cleaning_Loading_MySQL_ETL.ipynb` in Jupyter Notebook.

1.  **Configure**: Ensure `.env` is set up correctly.
2.  **Run Pipeline**: Execute the cells to scrape, clean, and load data.
3.  **Verify**: The final cells use SQL magic commands to query the database and verify the data load.

---

## Key Skills Demonstrated

- **Web Scraping**: Extracting specific data points from HTML structures.
- **Data Cleaning**: converting string currency to floats, normalizing text.
- **Database Integration**: Using SQLAlchemy to write DataFrames directly to SQL tables.
- **Automation**: Creating a repeatable script for data ingestion.

---

## Contact

**Author:** Akbar Basha
**GitHub:** [@AkbarDev](https://github.com/AkbarDev)
