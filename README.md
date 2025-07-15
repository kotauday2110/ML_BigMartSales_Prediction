
# 🛒 Big Mart Sales Analysis

A complete data‑analysis and predictive‑modeling project on Big Mart retail data using **Python, pandas, and scikit‑learn**. The goal is to forecast *Item Outlet Sales* and uncover the main drivers of revenue.

---

## 📌 Problem Statement

Big Mart wants to **understand and predict product‑level sales** across its outlets to improve inventory planning, pricing, and promotions.

---

## 📂 Dataset Overview

* **Records:** 8,523 rows
* **Target:** `Item_Outlet_Sales`
* **Features:** Product details (type, fat content, MRP, visibility) and outlet info (type, size, location)

---

## 🧹 Data Preprocessing

* Imputed missing `Item_Weight` (mean) and `Outlet_Size` (mode by `Outlet_Type`)
* Standardized inconsistent labels in `Item_Fat_Content`
* Label‑encoded 7 categorical columns
* Split data into **train 80 % / test 20 %**

---

## ⚙️ Model Building & Tuning

| Model         | Best Params          | R²        | RMSE      |
| ------------- | -------------------- | --------- | --------- |
| Lasso         | `alpha=0.1`          | 0.489     | 1 255     |
| Decision Tree | `max_depth=5`        | **0.580** | **1 138** |
| Random Forest | `n_estimators=200`   | 0.552     | 1 175     |
| XGBoost       | `learning_rate=0.05` | 0.571     | 1 152     |

**Decision Tree** chosen as final model (best R² / lowest RMSE). Hyper‑parameters tuned with **GridSearchCV**.

---

## 📈 Output

* Predictions exported to **`final_predictions_decision_tree.csv`** for downstream visualization or BI tools.

---

## 💡 Key Insights

* Item MRP and outlet characteristics strongly influence sales.
* Proper data cleaning and basic tree‑based algorithms can outperform more complex models when tuned correctly.

---

## 📁 Repository Structure

```text
.
├── data/
│   └── bigmart_train.csv
├── notebooks/
│   └── BigMart_Sales_Prediction.ipynb
├── final_predictions_decision_tree.csv
└── README.md
```

---

## 🚀 How to Reproduce

1. Clone the repo
2. Install requirements

   ```bash
   pip install -r requirements.txt
   ```
3. Run the Jupyter notebook in `notebooks/`

---

## 🙋‍♂️ Author

**Udaykanth Kota** – [udaykota41@gmail.com](mailto:udaykota41@gmail.com)
B.Tech Civil Engineering, NIT Warangal – Data Analytics & Trading Enthusiast

---
