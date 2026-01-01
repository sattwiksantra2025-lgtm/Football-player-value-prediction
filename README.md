# Football-player-value-prediction
ML model predicting football player market values with 98% R² accuracy using Python, Scikit-learn, and Random Forest on 15,905 FC25 players

# ⚽ Football Player Market Value Prediction using Machine Learning

![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)
![scikit-learn](https://img.shields.io/badge/scikit--learn-1.0+-orange.svg)
![License](https://img.shields.io/badge/License-MIT-green.svg)

## 📊 Project Overview

An end-to-end machine learning project that predicts football player market values using the EA Sports FC 25 dataset. The Random Forest model achieves **98% R² accuracy** with only **3% average error**.

## 🎯 Business Problem

Football clubs spend millions on player transfers. This project provides a data-driven approach to:
- Predict player market values accurately
- Identify undervalued talent
- Support transfer negotiations
- Benchmark player valuations

## 📈 Key Results

| Model | R² Score | MAE | MAPE | Status |
|-------|----------|-----|------|--------|
| Linear Regression | 0.75 | €4.0M | 17.86% | Baseline |
| **Random Forest** | **0.98** | **€0.86M** | **3.09%** | ✅ Best |

**Improvement:** 30.65% better than baseline

## 🔍 Feature Importance

- **Overall Rating (OVR):** 68.1% - Primary value driver
- **Age:** 29.0% - Career stage impact
- **Other features:** 2.9% - Minor refinements

## 🛠️ Tech Stack

- **Language:** Python 3.8+
- **Libraries:** Pandas, NumPy, Scikit-learn, Matplotlib, Seaborn
- **ML Models:** Linear Regression, Random Forest Regressor
- **Tools:** Jupyter Notebook

## 📁 Dataset

- **Source:** EA Sports FC 25 Player Database
- **Size:** 15,905 players
- **Features:** 26 original features + 6 engineered features
- **Attributes:** Overall rating, age, position, pace, shooting, passing, dribbling, defending, physical

## 🚀 Project Workflow

1. **Data Loading & Exploration**
   - Loaded 17,470 players from CSV
   - Initial data quality assessment

2. **Data Cleaning**
   - Filtered male players (15,905 remaining)
   - Removed low-rated players (OVR < 40)
   - Handled missing values

3. **Feature Engineering**
   - Position categories (Attacking, Midfield, Defending, Goalkeeper)
   - Age groups (Youth, Prime_Young, Prime_Peak, Experienced, Veteran)
   - Composite scores (Attack, Midfield, Defense)

4. **Target Variable Creation**
   - Synthetic market values using football economics
   - Exponential scaling with player rating
   - Age multipliers for peak years (25-27)
   - Position premiums

5. **Model Training**
   - Train/test split (80/20)
   - Linear Regression (baseline)
   - Random Forest (100 trees, max_depth=20)

6. **Evaluation & Validation**
   - Metrics: R², MAE, RMSE, MAPE
   - Feature importance analysis
   - Sample predictions on real players

## 📊 Visualizations

### Feature Importance
![Feature Importance](images/feature_importance.png)

### Actual vs Predicted
![Actual vs Predicted](images/actual_vs_predicted.png)

### Sample Predictions
Example predictions with 0-7% error range on test players.

## 💡 Key Insights

1. **Overall Rating is King:** Accounts for 68% of predictive power
2. **Age Matters:** Peak years (25-27) command premium values
3. **Non-linear Relationships:** Random Forest captures exponential value scaling better than Linear Regression
4. **Model Generalization:** Consistent accuracy across different player tiers

## 🎓 Skills Demonstrated

- ✅ Data cleaning & preprocessing
- ✅ Feature engineering
- ✅ Machine learning model selection
- ✅ Model evaluation & comparison
- ✅ Data visualization
- ✅ Business domain knowledge application
- ✅ Statistical analysis & interpretation

## 🚀 Installation & Usage

### Prerequisites
```bash
pip install -r requirements.txt

