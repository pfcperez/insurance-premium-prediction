# Insurance Premium Prediction - Linear Regression Model

[![Python](https://img.shields.io/badge/python-3.11+-blue.svg)](https://www.python.org)
[![Scikit-learn](https://img.shields.io/badge/Scikit--learn-Latest-orange.svg)](https://scikit-learn.org/)

## 📝 Overview

Data engineering pipeline that transforms insurance customer data and applies Linear Regression to predict medical insurance charges based on demographic and health factors.

- **Dataset:** 1,338 insurance records × 7 features
- **Target:** Annual Charges ($1K - $63K)
- **Model Performance:** R² Score 0.74 | MSE 36.45M
- **Business Application:** Premium estimation & risk pricing

---

## 🎯 Key Features

✅ Load insurance claim dataset (CSV)  
✅ Customer demographics analysis (age, sex, region)  
✅ Exploratory analysis of charges vs features  
✅ Categorical encoding (sex, smoker, region)  
✅ Feature scaling & normalization  
✅ Linear Regression model  
✅ R² and MSE evaluation  

---

## 🛠️ Tech Stack

- **Python 3.11+** | Pandas | NumPy
- **Visualization:** Matplotlib, Seaborn
- **ML:** Scikit-learn LinearRegression
- **Development:** Jupyter Notebook

---

## 📦 Installation

```bash
# Clone repo
git clone https://github.com/pfcperez/insurance-premium-prediction.git
cd insurance-premium-prediction

# Create virtual environment
python -m venv venv
source venv/bin/activate

# Install dependencies
pip install pandas numpy matplotlib seaborn scikit-learn jupyter

---

## 🚀 Usage

```bash
jupyter notebook insure.ipynb
```

**Pipeline Steps:**
1. Load insurance customer data (1,338 records × 7 features)
2. Exploratory analysis (age, BMI, charges distributions)
3. Detect correlations between features and charges
4. One-hot encode categorical variables (sex, smoker, region)
5. Standardize numerical features (age, BMI)
6. Split data 80/20 (train/test)
7. Train Linear Regression model
8. Evaluate with R² Score and Mean Squared Error

---

## 📊 Results

| Metric | Value |
|--------|-------|
| **R² Score** | 0.74 |
| **MSE (Mean Squared Error)** | 36,454,308.61 |
| **Training Records** | ~1,069 |
| **Test Records** | ~269 |

**Interpretation:** Model explains 74% of variance in charges. Average squared prediction error is ~$6,038 per prediction.

---

## 🔑 Features

- **age** - Customer age (18-64)
- **sex** - Male/Female
- **bmi** - Body Mass Index
- **children** - Number of dependents
- **smoker** - Smoker status (Yes/No)
- **region** - US region (northeast, northwest, southeast, southwest)
- **charges** - Annual medical costs (target variable)

---

## 📁 Project Structure

```
insurance-prediction-pipeline/
├── insurance.ipynb              # Main notebook
├── README.md
├── requirements.txt
└── data/
    ├── raw/
    │   └── insurance.csv
```

---

## 🔑 Data Transformations

- **Categorical Encoding:** One-hot encoding for sex, smoker, region
- **Feature Scaling:** Standardization for age, BMI, children
- **Missing Values:** None detected in dataset
- **Train/Test Split:** 80/20 split

---

## 📊 Feature Importance (Coefficients)

From Linear Regression coefficients:
- **Smoker Status:** +$24,120 (biggest impact!)
- **Age:** ~+$255 per year
- **BMI:** +$151 per unit
- **Region variations:** -$694 to +$434
- **Sex & Children:** Moderate impact

**Key Insight:** Being a smoker is the strongest predictor of insurance costs.

---

## 📚 Kaggle Dataset

Source: [Medical Cost Personal Datasets](https://www.kaggle.com/datasets/mirichoi0218/insurance)

---

**Author:** Ramiro Pérez | [GitHub](https://github.com/pfcperez)  
**Status:** ✅ Complete
