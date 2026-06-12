# 📊 Customer Churn Prediction & Analysis

![Python](https://img.shields.io/badge/Python-3.x-blue?logo=python)
![Power BI](https://img.shields.io/badge/PowerBI-Dashboard-yellow?logo=powerbi)
![MySQL](https://img.shields.io/badge/MySQL-Database-orange?logo=mysql)
![ML](https://img.shields.io/badge/ML-Logistic%20Regression-green)

## 📌 Problem Statement
Customer churn is one of the biggest challenges for telecom companies. This project analyzes a telecom dataset of **7,043 customers** to understand *why* customers leave and build a machine learning model to *predict* who is likely to churn — so the business can act before it's too late.

---

## 📁 Project Structure
```
customer-churn-prediction/
│
├── Project.ipynb                    # Main analysis & ML notebook
├── customer_churn_analysis.sql      # MySQL database setup + analysis queries
├── Customer_Churn_Dashboard.pbix    # Power BI dashboard
├── Project.csv                      # Dataset (7043 rows, 21 columns)
└── README.md
```

---

## 📂 Dataset
- **Source:** Telco Customer Churn Dataset
- **Rows:** 7,043 customers
- **Columns:** 21 features including demographics, services, billing, and churn label

| Column | Description |
|--------|-------------|
| `customerID` | Unique customer identifier |
| `gender`, `SeniorCitizen`, `Partner`, `Dependents` | Demographics |
| `tenure` | Months with the company |
| `PhoneService`, `InternetService`, `OnlineSecurity` ... | Services subscribed |
| `Contract` | Month-to-month / One year / Two year |
| `PaymentMethod` | How the customer pays |
| `MonthlyCharges`, `TotalCharges` | Billing info |
| `Churn` | **Target variable** — Yes / No |

---

## 🔍 Key Findings

- **Overall churn rate: 26.5%** — roughly 1 in 4 customers leaves
- Customers on **Month-to-Month contracts** churn at **42%** vs only **3%** for Two-Year contracts
- **Fiber optic** internet users churn more — likely due to higher pricing
- Customers in their **first 12 months** are the highest risk group (churn rate ~48%)
- **Electronic check** payment users churn at nearly 2x the rate of auto-pay users
- Churned customers pay on average **$13 more per month** than retained customers

---

## 🛠️ Tools & Technologies

| Tool | Purpose |
|------|---------|
| Python (pandas, numpy) | Data cleaning & preprocessing |
| Scikit-learn | Machine learning (Logistic Regression) |
| Matplotlib / Seaborn | Data visualization |
| MySQL Workbench | SQL analysis queries |
| Power BI | Interactive dashboard |

---

## 🤖 Machine Learning Model

**Algorithm:** Logistic Regression  
**Train/Test Split:** 80% / 20%  
**Features used:** All 20 columns (after encoding + scaling)

**Data preprocessing steps:**
1. Converted `TotalCharges` from string to numeric — 11 blank rows (new customers, `tenure=0`) filled with `0`
2. Dropped `customerID` (not a predictive feature)
3. Label-encoded all categorical columns
4. Standardized all features using `StandardScaler`

---

## 📊 Power BI Dashboard
The dashboard includes:
- KPI cards: Total Customers, Churned Customers, Churn Rate %, Avg Monthly Charges
- Churn by Contract Type
- Churn by Internet Service
- Churn by Payment Method
- Churn Rate by Tenure Group
- Slicers for gender, SeniorCitizen, Contract type

---

## 🗄️ SQL Analysis
The `customer_churn_analysis.sql` file contains:
- Full `CREATE TABLE` schema
- All 7,043 rows inserted
- 8 analysis queries covering churn rate, revenue impact, tenure groups, and more

**To run in MySQL Workbench:** File → Open SQL Script → Run All

---

## 🚀 How to Run the Notebook
```bash
# 1. Clone the repo
git clone https://github.com/Manish-9770/customer-churn-prediction.git
cd customer-churn-prediction

# 2. Install dependencies
pip install pandas numpy matplotlib seaborn scikit-learn

# 3. Open the notebook
jupyter notebook Project.ipynb
```

---

## 👤 Author
**[Manish]**  
[LinkedIn](www.linkedin.com/in/manish-kumar-b6b1623b1) | [GitHub](https://github.com/Manish-9770)

