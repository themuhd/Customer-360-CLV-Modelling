# Customer-360-CLV-Modelling
Built a Customer 360 data model and predicted CLV using ML (XGBoost, Random Forest, SVR) and probabilistic models (BG/NBD, Gamma-Gamma). Includes EDA, feature engineering (RFM), and model evaluation on multi-touchpoint customer data.


📦
🧠 Overview

This project develops a Customer 360° data model to analyse customer behaviour across multiple touchpoints and predict Customer Lifetime Value (CLV) using both:

Machine Learning models (XGBoost, Random Forest, etc.)
Probabilistic models (BG/NBD + Gamma-Gamma via Lifetimes)

The work is based on a real-world dataset from Collinson Group (Valuedynamx) and follows the CRISP-DM methodology .

🎯 Objectives
Build a unified Customer 360 dataset
Perform Exploratory Data Analysis (EDA) across multiple systems
Engineer RFM (Recency, Frequency, Monetary) features
Predict CLV using ML + statistical models
Compare model performance and business applicability


📊 Data Sources

The dataset combines four major systems into a single Customer 360 view:

SmartPay – transactional & loyalty purchases
SmartEarn – affiliate clicks & rewards
SmartRedeemStore – redemption behaviour
SmartLink – card-linked offers & transactions

👉 These were integrated into a single customer-level dataset for modelling

🔍 Exploratory Data Analysis (EDA)

Notebook: EDA.ipynb

Key insights:

Strong right-skewed transaction distributions (few high-value customers)
Majority of customers show:
Low spend
Low frequency
Clear seasonal trends in spending
Outliers identified in:
Transaction amounts
Settlement values
⚙️ Feature Engineering

Core features based on RFM model:

Recency → time since last purchase
Frequency → number of transactions
Monetary → total spend

Additional features:

Average Order Value
Decay-adjusted monetary value (time value of money)
🤖 Modelling Approaches
1. Machine Learning Models

Notebook: CLV_with_ML.ipynb

Models used:

XGBoost ⭐ (Best performer)
Random Forest
Gradient Boosting
Support Vector Regression
Evaluation Metrics:
RMSE
MAE
R²
Key Result:
XGBoost achieved:
R² ≈ 0.93
Lowest prediction error
2. Lifetimes (Probabilistic Models)

Notebook: CLV_with_Lifetimes.ipynb

Models:

BG/NBD → predicts purchase frequency
Gamma-Gamma → predicts monetary value

Outputs:

Expected purchases
Customer lifetime value (12-month forecast)
Key Insight:
Strong correlation between predicted CLV and actual revenue (0.91)
📈 Results Summary
Model	Performance
XGBoost	Best overall (high accuracy, low error)
Gradient Boosting	Comparable to XGBoost
Random Forest	Moderate performance
SVR	Weakest

📌 Final Recommendation:

Use XGBoost for prediction accuracy
Use Lifetimes models for interpretability & marketing use cases
🧩 Customer 360 Architecture

The project builds a unified customer model combining:

Transactions
Click behaviour
Rewards & redemptions
Account & membership data

This enables:
Cross-channel behaviour analysis
Better segmentation
Accurate CLV estimation

⚠️ Limitations
High data complexity & integration effort
Computational constraints (large datasets)
GDPR restrictions limiting feature richness

🚀 Future Improvements
Customer segmentation (clustering)
Deep learning models (DNN)
Real-time CLV prediction
Incorporating unstructured data (reviews, sentiment)

🛠️ Tech Stack
Python (Pandas, NumPy, Scikit-learn)
XGBoost
Lifetimes library
Jupyter Notebook
Azure Databricks / Google Colab
