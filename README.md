(https://youtu.be/WeJyDgC8ZJU) Team DataJustice
# Boston Police Department (BPD) Budget & Payroll Analysis

## Overview
This project analyzes the Boston Police Department (BPD) budget, payroll, and overtime data to identify spending patterns, compensation trends, and to build machine learning models for predicting overtime expenditures.

The project includes:
- Data preprocessing and cleaning pipelines
- Exploratory data analysis and visualization
- Regression and classification modeling
- A Flask-based web dashboard for insights and predictions

---

## Objectives
- Analyze shifts in funding across departments
- Compare regular pay vs overtime trends
- Identify top-earning employees
- Predict overtime expenditure using machine learning
- Classify employees into high vs low overtime earners
- Build an interactive dashboard to present insights

---

## Dataset

### Source
- **Employee Earnings Data (2024)** — Payroll data for all Boston city employees (filtered for police)
- **Employee Earnings Data (2023)** — Used for testing model generalization

### Preprocessing
- Dropped columns with high missingness: `QUINN_EDUCATION`, `TOTAL_GROSS`
- Filled missing values using `SimpleImputer` and `IterativeImputer`
- Final datasets:
  - `cleaned_police_overtime_data.csv` (2024, ~14k rows)
  - `cleaned_data_test.csv` (2023, ~14k rows)

---

## Workflow

1. Import 2024 payroll data
2. Run `Boston_Police_Overtime.ipynb` → generate cleaned dataset
3. Run `data_visualization.ipynb` → create visual insights
4. Run `ML_Model_DS_Project.ipynb` → train regression models
5. Run `Classification_model.ipynb` → classify high vs low overtime earners
6. Import 2023 payroll data
7. Run `Boston_Police_Overtime_test.ipynb` → clean test dataset
8. Run `ML_Model_DS_test.ipynb` → evaluate models on 2023 data
9. Launch Flask dashboard using `app2.py`

---

## Models

| Model | R² Score | MAE |
|------|----------|------|
| XGBoost Regressor | 0.820 | $2,756 |
| Random Forest Regressor | 0.813 | $2,839 |
| Linear Regression | 0.709 | $4,421 |

### 2023 Test Results

| Model | R² Score | MAE |
|------|----------|------|
| Random Forest | 0.123 | $9,579 |
| XGBoost | 0.045 | $10,011 |

Additional analysis includes SHAP explainability and KMeans clustering of officers based on pay patterns.

---

## Data Visualization
- Department-wise pay distributions
- Top 10 employees by total pay
- Regular vs overtime scatter analysis
- Correlation heatmaps
- Pay component distributions

---

## Running the Project

### Install dependencies
```bash
pip install numpy pandas scikit-learn matplotlib xgboost flask flask_cors

## Tech Stack  
- **Python** (data preprocessing, ML models)  
- **Google Colab** (development environment, notebooks)
- **Visual Studio Code** (development environment)
- **Flask**
- **Javascript** 
- **HTML/CSS Boostrap**
  
# About us:
- Kaushik Joshi
- Ashish Joshi
- Siddhanth Kalyanaraman
- Vidney Jadhav
- Adithya Nayak
