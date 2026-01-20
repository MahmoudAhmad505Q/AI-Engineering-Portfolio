# 🚗 Vehicle Price Prediction

## 📌 Project Overview
Buying a used car can be challenging due to varying factors like engine condition, mileage, and brand value. This project builds a Machine Learning model to predict the selling price of used cars based on their specifications.

## 🛠️ Technologies Used
* **Python** (Pandas, NumPy, Re)
* **Machine Learning** (Random Forest Regressor)
* **Data Cleaning** (Regular Expressions for unit removal)

## ⚙️ Key Steps
1.  **Advanced Data Cleaning:** Used **Regex** to extract numerical values from mixed columns like `mileage` (e.g., "20 kmpl" → 20) and `engine` (e.g., "1200 CC" → 1200).
2.  **Feature Engineering:** Extracted `Brand` name from the car title to use as a feature.
3.  **Modeling:** Employed **Random Forest Regressor**, which handles non-linear relationships well, achieving excellent accuracy.

## 📊 Results
* **R² Score:** ~0.96 (High Accuracy)
* The model successfully identifies key price drivers like Engine Power and Car Age.
