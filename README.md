# Amazon_sales_data_analysis

# Amazon Sales Analysis — ETL, EDA, Dashboards  

## 📌 Overview  
A production‑oriented **data science project** that performs ETL on an **Amazon e‑commerce dataset**, analyzes sales trends month‑wise, year‑wise, and yearly‑month‑wise, and surfaces key metrics, drivers, and relationships across products, channels, and regions.  

The repository is **modular, testable, and portable**, and includes guidance for Python workflows and BI dashboards (**Tableau/Power BI**) as required in the brief.  

---

## 🎯 Objectives  
- Build a reliable **ETL pipeline**: extract dataset, transform to clean and feature‑rich tables, and load curated outputs for analysis and dashboards.  
- Compute sales trends **month‑wise, year‑wise, and yearly‑month‑wise**, and surface KPIs such as revenue, cost, profit, units, and margins with time‑series views.  
- Identify **key factors and meaningful relationships** across item types, regions, sales channels, and order priorities, and document findings in a report.  

---

## 📂 Dataset  
- Store the original file under `data/raw` without modification to preserve provenance and reproducibility.  
- Place cleaned and enriched tables under `data/processed` after running the ETL pipeline.  
- Maintain a **data dictionary** for versioning and schema notes.  

---

## 🛠 Tech Stack  
- **Python** with pandas and NumPy for ETL and analysis.  
- **Anaconda** and **Jupyter Notebook** for environment management and exploratory workflows.  
- **Tableau / Power BI** for dashboards.  

---

## 📁 Project Structure  
```
README.md                → Project overview, setup, usage guide  
data/raw/                → Original dataset (immutable source of truth)  
data/processed/          → Cleaned, enriched ETL outputs  
notebooks/               → Exploratory analysis & validation visualizations  
src/etl/                 → Extract, Transform, Load modules  
src/analysis/            → KPI calculations & relationship analyses  
src/viz/                 → Plotting utilities & figure exports  
dashboards/tableau/      → Tableau workbooks/exports  
dashboards/powerbi/      → Power BI .pbix & exports  
tests/                   → Unit tests for ETL & KPIs  
reports/                 → Final report & supporting figures  
```

---

## ⚙️ Installation  
1. Create and activate a **conda environment** (example: `amazon-sales`).  
2. Install dependencies from `requirements.txt`:  
   ```bash
   pip install -r requirements.txt
   ```  
3. Verify imports with a smoke test.  

---

## 🚀 Quick Start  
1. Place the raw dataset under `data/raw`.  
2. Update dataset filenames in `config/config.yml`.  
3. Run the ETL pipeline:  
   ```bash
   python -m src.etl.run
   ```  
   or use `make etl` if Makefile is included.  
4. Processed data will be stored in `data/processed/`.  
5. Execute analysis scripts or notebooks for KPIs & trends.  
6. Open dashboards in Tableau/Power BI and refresh extracts.  

---

## 🔄 ETL Pipeline  
- **Extract:** Load raw CSV/XLSX → standardize columns, types, schema checks.  
- **Transform:** Clean anomalies, derive time features, compute revenue/cost/profit/margins, normalize categoricals.  
- **Load:** Write curated outputs to `data/processed/`.  

---

## 📊 Key Metrics  
- **Totals:** Revenue ≈ 137.35M | Cost ≈ 93.18M | Profit ≈ 44.17M  
- **Averages:** Unit Price ≈ 276.76 | Unit Cost ≈ 191.05 | Profit per order ≈ 0.44M  
- **Units:** Avg. Units Sold ≈ 5.13K/order (2011–2017 series available).  

---

## 📈 Trends & Relationships  
- **Time:** Profit & Units Sold trends across years, months, and year‑month cycles.  
- **Geography:** Sub‑Saharan Africa (~40M revenue) > Europe (~33M) > Asia (~21M).  
- **Category:** Cosmetics highest profit (~14.56M), followed by Household & Office Supplies.  
- **Channels:** Offline ≈ 58% of profit vs Online ≈ 42%.  
- **Priorities:** Distribution varies by region; impacts fulfillment and operations.  

---

## ✅ Reproducibility & Tests  
- Modularized ETL functions with unit tests for parsing, casting, features, and KPIs.  
- Immutable `data/raw` & idempotent outputs ensure consistent dashboards.  
- Documented assumptions, validation checks, and deterministic seeds.  

---

## 📊 BI Dashboards  
- Publish Tableau Public or Power BI artifacts.  
- Filters: Region, Item Type, Channel, Time.  
- Features: Drill‑downs, trend lines, distribution charts.  
- Consistency: Ensure KPI definitions match ETL outputs.  

---

## 📜 Deliverables Checklist  
- Modular **Python ETL & analysis code** with tests.  
- **Dashboards (Tableau/Power BI)** with KPIs & interactivity.  
- **Final report** summarizing findings & recommendations.  

---

## ⚖️ Safety & Data Ethics  
- Do not modify or commit raw data if restricted.  
- Document licenses & transformations clearly.  
- Label units, time ranges, and filters to avoid misinterpretation.  

---

## 📄 License  
MIT License (or as mandated by your organization).  

---

## 🙏 Acknowledgments  
Thanks to stakeholders and reviewers for emphasizing **modularity, safety, testability, maintainability, and clarity**.  

---
