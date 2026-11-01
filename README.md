# E-Commerce-Sales-Data-Analysis
The Data Science project End-to-end Retail Sales EDA with Python, Pandas &amp; Seaborn — data cleaning, feature engineering, and business insights from 230+ transactions across 6 stores.
<div align="center">


## 📌 Project Overview

This project performs a complete **Exploratory Data Analysis (EDA)** on a
retail sales dataset covering **230+ transactions** across **6 stores**
(Jan–Jun 2024).

**Author:** Hassan Mukhtar

---

## 📌 Problem Statement

An E-commerce retail company recorded 228 sales transactions across multiple stores and regions. The raw data was messy:

- Inconsistent text formatting (e.g. `" central"`, `"WEST"`, `"nida_iqbal"`)
- Missing values in `unit_price`, `order_date` and `rating`
- Duplicate rows and duplicate `order_id`s
- No revenue column, only `quantity` and `unit_price`
- Store details (manager, city) kept in a separate table

The goal is to turn this into a clean, analysis-ready dataset and extract business insights.

## 🎯 Objectives

1. Clean and standardise the dataset
2. Merge sales data with the store dimension table
3. Engineer features: `total_amount`, `order_month`, `week_day`, `quarter`, `rating_bucket`
4. Perform EDA (univariate, bivariate and pivot-based summaries)
5. Visualise revenue by category, region and month
6. Export a clean dataset for further data science work

## 🛠️ Tools & Libraries

- Python
- Pandas, NumPy
- Matplotlib, Seaborn
- Jupyter Notebook

## 📂 Project Structure

```
ecommerce-sales-analysis/
├── E-Commerce_Sales___Store_Data_Analysis.ipynb   # Main analysis notebook
├── sales_data.csv                                 # Raw sales transactions
├── stores.csv                                     # Store dimension table
├── clean_sales_data.csv                           # Cleaned output dataset
└── README.md
```

## 🧹 Data Cleaning Steps

| Issue | Treatment |
|-------|-----------|
| Missing `unit_price` | Filled with the median |
| Missing `order_date` | Rows dropped (time analysis needs valid dates) |
| Missing `rating` | Filled with the median rating of each category |
| Duplicate rows / `order_id`s | Removed, keeping the first occurrence |
| Inconsistent text | Stripped whitespace, replaced `_`, applied title case |
| Wrong data types | Converted dates to datetime and prices/ratings to numeric |

## ⚙️ Feature Engineering

- `total_amount` = `quantity` × `unit_price`
- `order_month`, `order_year`, `week_day`, `quarter` extracted from `order_date`
- `rating_bucket`: low (1–2), mid (3), high (4–5)

## 📊 Key Findings

> Update these numbers after re-running the final notebook.

- **Top category:** Appliances generated the highest revenue (~67K), while Accessories generated the lowest (~15K).
- **Top region:** South led in revenue, and Central had the lowest.
- **Monthly trend:** Revenue peaked in May and dipped in April.
- **Ratings:** Most orders fall in the mid rating bucket.

## 📈 Visualisations

- Revenue by category (horizontal bar chart)
- Revenue by region (bar chart)
- Monthly revenue trend (line chart)
- Rating bucket share (pie chart)

## ▶️ How to Run

1. Clone the repository:
   ```
git clone https://github.com/Hassanmukhtaar/E-Commerce-Sales-Data-Analysis.git
cd E-Commerce-Sales-Data-Analysis
   ```
2. Install the dependencies:
   ```
   pip install pandas numpy matplotlib seaborn jupyter
   ```
3. Launch Jupyter and open the notebook:
   ```
   jupyter notebook
   ```
4. Run all cells (**Kernel → Restart & Run All**).

## 🚀 Future Improvements

- Customer segmentation and repeat-purchase analysis
- Sales forecasting with time-series models
- Interactive dashboard (Power BI or Plotly)

## 📬 Contact

**Hassan Mukhtar**
- LinkedIn: www.linkedin.com/in/hassan-mukhtar-753016283
- Email: hassanmukhtar722@gmail.com
