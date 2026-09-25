# 🍽️ Zomato Bangalore Restaurant Data Analysis

A beginner-level data analytics project exploring restaurant trends, pricing, and ratings across Bangalore using a real Zomato dataset.

## 📌 Problem Statement
Bangalore has thousands of restaurants listed on Zomato. This project analyzes that data to answer practical questions: Which cuisines and restaurant types dominate the market? Does online ordering or table booking actually correlate with better ratings? Which localities offer the best food, and which offer the best *value*?

## 📊 Dataset
- **Source:** Kaggle — Zomato Restaurants Dataset (Bangalore)
- **Size:** 7,105 restaurants, 12 raw columns
- **Fields:** restaurant name, type, rating, number of ratings, average cost for two, online ordering availability, table booking availability, cuisines, area, and locality

## 🛠️ Tools Used
- **Python** — pandas (data cleaning & analysis), matplotlib & seaborn (visualization)
- **Jupyter Notebook** — for the full analysis walkthrough

## 🧹 Data Cleaning Steps
- Removed junk export columns and standardized column names
- Treated `rating == 0` and `cost == 0` as missing values (not real ratings/costs)
- Converted Yes/No fields to proper booleans
- Extracted a `primary_cuisine` and `primary_type` from multi-value fields
- Bucketed cost into Budget / Mid-range / Premium / Fine Dine brackets

## 🔍 Key Insights
1. **North Indian dominates** as the most common cuisine (~1,940 restaurants), followed by South Indian and Chinese.
2. **Quick Bites & Casual Dining** make up ~65% of all restaurants — Bangalore's scene is casual-first, not fine-dining-first.
3. **Online ordering barely moves the needle on ratings** (+2.3% average rating) — food quality matters more than delivery availability.
4. **Table booking is the strongest upscale signal**: restaurants offering it average **4.04★** vs **3.45★**, and cost ~3x more (₹1,355 vs ₹444 for two).
5. **Cost and rating are only moderately correlated** (r ≈ 0.38) — plenty of budget spots are still highly rated.
6. **Lavelle Road, Church Street, and Koramangala 5th Block** have the highest average ratings in the city.
7. **Basavanagudi stands out for value-for-money** — strong ratings at a comparatively low average cost.
8. Only **10.5%** of restaurants offer table booking vs **52.5%** offering online ordering — the market is optimized for delivery, not dine-in reservations.

## 📁 Project Structure
```
├── Zomato_Restaurant_Analysis.ipynb   # Full analysis notebook (cleaning + EDA + charts + insights)
├── zomato_cleaned.csv                 # Cleaned dataset
├── charts/                            # Exported chart images
│   ├── 01_top_cuisines.png
│   ├── 02_top_localities.png
│   ├── 03_cost_vs_rating.png
│   ├── 04_online_order_vs_rating.png
│   ├── 05_restaurant_types.png
│   ├── 06_correlation_heatmap.png
│   └── 07_table_booking_comparison.png
└── README.md
```

## ▶️ How to Run
1. Open `Zomato_Restaurant_Analysis.ipynb` in Jupyter Notebook or upload it to Google Colab.
2. Make sure the raw CSV is in the same folder (or update the `RAW_PATH` variable at the top).
3. Run all cells top to bottom.

## 🚀 Possible Extensions
- Predict restaurant rating from its attributes (ML classification/regression)
- Scrape live Swiggy data and compare pricing/rating trends against this Zomato snapshot
- Build an interactive Power BI / Tableau dashboard on top of `zomato_cleaned.csv`

---
*Project by Nikhil — B.Tech CSE (IT), 2026*
