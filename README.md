# Geospatial Loan Default Risk Prediction for Agriculture
This project implements a machine learning pipeline to predict agricultural loan default risks for farmers in Azerbaijan by integrating traditional tabular financial data with satellite-based remote sensing and geospatial indicators.

## 📌 Project Overview
Assessing credit risk in agriculture requires evaluating environmental factors. This repository demonstrates how to merge borrower data with satellite agro-indices to capture climate risks (like droughts or shifting rainfall patterns) that directly impact a farmer's capacity to repay loans.

---

## 🛠️ Data Sources & Integration

The dataset models a hybrid data fusion approach combining 4 distinct types of information based on geographic coordinates:
1. **Farmer Loan Records:** Mimics Lending Club loan metrics (amounts, interest rates, titles filtered for agricultural workers).
2. **Vegetation Index (NDVI):** Simulates NASA MODIS (MOD13A3) monthly indices to monitor crop health.
3. **Climate & Rainfall:** Simulates NASA POWER monthly precipitation anomalies.
4. **Soil Properties:** Simulates SoilGrids V2.0 indicators for soil quality score.
5. **Market Accessibility (Bonus):** Calculates distance from the farm coordinates to major regional markets/hubs.

---

## 🚀 Key Features

* **Spatial Feature Engineering:** Derives a critical `drought_flag` when $NDVI < 0.2$ and computes rainfall deviation percentages.
* **XGBoost Classification:** Implements a tuned gradient boosting framework optimized to prevent overfitting on complex agro-indicators.
* **Explainable AI (XAI):** Utilizes **SHAP (SHapley Additive exPlanations)** to dissect black-box predictions and isolate environmental triggers for defaults.

---

## 📊 Repository Structure

```text
├── agro-loan-geospatial-risk/
│   ├── Predict_Loan_Default_Geospatial.ipynb   # Main Google Colab / Jupyter Notebook
│   ├── note.md                                  # Task-specific insights & metrics report
│   └── README.md                                # Project documentation
