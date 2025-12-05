# MySQL/MariaDB Connection and Querying

## Project Overview

This project demonstrates how to connect to **MySQL** or **MariaDB** databases using Python. It covers two primary approaches:
1.  **Programmatic Access**: Using `mysql-connector-python` for application development and ETL scripts.
2.  **Interactive Analysis**: Using `ipython-sql` magic commands to write SQL directly within Jupyter Notebook cells.

The notebook includes examples of Data Definition Language (DDL) for creating tables and Data Manipulation Language (DML) for inserting and querying data.

---

## Tech Stack

| Component | Technology | Description |
|---|---|---|
| **Database** | MySQL / MariaDB | Relational database management system. |
| **Driver** | `mysql-connector-python` | Official Oracle driver for connecting Python to MySQL. |
| **ORM/Toolkit** | `sqlalchemy` | SQL toolkit used by `ipython-sql` for connections. |
| **Extension** | `ipython-sql` | Jupyter extension for running SQL magic commands. |
| **Language** | Python 3.12 | Core programming language. |

---

## Workflow

```mermaid
graph TD
    A[Start] --> B[Load Credentials (.env)]
    B --> C{Choose Method}
    C -->|Method 1: Python Driver| D[Connect via mysql.connector]
    D --> E[Execute Cursor Commands]
    E --> F[Fetch Results]
    C -->|Method 2: SQL Magic| G[Load %sql Extension]
    G --> H[Connect via SQLAlchemy String]
    H --> I[Run %%sql Cells]
    F --> J[End]
    I --> J
```

---

## Setup & Installation

### 1. Prerequisites
- Python 3.8+
- A running MySQL or MariaDB server (local or remote)
- Database credentials

### 2. Environment Configuration
Copy the template and fill in your credentials:
```bash
cp .env.template .env
```
Edit `.env` with your details:
- `DB_HOST`, `DB_USER`, `DB_PASS`, `DB_NAME`

### 3. Install Dependencies
```bash
pip install mysql-connector-python sqlalchemy ipython-sql
```

---

## Usage

Open `MySQL_MariaDB_Connection_and_Querying.ipynb` in Jupyter Notebook or VS Code.

1.  **Configure**: Ensure the `.env` file is set up correctly.
2.  **Run Method 1**: Execute the cells to see how to create tables and insert data using Python code.
3.  **Run Method 2**: Execute the cells to write SQL queries directly (e.g., `SELECT * FROM employees`).

---

## Key Skills Demonstrated

- **Database Connectivity**: Establishing secure connections to RDBMS.
- **SQL Proficiency**: Writing DDL (CREATE) and DML (INSERT, SELECT) queries.
- **Python Integration**: Handling cursors, transactions, and result sets.
- **Interactive Analytics**: Leveraging Jupyter magic commands for efficient data exploration.

---

## Future Enhancements

- **ORM Integration**: Use SQLAlchemy ORM for object-oriented database interaction.
- **Data Visualization**: Plot query results directly using `matplotlib` or `seaborn`.
- **Migration Scripts**: Create scripts to handle database schema changes.

---

## Contact

**Author:** Akbar Basha
**GitHub:** [@AkbarDev](https://github.com/AkbarDev)
