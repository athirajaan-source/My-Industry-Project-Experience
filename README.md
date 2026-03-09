

# 📈 Quantitative Research – End-to-End Modeling Project

[![Python](https://img.shields.io/badge/Python-3.8%2B-blue?logo=python&logoColor=white)](https://www.python.org/)
[![Jupyter](https://img.shields.io/badge/Notebook-Jupyter-F37626?logo=jupyter&logoColor=white)](https://jupyter.org/)
[![Machine Learning](https://img.shields.io/badge/Machine%20Learning-XGBoost%20%7C%20Scikit--Learn-yellow)](#)
[![Finance](https://img.shields.io/badge/Domain-Quantitative%20Finance-0052CC)](#)

> **A comprehensive industry-style project integrating commodities forecasting, derivatives pricing, and credit risk modeling.**

 📋 Project Overview

This repository contains four quantitative research tasks modeled after real-world workflows used in commodities markets, risk analytics, and credit modeling. All work is performed and documented in Jupyter Notebooks to ensure transparency, reproducibility, and clear communication of results.

---

 🎯 Tasks Summary

### 1️⃣ Task 1 – Natural Gas Forecasting & Price Estimation
Implements statistical and machine learning forecasting models to predict natural gas prices:
- **Models Used:** `SARIMAX` with seasonal structure, `XGBoost` regression for non-linear patterns.
- **Feature Engineering:** Implemented Fourier seasonal terms to capture long periodic cycles.
- **Outputs:** Estimation of natural gas price for any arbitrary future date, accompanied by visualizations of trends and seasonality.

![Model Output]
<img width="997" height="528" alt="NaturalGasPrice_Forecasting" src="https://github.com/user-attachments/assets/e55d0fa8-8f58-449b-a3fc-e3f229f73f9f" />
![Model Output]
<img width="420" height="165" alt="PDEstimation_Output" src="https://github.com/user-attachments/assets/2d6c60c9-ff23-478f-ad3e-0dedf775cb52" />
![Model Output]
<img width="506" height="414" alt="FICOBukets_EvaluationMetrics" src="https://github.com/user-attachments/assets/82e36eb0-1f2a-4c94-8600-144f7441b5c0" />

### 2️⃣ Task 2 – Natural Gas Storage Contract Pricing
Simulates operational and financial components of a real-world gas storage contract:
- **Modeling Components:** 
  - Injection & withdrawal scheduling.
  - Maximum storage capacity modeling.
  - Rent, injection, withdrawal, and transport cost modeling.
- **Valuation:** Contract value calculation utilizing the gas price forecasts from Task 1.
- **Core Logic Engine:**
  ```text
  Contract Value = ((Sell Price – Buy Price) × Volume) – Total Costs
  ```

### 3️⃣ Task 3 – Personal Loan Probability of Default (PD) Model
Builds a borrower-level Probability of Default (PD) model using engineered credit features:
- **Features Engineered:** Debt-to-Income ratio (DTI), Credit utilization, Employment stability, Exposure at Default (EAD), and Previous default flags.
- **Model:** `Logistic Regression` & `XGBoost`.
- **Outputs:** Portfolio Expected Loss (EL) calculations.
  ```text
  Expected Loss (EL) = Probability of Default (PD) × Exposure at Default (EAD) × Loss Given Default (LGD)
  ```

### 4️⃣ Task 4 – Mortgage PD using FICO Score Bucketization
Creates interpretable credit risk buckets using quantization techniques:
- **Methodology:** Split continuous FICO scores into ordered risk buckets.
- **Model:** Trained a logistic regression model on bucketed data to predict PD.
- **Result:** Produced monotonic, highly interpretable PD values aligned with regulatory and credit risk expectations.

---

## 📂 Project Structure

```text
My-Industry-Project-Experience/
│
├── data/
│   ├── Nat_Gas.csv                             # Natural gas monthly prices
│   ├── Task_3_and_4_Loan_Data.csv              # Personal loan dataset for PD
│   ├── Portfolio_Expected_Loss_Output.csv      # Generated Expected Loss results
│   └── mortgage_with_PD.csv                    # Generated Mortgage dataset with PD outputs
│
├── notebooks/
│   ├── 01_NaturalGas_Forecasting_PriceEstimation.ipynb
│   ├── 02_GasStorage_PricingModel.ipynb
│   ├── 03_PersonalLoan_PD_LogisticRegression.ipynb
│   └── 04_MortgagePD_FICO_Bucketization.ipynb
│
├── requirements.txt
└── README.md
```

---

## 🚀 Quickstart Instructions

**1. Clone the Repository**
```bash
git clone https://github.com/athirajaan-source/My-Industry-Project-Experience.git
cd My-Industry-Project-Experience
```

**2. Install Dependencies**

Install required packages using the `requirements.txt` file:
```bash
pip install -r requirements.txt
```
*(Alternatively, install manually:)*
```bash
pip install pandas numpy scikit-learn statsmodels xgboost matplotlib seaborn jupyter
```

**3. Launch Jupyter Notebook**
```bash
jupyter notebook
```
*Navigate to the `notebooks/` folder and open the desired `.ipynb` file to view the analysis.*

---

## 📊 Results Summary

| Task | Outcome / Insights |
| :--- | :--- |
| **Gas Forecasting** | Identified clear seasonal patterns. `SARIMAX` + Fourier features provided stable and robust multi-horizon forecasts. |
| **Contract Valuation** | Custom engine produced realistic contract valuations demonstrating accurate sensitivity to simulated price scenarios. |
| **PD Model (Loans)** | Developed an `XGBoost` model with strong ROC-AUC performance. Successfully generated PD and EL metrics for the entire portfolio. |
| **Mortgage PD** | Achieved clean, interpretable FICO bucketization. The Logistic regression PD outputs perfectly aligned with standard credit risk expectations. |

---

## 🛠️ Skills Demonstrated

- **Time Series Modeling:** `SARIMAX`, Seasonality extraction, Fourier terms
- **Machine Learning:** `XGBoost`, Logistic Regression, Classification metrics
- **Risk Modeling:** Probability of Default (PD), Exposure at Default (EAD), Loss Given Default (LGD), Expected Loss (EL)
- **Financial Modeling:** Derivatives valuation, Storage contract pricing
- **Feature Engineering:** Credit features, Quantization/Bucketization
- **Data Visualization:** `Matplotlib`, `Seaborn`
- **Core Stack:** Python, `pandas`, `NumPy`, `scikit-learn`, `statsmodels`

### License

This project is released under the MIT License.

### Author

Athilakshmi Alagarsamy Quantitative Research | Machine Learning | Financial Modeling
---



