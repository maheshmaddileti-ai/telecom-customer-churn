# Telecom Customer Churn Prediction

End-to-end machine learning project to predict which telecom customers are likely to churn, enabling proactive retention strategies.

---

## Problem Statement

A telecom company named "Neo" is losing customers to competitors. This project analyzes customer data to identify patterns in churning behavior and builds predictive models to flag high-risk customers before they leave.

---

## Dataset

**File:** `customer_churn.csv`  
**Rows:** 7,043  
**Domain:** Telecom

Key columns include: `customerID`, `gender`, `SeniorCitizen`, `tenure`, `PhoneService`, `InternetService`, `Contract`, `MonthlyCharges`, `TotalCharges`, `Churn`

---

## Project Objectives

1. Identify patterns and insights in customer churn behavior
2. Build and compare multiple ML models to predict churn
3. Determine the best model for production use

---

## Key Findings

- **Contract Type:** Customers on month-to-month contracts churn significantly more than those on 1 or 2-year contracts — two-year contract customers have the highest tenure
- **Monthly Charges:** Higher monthly charges are associated with increased churn probability
- **Fiber Optic Users:** Majority of internet service customers use Fiber Optic — this segment shows higher churn rates
- **Tenure Pattern:** Most customers who leave do so within the first 10–65 months of service
- **Senior Citizens with Electronic Check payments** represent a high-risk churn segment

---

## Data Manipulation Performed

- Extracted specific customer segments by filtering on multiple conditions
- Handled missing values and data type conversions
- Label encoded all categorical variables
- Applied VIF (Variance Inflation Factor) analysis to remove multicollinear features

---

## Models Built

| Model | Split | Metric |
|---|---|---|
| Linear Regression | 70:30 | RMSE |
| Logistic Regression (Simple) | 65:35 | Accuracy + Confusion Matrix |
| Logistic Regression (Multiple) | 80:20 | Accuracy + Confusion Matrix |
| Decision Tree Classifier | 80:20 | Accuracy + Confusion Matrix |
| Random Forest Classifier | 70:30 | Accuracy + Confusion Matrix |

**Best Model:** Multiple Logistic Regression — provided the highest accuracy with `tenure` and `MonthlyCharges` as features.

---

## Business Recommendation

Focus retention campaigns on:
- Month-to-month contract customers in their first 12 months
- Customers with monthly charges above $65
- Senior citizens using electronic check payments

Offering better pricing on 2-year contracts could significantly reduce churn rate.

---

## Tech Stack

- **Language:** Python 3
- **Libraries:** Pandas, NumPy, Matplotlib, Seaborn, Scikit-learn

---

## Project Structure

```
telecom-customer-churn/
│
├── customer_churn.py         # Full analysis, visualization, and modeling code
├── customer_churn.csv        # Dataset
└── README.md                 # Project documentation
```

---

## How to Run

1. Clone the repository
```bash
git clone https://github.com/maheshmaddileti-ai/telecom-customer-churn
```

2. Install dependencies
```bash
pip install pandas numpy matplotlib seaborn scikit-learn
```

3. Run the script
```bash
python customer_churn.py
```

---

## Author

**Mahesh Maddileti**  
PGP in Data Science & Machine Learning — IntelliPaat (April 2026)  
[LinkedIn](https://linkedin.com/in/maheshmaddileti) | [GitHub](https://github.com/maheshmaddileti-ai)

---

## Certificate

This project was completed as part of the IntelliPaat Post Graduate Program in Data Science & Machine Learning.  
Certificate ID: 31679-462158-209407
