# 🏡 House Price Prediction using Machine Learning

This project predicts house prices based on various features such as overall quality, size, number of rooms, garage capacity, and year built. It uses multiple regression models to analyze relationships and deliver accurate price predictions.

---

## 📊 Project Overview

In the modern real estate market, accurate price estimation is crucial.  
This project applies **Multiple Linear Regression**, **Ridge**, and **Lasso** regression techniques to predict house prices.

---

## 🚀 Objectives

- Perform **exploratory data analysis (EDA)** to understand trends and correlations.
- Build and evaluate multiple regression models:
  - Linear Regression
  - Ridge Regression (with cross-validation)
  - Lasso Regression (with cross-validation)
- Compare model performances using R², MAE, MSE, RMSE.
- Visualize results and identify the most important features affecting price.

---

## 🧩 Technologies Used

- **Python 3.x**
- **Pandas, NumPy, Matplotlib, Seaborn**
- **Scikit-learn**
- **Jupyter Notebook**

---

## 🧠 Key Steps

### 1️⃣ Data Preprocessing
- Handled missing values and outliers.
- Encoded categorical variables.
- Scaled numerical features using `StandardScaler`.

### 2️⃣ Model Training
- Trained three models:
```python
LinearRegression()
RidgeCV(alphas=[0.1, 1, 10, 100], cv=5)
LassoCV(alphas=[0.0001, 0.001, 0.01, 0.1], cv=5)
```
### 3️⃣ Model Evaluation

| Metric                      | Linear Regression | RidgeCV | LassoCV |
| :-------------------------- | :---------------- | :------ | :------ |
| **R² Score**                | 0.8548            | 0.8534  | 0.8548  |
| **RMSE**                    | 31004             | ~31000  | ~31000  |
| **Best α (Regularization)** | –                 | 100     |0.1     |


✅ Lasso Regression gave the best balance of performance and simplicity.

---

### 4️⃣ Feature Importance

Top features influencing house prices:

- OverallQual	23989
- GrLivArea	14088
- GarageCars	11727
- YearBuilt	10431
- 2ndFlrSF	9734

## 🧾 Results Summary

The model explains ~85% of the variance in house prices.

Regularization helped control overfitting.

Lasso automatically removed less relevant features.