# Senior Data Associate – Database Design Assignment

Author: Navneet Mishra  

---

## Overview

This project focuses on designing and implementing a relational database to store and analyze high-volume Futures & Options (F&O) trading data.  

The objective of this assignment is to demonstrate skills in:

- Database schema design
- SQL querying for financial analytics
- Query optimization
- Handling large-scale trading datasets

The dataset used contains Futures and Options trading data including symbols, expiry dates, strike prices, OHLC prices, trading volume, open interest, and timestamps.

---

## Dataset

Dataset Used: **NSE Future and Options Dataset (3 Months)**

The dataset contains the following columns:

- Instrument
- Symbol
- Expiry Date
- Strike Price
- Option Type
- Open, High, Low, Close prices
- Settle Price
- Contracts / Volume
- Open Interest
- Timestamp

The schema is designed in a way that it can support multiple exchanges such as:

- NSE
- BSE
- MCX

by including an `exchange` column.

---

## Tools & Technologies

The following tools were used in this project:

- Python
- DuckDB
- SQL
- Jupyter Notebook
- Git
- GitHub

---

## Database Design

The database schema follows **Third Normal Form (3NF)** to eliminate redundancy and maintain data integrity.

The design separates the data into multiple entities:

### Instruments
Stores unique financial instruments such as NIFTY, BANKNIFTY, etc.

### Expiries
Stores expiry dates and strike prices for options contracts.

### Exchanges
Stores exchange information such as NSE, BSE, and MCX.

### Trades
Stores trading data including:

- OHLC prices
- Volume
- Open Interest
- Timestamp

This schema allows efficient storage and querying of large trading datasets.

---

## SQL Analysis Queries

The following analytical SQL queries were implemented:

1. Top 10 symbols by Open Interest
2. 7-day rolling volatility using window functions
3. Cross-exchange settlement price comparison
4. Option chain volume summary grouped by expiry and strike price
5. Maximum trading volume analysis
6. Query optimization using EXPLAIN

These queries demonstrate financial data analysis capabilities using SQL.

---

## Performance Optimization

To improve query performance, indexing strategies were considered on the following columns:

- Symbol
- Timestamp
- Exchange

Indexes improve performance for filtering and time-series analysis queries.

Additionally, the **EXPLAIN query plan** was used to analyze query execution and optimize performance.
## Project Structure
fno-data-assignment
│
├── assignment.ipynb # Jupyter notebook with data loading and SQL queries
├── queries.sql # SQL queries used for analysis
├── ER_diagram.png # Entity Relationship Diagram
├── reasoning.pdf # Explanation of database design and optimization
├── 3mfanddo.csv # Dataset used for analysis
└── README.md # Project documentation


---

## How to Run the Project

1. Clone the repository
git clone https://github.com/Navneet308097/fno-data-assignment.git
2. Install required libraries
pip install duckdb pandas
3. Open the Jupyter Notebook
assignment.ipynb


4. Run all cells to load the dataset and execute SQL queries.

---

## Conclusion
This project demonstrates how a relational database can be designed and optimized for analyzing large-scale financial trading datasets.
By applying normalization, SQL analytics, and query optimization techniques, the system supports efficient financial data analysis and can scale to handle millions of trading records.

## Project Structure
