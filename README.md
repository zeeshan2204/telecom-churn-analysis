# 📉 Telecom Customer Churn Analysis

![Python](https://img.shields.io/badge/Python-3.11-blue?style=flat&logo=python)
![Power BI](https://img.shields.io/badge/PowerBI-Dashboard-yellow?style=flat&logo=powerbi)
![XGBoost](https://img.shields.io/badge/Model-XGBoost-orange?style=flat)
![Accuracy](https://img.shields.io/badge/Accuracy-95%25-brightgreen?style=flat)
![SQL](https://img.shields.io/badge/Database-SQLite-lightgrey?style=flat&logo=sqlite)

> Identifying why telecom customers leave — and what the company can do about it.

---

## 📌 Problem Statement

Customer churn is one of the biggest revenue threats in the telecom industry. This project analyzes **3,333 customer records** to uncover the key drivers of churn and build a predictive model — helping retention teams act before customers leave.

---

## 🗂️ Project Structure

```
telecom_churn_project/
│
├── data/
│   ├── churn-bigml-80.csv        ← Training data
│   └── churn-bigml-20.csv        ← Test data
│
├── notebooks/
│   └── analysis.ipynb            ← Full analysis + model
│
├── database/
│   └── churn.db                  ← SQLite database
│
└── dashboard/
    ├── churn_analysis.png        ← EDA plots
    ├── feature_importance.png    ← Top churn factors
    ├── full_data_powerbi.csv     ← Power BI data
    └── telecom_churn_project.pdf ← Dashboard export
```

---

## 🛠️ Tools & Technologies

| Category | Tools |
|---|---|
| Language | Python 3.11 |
| Data Analysis | Pandas, NumPy |
| Machine Learning | Scikit-learn, XGBoost |
| Database | SQLite |
| Visualization | Matplotlib, Seaborn |
| Dashboard | Power BI Desktop |

---

## 📊 Key Findings

### 🔴 Finding 1 — International Plan is a Major Red Flag
Customers with an international plan churn at **42.4%** vs just **11.5%** for those without — nearly **4x higher risk**. These customers are likely dissatisfied with call rates or plan value.

### 🔴 Finding 2 — Customer Service Calls = Early Warning Signal
Churn rate jumps dramatically after **4+ customer service calls**:

| Calls | Churn Rate |
|---|---|
| 0–3 calls | ~10–13% |
| 4 calls | 45.8% |
| 5 calls | 60.6% |
| 6+ calls | 63–100% |

> Customers who call support repeatedly are clearly frustrated — and likely to leave.

### 🔴 Finding 3 — High-Risk States
**NJ, TX, MD** have the highest churn rates (24–26%), suggesting regional pricing or network quality issues.

---

## 🤖 Machine Learning Model

| Metric | Score |
|---|---|
| Algorithm | XGBoost Classifier |
| Accuracy | **95%** |
| Precision (Churn) | 96% |
| F1-Score (Churn) | 0.81 |
| Train/Test Split | 80/20 |

### Top Churn Factors (Feature Importance)
1. `customer_service_calls` — #1 predictor
2. `international_plan` — 4x churn multiplier
3. `total_day_minutes` — heavy users churn more
4. `total_intl_calls` — dissatisfied international users
5. `voice_mail_plan` — plan mismatch indicator

---

## 📈 Power BI Dashboard

The interactive dashboard covers:
- **Overall churn rate** — 14.49% across 3,333 customers
- **State-wise churn map** — geographic breakdown
- **International plan impact** — pie chart comparison
- **Service calls danger zone** — line chart showing churn spike
- **Risk segmentation** — Low / Medium / High risk customer split

> 📎 [View Dashboard PDF](./dashboard/telecom_churn_project.pdf)

---

## 💡 Business Recommendations

1. **Flag customers at 3+ service calls** — proactively reach out before they churn
2. **Audit the international plan** — revise pricing or add value; 42% churn is unsustainable
3. **Target NJ, TX, MD** with retention offers — highest churn states need priority attention
4. **Monitor heavy daytime users** — offer loyalty plans to high-usage customers

---

## 🚀 How to Run

```bash
# Clone the repo
git clone https://github.com/zeeshan2204/telecom-churn-analysis.git
cd telecom-churn-analysis

# Install dependencies
pip install pandas numpy scikit-learn xgboost matplotlib seaborn openpyxl

# Open notebook
jupyter notebook notebooks/analysis.ipynb
```

---

## 📁 Dataset

- **Source:** [Telecom Churn Dataset — Kaggle](https://www.kaggle.com/datasets/mnassrib/telecom-churn-datasets)
- **Records:** 3,333 customers
- **Features:** 20 columns (usage stats, plan info, service calls, churn label)

---

## 👤 Author

**Zeeshan**
B.Tech CSE (Data Science) — Techno Main Salt Lake, Kolkata
[LinkedIn](https://linkedin.com/in/zeeshan2204) • [GitHub](https://github.com/zeeshan2204)
