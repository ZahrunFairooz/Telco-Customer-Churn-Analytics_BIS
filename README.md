# Telco-Customer-Churn-Analytics_BIS
Data Analytics Project on Customer Churn in Telecommunications

# Customer Churn Analysis – Telco Dataset

**Student ID:** 21021074  
**Name:** M.F.F. Zahrun  

---

##  Project Overview

Customer churn is a major challenge in the telecommunications industry. Losing existing customers directly impacts revenue and increases customer acquisition costs. This project analyzes customer churn behavior using the Telco Customer Churn dataset and develops a predictive model to identify customers at high risk of leaving.

The goal of this analysis is to:

- Identify key drivers of customer churn
- Perform exploratory data analysis (EDA)
- Build and evaluate a predictive model
- Provide actionable business insights

---

##  Business Domain

**Domain:** Telecommunications / Customer Behavior Analytics  

Churn prediction is critical for improving customer retention strategies and increasing customer lifetime value.

---

##  Dataset Information

- **Dataset Name:** Telco Customer Churn
- **Source:** Kaggle  
  https://www.kaggle.com/datasets/blastchar/telco-customer-churn
- **Total Records:** 7,043 customers
- **Total Features:** 21 variables

### Target Variable
- `Churn` (Yes / No)

### Feature Categories
- Demographics (Gender, SeniorCitizen, Partner, Dependents)
- Service Information (InternetService, OnlineSecurity, StreamingTV, etc.)
- Contract & Billing (Contract, PaymentMethod)
- Financial Information (MonthlyCharges, TotalCharges, tenure)

---

##  Data Analytics Process

### 1️ Data Collection
- Dataset downloaded from Kaggle
- Loaded into Python using Pandas

### 2️ Data Preprocessing
- Removed `customerID` (non-predictive identifier)
- Converted `TotalCharges` to numeric format
- Handled missing values using `pd.to_numeric(errors='coerce')`
- Applied one-hot encoding to categorical variables
- Standardized numerical features using `StandardScaler`
- Split data into training and testing sets (80/20)

### 3️ Exploratory Data Analysis (EDA)

The following analyses were performed:

- Missing values heatmap
- Churn distribution analysis
- Tenure distribution
- Monthly charges distribution
- Total charges distribution
- Correlation matrix
- Contract type vs churn analysis

Key observations:
- 26.6% of customers churned
- Customers with month-to-month contracts show highest churn
- Higher monthly charges are associated with higher churn
- Customers with low tenure are more likely to churn
- Strong correlation (0.83) between tenure and TotalCharges

---

##  Model Development

A **Logistic Regression** model was built for churn prediction.

### Why Logistic Regression?
- Suitable for binary classification
- Interpretable coefficients
- Efficient and reliable baseline model

---

##  Model Performance

| Metric | Value |
|--------|--------|
| Accuracy | 78.7% |
| Precision (Churn) | 0.62 |
| Recall (Churn) | 0.52 |
| F1-Score | 0.56 |
| ROC-AUC | 0.83 |

### Interpretation

- The model performs well overall (AUC = 0.83)
- Better at predicting non-churn customers
- Moderate performance in detecting churned customers
- Some high-risk customers remain undetected due to class imbalance

---

##  Key Drivers of Churn

Based on logistic regression coefficients:

### Strong Positive Predictors:
- Fiber optic internet service
- Higher TotalCharges
- StreamingTV & StreamingMovies
- Electronic check payments
- Month-to-month contracts

### Strong Negative Predictors (Retention):
- Longer tenure
- One-year and two-year contracts
- Automatic payment methods

---

##  Business Insights

The analysis indicates:

- New customers (0–10 months tenure) are most vulnerable
- Month-to-month contracts significantly increase churn risk
- Premium service users (Fiber optic + Streaming) show higher churn
- Automatic payment methods improve retention

### Recommended Business Actions:

- Improve onboarding for new customers
- Offer incentives for long-term contracts
- Review pricing strategy for premium services
- Encourage automatic payment enrollment
- Develop targeted retention campaigns for high-risk segments

---

##  Tools & Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn

---

##  Repository Structure

Telco-Customer-Churn-Analytics_BIS/
│
├── README.md
├── Zahrun_Notebook.ipynb
└── 21021074_BIS.pdf


---

## Conclusion

This project successfully identified key churn drivers and developed a predictive model with strong discriminative performance (AUC = 0.83). While overall accuracy is high, improving recall for churn prediction would further enhance business impact.

By targeting high-risk customers such as new users and month-to-month contract holders, telecom companies can reduce churn and improve long-term profitability.

---

