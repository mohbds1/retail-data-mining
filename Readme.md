# 🛒 Retail Data Mining Project

**Author:** Legend (Mohammed)  
**Course:** Data Mining – Practical Exam  
**Language:** Python 3.10+  
**Dataset:** Retail Transactions (5,000 rows × 24 columns)

---

## 📘 Overview
This project delivers a complete **end-to-end data mining and analytics workflow** for retail sales data.  
It adheres strictly to the evaluation criteria outlined in the practical exam document (`اختبار عملي.pdf`), covering the full data science lifecycle:

1. **Know Your Data & Data Cleaning** — Data structure analysis, missing value imputation, financial data conversion, and outlier treatment (IQR/Winsorization).  
2. **Exploratory Data Analysis (EDA)** — Distribution analyses for *Sales, Profit,* and *Discounts*, along with comparative insights by *City, Customer Type,* and *Product Category*.  
3. **Data Mining Tasks**
   - 🧠 **Classification:** Predict *Customer Type* using Random Forest, enhanced with **SMOTE** for class balance and **Stratified K-Fold CV** for validation.  
   - 📈 **Regression:** Predict *Profit Margin* via Linear Regression with **K-Fold CV**, **residual diagnostics**, and **permutation-based feature importance**.  
   - 🎯 **Clustering:** Perform customer segmentation using KMeans, validated with **Silhouette** and **Davies–Bouldin scores**, followed by detailed **cluster profiling**.  
   - 🔗 **Association Rules:** Discover frequent product combinations using the Apriori algorithm and evaluate the **impact of discounts on co-purchases**.  
   - ⏳ **Time Series:** Build a **SARIMAX** model for sales forecasting, including 6-month backtesting and a **12-month forward forecast** with confidence intervals.  
4. **Reporting & Insights** — Summarized model outputs, validation metrics, and **business-driven recommendations**.

---

## ⚙️ Environment & Reproducibility
All experiments are deterministic with `random_state=42` for full reproducibility.

| Library | Version (tested) |
|----------|------------------|
| Python | 3.10+ |
| pandas | 2.2.x |
| numpy | 1.26.x |
| scikit-learn | 1.5.x |
| statsmodels | 0.14.x |
| seaborn | 0.13.x |
| matplotlib | 3.9.x |
| mlxtend | 0.23.x |
| imbalanced-learn | 0.12.x |

---

## 📂 Files Included
| File | Description |
|------|-------------|
| `retail_exam.ipynb` | Jupyter Notebook with full analysis, code, and outputs |
| `retail_exam_report.html` | **Final exported HTML report** (ideal for viewing and grading) |
| `data.csv` | Source dataset |
| `forecast_next_12m.csv` | **SARIMAX 12-month sales forecast results** |
| `perm_importance_top10.csv` | Top 10 features ranked by permutation importance |
| `اختبار عملي.pdf` | **Official Exam Rubric / Task Instructions** |

---

## 🧩 How to Run

1. **Install dependencies:**
   ```bash
   pip install -r requirements.txt

*(or manually install: pandas, numpy, scikit-learn, statsmodels, seaborn, matplotlib, mlxtend, imbalanced-learn)*

2. **Launch notebook:**

   ```bash
   jupyter notebook retail_exam.ipynb
   ```

3. **Execute all cells:**
   Go to `Kernel → Restart & Run All`.
   All visualizations, metrics, and result files will regenerate automatically.

---

## 🧾 Key Results

| Task                  | Highlight                                                                                                       |
| --------------------- | --------------------------------------------------------------------------------------------------------------- |
| **Classification**    | Achieved **Cross-Validated F1-macro = 0.362**, with SMOTE balancing and Random Forest tuned via GridSearchCV.   |
| **Regression**        | Attained **R² ≈ 0.945**, identifying *Retail Price* and *Order Number* as dominant predictors of profit margin. |
| **Clustering**        | Produced **3 stable customer segments** (Silhouette = 0.678, DB = 0.864) with distinct behavioral profiles.     |
| **Association Rules** | High-lift bundles detected (e.g., A+B lift ≈ 3.2), especially under low-discount regimes.                       |
| **Time Series**       | SARIMAX forecast revealed **strong Q4 seasonality**, guiding inventory pre-stocking strategy.                   |

---

## 🧠 Business Insights

* **Bundle Optimization:** Launch A+B and C+D combos to exploit strong cross-sell lift.
* **Discount Control:** Maintain discounts within 15–20% to sustain profit margins.
* **Customer Segments:** Prioritize premium packaging for Cluster 0 and loyalty rewards for Cluster 1.
* **Inventory Planning:** Increase Q4 stock by 15% based on seasonal peaks.
* **Reproducibility:** Configured environment ensures consistent reruns and grading alignment.

---

## 🏁 Notes

This notebook demonstrates mastery of the data science process — from raw data cleaning and feature engineering to advanced modeling, validation, and strategic interpretation.
All findings are **traceable, reproducible, and actionable** for real-world retail analytics applications.

---

© 2025 Legend | Data Science
