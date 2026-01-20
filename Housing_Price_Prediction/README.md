# 🏠 Advanced Housing Price Prediction

## 📌 Project Overview
Predicting house prices is a classic regression problem that requires deep understanding of feature correlations. This project uses an advanced **XGBoost** regression model to predict house sales prices based on features like square footage, location (neighborhood), overall quality, and year built.

## 🛠️ Technologies Used
* **Python** (Pandas, NumPy)
* **Machine Learning** (XGBoost, Scikit-Learn)
* **Data Preprocessing** (StandardScaler, Log-Transform)
* **Visualization** (Seaborn, Matplotlib)

## ⚙️ Key Methodology
1.  **Data Preprocessing:**
    * Handled missing data.
    * Performed **One-Hot Encoding** for categorical features like `Neighborhood`.
2.  **Feature Engineering:**
    * Created a new strong predictor: `TotalSF` (Total Square Footage) by combining Basement, 1st Floor, and 2nd Floor areas.
3.  **Outlier Detection:** Removed "Noise" data points (e.g., properties with huge square footage but unusually low prices) to prevent model skewing.
4.  **Target Transformation:** Applied `np.log1p` to the `SalePrice` to normalize the distribution and improve prediction accuracy for lower and higher-end properties simultaneously.
5.  **Modeling:** Utilized **XGBoost Regressor** with a "slow learning" approach (low learning rate, high estimators) for maximum precision.

## 📊 Results
* **Model:** XGBoost Regressor
* **Metric:** Root Mean Squared Error (RMSE) & R² Score.
* The model demonstrates strong predictive power, effectively handling complex relationships between housing features.

## 🚀 How to Run
1.  Clone the repository.
2.  Ensure `train.csv` is in the project directory.
3.  Run `housing_price.ipynb` to see the preprocessing pipeline and model output.
