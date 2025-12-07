JPMorgan – Quantitative Research Project

This repository contains a multi-domain quantitative modeling suite inspired by the JPMorgan Quantitative Research workflow.
It includes time series forecasting for natural gas markets, valuation of gas storage contracts, and credit risk modeling for personal loans and mortgage portfolios.

Overview

This project demonstrates end-to-end development of quantitative tools covering:

Time series modeling and forecasting using SARIMAX, XGBoost, and Fourier features

Derivatives-style valuation of natural gas storage contracts

Probability of Default (PD) modeling for personal loans using XGBoost

Mortgage PD modeling using FICO score discretization and logistic regression

The project reflects industry-aligned methods used in pricing, risk analytics, and portfolio management.

Key Components
1. Natural Gas Forecasting

Built forecasting models using SARIMAX and XGBoost

Added Fourier seasonality features to capture long-term cyclical patterns

Generated multi-horizon forecasts (short- and long-term)

Produced trend and seasonality visualizations for analysis

2. Gas Storage Contract Valuation

Modeled injection and withdrawal schedules

Implemented operational constraints and storage capacity rules

Integrated price forecasts to compute contract value

Included cost elements such as storage fees, injection/withdrawal costs, and transport costs

3. Personal Loan PD Modeling

Engineered credit features including DTI, utilization, job stability, and outstanding exposure

Trained an XGBoost classifier to estimate borrower-level PD

Calculated Expected Loss (EL) using PD × EAD × LGD

Evaluated model using ROC-AUC and feature-importance analysis

4. Mortgage PD Modeling Using FICO Buckets

Discretized FICO scores into ordinal credit buckets using quantile-based binning

Mapped buckets to risk ratings for interpretability

Trained a logistic regression PD model

Generated PD estimates and EL calculations for all mortgage borrowers

Technology Stack

Languages and Libraries

Python

Pandas, NumPy

scikit-learn

statsmodels (SARIMAX)

XGBoost

Matplotlib, Seaborn

Methods Used

Time series forecasting

Logistic regression

Ensemble models

Feature engineering

Quantization/bucketing

Derivatives valuation logic

Credit risk modeling

Project Structure
project/
│
├── data/
│   ├── natural_gas_prices.csv
│   ├── personal_loans.csv
│   └── mortgage_data.csv
│
├── forecasting/
│   ├── sarimax_model.py
│   ├── xgboost_model.py
│   └── fourier_features.py
│
├── valuation/
│   └── gas_storage_valuation.py
│
├── credit_risk/
│   ├── loan_pd_xgboost.py
│   ├── fico_bucketization.py
│   └── mortgage_pd_logit.py
│
├── notebooks/
│   ├── 01_gas_forecasting.ipynb
│   ├── 02_storage_valuation.ipynb
│   ├── 03_loan_pd_model.ipynb
│   └── 04_mortgage_pd_model.ipynb
│
└── README.md

Installation

Clone the repository:

git clone https://github.com/yourusername/jpm-qresearch-project.git
cd jpm-qresearch-project
pip install -r requirements.txt

Usage

Run natural gas forecasting:

python forecasting/sarimax_model.py
python forecasting/xgboost_model.py


Run gas storage valuation:

python valuation/gas_storage_valuation.py


Train personal loan PD model:

python credit_risk/loan_pd_xgboost.py


Train mortgage PD model:

python credit_risk/mortgage_pd_logit.py

Future Enhancements

Add GARCH volatility modeling for natural gas price risk

Monte Carlo simulation for price paths

SHAP explanations for credit models

Extend mortgage PD model to lifetime ECL

License
