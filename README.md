# 🚗 Car Price Prediction using Machine Learning

## 📌 Project Overview

This project focuses on predicting the price of used cars based on various features such as brand, mileage, engine volume, year, and more.
The goal is to build a robust regression model that can estimate car prices with good accuracy.

---

## 🧠 Problem Statement

Used car prices vary significantly based on multiple factors.
This project aims to:

* Analyze the dataset
* Perform data preprocessing and feature engineering
* Train a machine learning model
* Predict car prices based on user input

---

## 📊 Dataset

The dataset contains **9576 rows and 10 features**, including:

* `car` → Brand of the car
* `price` → Target variable (car price)
* `body` → Car body type
* `mileage` → Distance traveled
* `engV` → Engine volume
* `engType` → Fuel type
* `registration` → Registration status
* `year` → Manufacturing year
* `model` → Car model
* `drive` → Drive type

---

## ⚙️ Data Preprocessing

* Handled missing values (`engV`, `drive`)
* Removed outliers (top 1% of price & mileage)
* Created new features:

  * `car_age` = current year - manufacturing year
* Applied encoding using `pd.get_dummies()`
* Log transformation on target variable (`price`) to handle skewness

---

## 🧩 Feature Engineering

* Brand grouping (top brands vs others)
* Mileage transformation (`log`)
* Handling categorical variables
* Ensuring consistent feature space for prediction

---

## 🤖 Model Used

* **Random Forest Regressor**

  * `n_estimators = 300`
  * `max_depth = 15`
  * `min_samples_split = 5`

---

## 📈 Model Performance

| Metric   | Value      |
| -------- | ---------- |
| R² Score | ~0.68      |
| MAE      | ~2200–3600 |

👉 The model explains approximately **68% of variance** in car prices.

---

## 📊 Visualization

* Scatter plot of **Actual vs Predicted prices**
* Helps analyze model performance and error distribution

---

## 🔮 Prediction System

The model allows users to input:

* Car brand
* Mileage
* Engine volume
* Year
* Fuel type
* Body type
* Drive type

👉 And returns the **predicted price**

---

## 🚀 How to Run

```bash
# Install dependencies
pip install pandas numpy scikit-learn matplotlib
```

```python
# Run notebook or script
python main.py
```

---

## 🧠 Key Learnings

* Importance of feature engineering over model complexity
* Handling data leakage in ML pipelines
* Understanding overfitting vs underfitting
* Proper evaluation using R² instead of accuracy

---

## ⚠️ Limitations

* Dataset lacks important features like:

  * Car condition
  * Accident history
  * Location
* Model performance is limited by available data

---

## 📌 Future Improvements

* Use advanced models like XGBoost
* Deploy as a web app (Streamlit)
* Add more real-world features

---

## 👨‍💻 Author

Shikhar Khanna
B.Tech 2nd year Student

---

## ⭐ If you like this project, give it a star!
