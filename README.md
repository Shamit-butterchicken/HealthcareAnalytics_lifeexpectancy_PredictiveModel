# HealthcareAnalytics_lifeexpectancy_PredictiveModel
# Global Life Expectancy Prediction & Exploratory Analysis

An end-to-end data science and machine learning project analyzing public health, socio-economic factors, and global life expectancy using linear regression.

---

## 📌 Project Overview
This repository investigates key determinants of global life expectancy across 193 nations using WHO public health datasets. The goal of this project is to perform comprehensive exploratory data analysis (EDA), engineer clean data pipelines, evaluate socio-economic correlations, and build a predictive Multiple Linear Regression model.

Key outcomes achieved:
- **Explanatory Power ($R^2$)**: Explained ~81.5% of variance in global life expectancy.
- **Model Accuracy**: Achieved a low test error with an RMSE of ~4.08 years and MAPE of ~4.61%.

---

## 📊 Dataset Summary
- **Observations**: 2,938 rows (country-year instances)
- **Features**: 22 health, economic, and demographic variables
- **Preprocessing**: Imputed missing data using country-level median values with global fallbacks; encoded categorical country status into binary indicators (0 = Developing, 1 = Developed).

---

## 🔍 Key Insights & Analysis
1. **Schooling & Education**: Demonstrates the strongest positive relationship ($r = 0.71$) with life expectancy, highlighting health literacy as a primary driver of longevity.
2. **Adult Mortality & HIV/AIDS**: Show severe inverse relationships ($r = -0.70$ and $r = -0.56$, respectively), emphasizing the impact of infectious disease burdens.
3. **Healthcare Spending vs. Outcomes**: Increasing healthcare expenditure percentage without underlying infrastructure improvements yields minimal lifespan gains in low-life-expectancy countries ($< 65$ years).
4. **Alcohol Consumption (Confounding Variable)**: Higher alcohol consumption correlates positively ($r = 0.40$) with life expectancy due to socio-economic development as a confounding factor—higher-income nations report higher alcohol metrics alongside stronger health infrastructure.

---

## 📈 Model Performance

A **75/25 train-test split** was implemented to evaluate generalizability and ensure zero overfitting:

| Metric | Training Set (75%) | Test Set (25%) | Entire Dataset |
| :--- | :---: | :---: | :---: |
| **$R^2$ Score** | **0.819** | **0.815** | **0.818** |
| **RMSE (Years)** | 4.048 | **4.081** | 4.056 |
| **MAPE (%)** | 4.628% | **4.614%** | 4.625% |

---

## 🛠️ Tech Stack & Libraries
- **Language**: Python 3.x
- **Environment**: Google Colab / JupyterLab
- **Data Wrangling**: Pandas, NumPy
- **Visualization**: Seaborn, Matplotlib
- **Machine Learning**: Scikit-Learn (`LinearRegression`, `train_test_split`, metrics)

---

## 🚀 How to Run
1. Clone this repository:
   ```bash
   git clone [https://github.com/your-username/your-repo-name.git](https://github.com/your-username/your-repo-name.git)
