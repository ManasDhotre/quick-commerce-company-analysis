# Quick Commerce Platform Analysis 🛵📦

End-to-end analysis of a **quick commerce orders dataset** spanning platforms like Swiggy Instamart, Blinkit, Zepto, and BigBasket Now — covering revenue comparison, delivery efficiency scoring, customer rating distributions, discount impact, and city-wise expansion recommendations, culminating in a **mini KPI dashboard**.

---

## Project Overview

This is the most technically advanced project in this portfolio — going beyond basic EDA to include outlier removal, group-wise imputation, MinMaxScaler normalisation, Plotly interactive charts, and a multi-panel business dashboard.

Key questions answered:
- Which quick commerce platform generates the highest total revenue?
- Which platform has the best Average Order Value (AOV)?
- How do customer ratings compare across platforms?
- Does faster delivery actually improve delivery partner ratings?
- What is the most popular product category for a specific demographic (Swiggy Instamart, Mumbai, age 30–40)?
- Which cities should platforms expand into based on ratings, delivery speed, and order volume?
- Are discounts helping or hurting revenue?
- Which platform has the best operational efficiency (orders vs delivery time)?

---

## Dataset

| Property | Detail |
|---|---|
| Source | Quick Commerce Dataset (Kaggle / Udemy) |
| Columns | Order_ID, Company, City, Customer_Age, Customer_Rating, Delivery_Time_Min, Delivery_Partner_Rating, Order_Value, Items_Count, Product_Category, Discount_Applied, Distance_Km |
| Platforms covered | Swiggy Instamart, Blinkit, Zepto, BigBasket Now |
| Cities covered | Mumbai, Delhi, Bengaluru, Hyderabad, Pune, and more |

---

## Tools & Libraries

![Python](https://img.shields.io/badge/Python-3.10-blue)
![Pandas](https://img.shields.io/badge/Pandas-2.0-green)
![NumPy](https://img.shields.io/badge/NumPy-1.24-yellow)
![Matplotlib](https://img.shields.io/badge/Matplotlib-3.7-orange)
![Seaborn](https://img.shields.io/badge/Seaborn-0.12-teal)
![Plotly](https://img.shields.io/badge/Plotly-5.x-purple)
![Scikit--learn](https://img.shields.io/badge/Scikit--learn-1.3-red)

---

## Key Findings

- **Revenue leader wins on order volume, not basket size** — AOV differences are smaller than total revenue gaps across platforms
- **Customer ratings are industry-wide consistent** — no platform significantly outperforms others, indicating a sector-wide experience ceiling
- **Delivery time has near-zero correlation with partner ratings** — speed alone doesn't make partners happier
- **Discounts increase item volume but reduce average order value** — classic margin vs volume trade-off confirmed by data
- **Best expansion cities** meet all three criteria: Avg Rating ≥ 3.5, Avg Delivery Time ≤ 15 min, above-median order volume
- **Swiggy Instamart users in Mumbai aged 30–40** prefer Personal Care as their top product category

---

## Advanced Techniques Used

- **Group-wise mean imputation** using `transform(lambda x: x.fillna(x.mean()))`
- **Outlier removal** via percentile capping (`clip`) and row filtering
- **MinMaxScaler** from Scikit-learn for fair cross-platform efficiency comparison
- **Delivery Time Buckets** using `pd.cut()` for categorical binning
- **Plotly bubble scatter chart** for interactive operational efficiency visualisation
- **Multi-panel Matplotlib KPI Dashboard** with subplot2grid layout

---

## Project Structure

```
quick-commerce-analysis/
│
├── Quick_Commerce_analysis.ipynb        # Main analysis notebook
├── quick_commerce_data_raw.csv          # Raw dataset
├── requirements.txt                     # Python dependencies
└── README.md                            # This file
```

---

## How to Run

1. Clone this repository
   ```bash
   git clone https://github.com/YOUR_USERNAME/quick-commerce-analysis.git
   cd quick-commerce-analysis
   ```
2. Install dependencies
   ```bash
   pip install -r requirements.txt
   ```
3. Launch Jupyter
   ```bash
   jupyter notebook Quick_Commerce_analysis.ipynb
   ```

> **Note:** Remove the `new_path` and `data.to_csv(new_path)` cells or update the path to `./quick_commerce_data_cleaned.csv` before running locally.

---

## Author

**Manas Dhotre**
Aspiring Data Scientist | Python · Pandas · Plotly · Scikit-learn
📍 Pune, India

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-blue)](https://linkedin.com/in/YOUR_LINKEDIN)
[![GitHub](https://img.shields.io/badge/GitHub-Follow-black)](https://github.com/YOUR_USERNAME)

---

## Acknowledgements

Dataset sourced from Udemy — Big Data Analysis with Python course (Project 15)
