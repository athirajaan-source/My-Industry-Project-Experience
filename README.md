JPMorgan Quantitative Research – End-to-End Modeling Project

A comprehensive industry-style project integrating commodities forecasting, derivatives pricing, and credit risk modeling.

Badges
![Python](https://img.shields.io/badge/Python-3.10+-blue.svg)
![Jupyter](https://img.shields.io/badge/Platform-Jupyter%20Notebook-orange.svg)
![Models](https://img.shields.io/badge/Models-SARIMAX%20%7C%20XGBoost%20%7C%20LogReg-blue)
![License](https://img.shields.io/badge/License-MIT-green.svg)
![Status](https://img.shields.io/badge/Project-Completed-brightgreen.svg)


(Paste the above block exactly into your README — GitHub will convert them into badges.)

Project Overview

This repository contains four quantitative research tasks modeled after real workflows used in commodities markets, risk analytics, and credit modeling.
All work is performed in Jupyter Notebooks for transparency and reproducibility.

Tasks Summary
Task 1 – Natural Gas Forecasting & Price Estimation

Implements statistical and machine learning forecasting models including:

SARIMAX with seasonal structure

XGBoost regression for non-linear patterns

Fourier seasonal terms to capture long periodic cycles

Estimation of natural gas price for any arbitrary date

Visualization of trends & seasonality

Example visual:
(Add your plot here)

[Insert Natural Gas Forecast Plot]

Task 2 – Natural Gas Storage Contract Pricing

Simulates operational and financial components of a real gas storage contract:

Injection & withdrawal scheduling

Maximum storage capacity modeling

Rent, injection, withdrawal, and transport cost modeling

Contract value calculation using gas price forecasts

Equation Example:

Contract Value = (Sell Price – Buy Price) × Volume – Total Costs


Example visual:

[Insert Storage Valuation Flow Diagram]

Task 3 – Personal Loan Probability of Default (PD) Model

Builds a borrower-level PD model using XGBoost with engineered credit features:

Debt-to-Income ratio (DTI)

Credit utilization

Employment stability

Exposure at Default (EAD)

Previous default flag

Outputs:

Probability of Default (PD)

Expected Loss (EL)

EL = PD × EAD × LGD


Example visual:

[Insert Feature Importance Plot]

Task 4 – Mortgage PD using FICO Score Bucketization

Creates interpretable credit risk buckets using quantization:

Split FICO scores into ordered buckets

Train logistic regression for PD

Produce monotonic, interpretable PD values

Example visual:

[Insert FICO bucket PD chart]

Project Structure
My-Industry-Project-Experience/
│
├── data/
│   ├── Nat_Gas.csv                          # Natural gas monthly prices
│   ├── Task 3 and 4_Loan_Data.csv           # Personal loan dataset for PD
│   ├── Portfolio_Expected_Loss_Output.csv   # Expected Loss results
│   └── mortgage_with_PD.csv                 # Mortgage dataset with PD outputs
│
├── notebooks/
│   ├── 01_NaturalGas_Forecasting_PriceEstimation.ipynb
│   ├── 02_GasStorage_PricingModel.ipynb
│   ├── 03_PersonalLoan_PD_XGBoost.ipynb
│   └── 04_MortgagePD_FICO_Bucketization.ipynb
│
└── README.md

Quickstart Instructions
1. Clone the Repository
git clone https://github.com/athirajaan-source/My-Industry-Project-Experience.git
cd My-Industry-Project-Experience

2. Install Dependencies
pip install -r requirements.txt


If you don’t have a requirements file, install manually:

pip install pandas numpy scikit-learn statsmodels xgboost matplotlib seaborn

3. Launch Jupyter Notebook
jupyter notebook


Open the desired notebook from the notebooks/ folder.

Results Summary
Task 1 – Gas Forecasting

Seasonal patterns identified

SARIMAX + Fourier provided stable predictions

Multi-horizon forecasts generated

Task 2 – Contract Valuation

Engine produced realistic contract valuations

Demonstrated sensitivity to price scenarios

Task 3 – PD Model

XGBoost model with strong ROC-AUC

Generated PD and EL for entire portfolio

Task 4 – Mortgage PD

Clean, interpretable bucketization

Logistic regression PD aligned with credit risk expectations

Skills Demonstrated

Time Series Modeling: SARIMAX, seasonality extraction

Machine Learning: XGBoost, logistic regression

Risk Modeling: PD, EAD, LGD, EL

Financial Modeling: Storage contract pricing

Feature Engineering: Credit features, quantization

Data Visualization: Matplotlib, Seaborn

Python: pandas, NumPy, scikit-learn

License

This project is released under the MIT License.

Author

Athilakshmi Alagarsamy
Quantitative Research | Machine Learning | Financial Modeling

