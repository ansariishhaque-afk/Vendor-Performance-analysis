📊 Vendor Performance Analysis

📖 Project Overview

This project analyzes vendor performance using structured inventory, purchase, sales, and invoice data stored in a SQLite database.
The goal is to transform raw transactional data into meaningful business insights that support procurement decisions, cost optimization, and revenue growth.
The analysis is performed using Python (Pandas) and SQL within a Jupyter Notebook environment.

🎯 Business Objectives

✔ Evaluate vendor-wise purchase performance
✔ Analyze brand-level profitability
✔ Compare purchase price vs actual pricing
✔ Assess freight cost impact
✔ Identify high-revenue brands
✔ Support strategic procurement decisions

🛠 Tech Stack
Technology	Purpose
Python	Data processing
Pandas	Data manipulation
SQLite	Database storage
SQLAlchemy	Database engine
SQL	Querying & aggregation
Jupyter Notebook	Analysis environment

🗂 Project Structure

Vendor-Performance-Analysis/
│
├── vendor performance analysis.ipynb
├── inventory.db
└── README.md

🗄 Database Architecture

The SQLite database (inventory.db) stores structured tables including:

purchases
purchase_prices
sales
vendor_invoice

Data is ingested using a reusable function:

def ingest_db(df, table_name, engine):
    df.to_sql(table_name, con=engine, if_exists='replace', index=False)

This ensures clean and consistent table updates.

🔎 Exploratory Data Analysis

The notebook performs SQL-driven EDA to evaluate vendor performance.

🛒 1. Purchase Analysis

Vendor-wise purchase quantity
Brand-level purchase cost
Total procurement spending

Purpose: Identify high-volume vendors and spending concentration.

💰 2. Purchase Price Comparison

Listed purchase price vs actual price
Volume impact on pricing
Brand-level pricing trends

Purpose: Detect pricing inconsistencies and cost-saving opportunities.

🧾 3. Vendor Invoice Analysis

Total purchase orders (PO count)
Freight cost aggregation
Invoice distribution

Purpose: Measure transaction frequency and logistical cost burden.

📈 4. Sales Performance Analysis

Brand-wise revenue
Sales quantity trends
Sales price evaluation

Purpose: Identify top-performing brands and revenue drivers.

🔗 5. Join Analysis (Purchases + Pricing)

SQL JOIN operations calculate:
Total purchase dollars
Price deviations
Vendor-level aggregation
Brand-level performance

Purpose: Compare negotiated vs actual pricing and evaluate vendor efficiency.

📊 Key Insights

Certain vendors contribute significantly to procurement cost.
Freight cost impacts overall vendor profitability.
Brand-level revenue distribution is uneven.
Pricing discrepancies highlight negotiation opportunities.
High-volume purchases influence cost structure.

▶️ How to Run
1️⃣ Install Dependencies
pip install pandas sqlalchemy
2️⃣ Launch Jupyter Notebook
jupyter notebook
3️⃣ Run the Notebook

Execute all cells sequentially to:

Ingest data into SQLite
Connect to the database
Perform SQL-based analysis
Generate business insights

🚀 Future Improvements

Add data visualizations (Matplotlib / Seaborn)
Create an interactive dashboard (Power BI / Tableau)
Implement KPI scoring model
Automate vendor ranking system
Add profitability margin analysis

📈 Business Impact

This project demonstrates:

Data-driven vendor evaluation
Cost optimization strategies
SQL + Python integration
Business analytics workflow
Procurement intelligence
