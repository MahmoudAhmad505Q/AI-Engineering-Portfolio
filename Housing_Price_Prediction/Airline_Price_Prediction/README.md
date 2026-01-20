# ✈️ Airline Ticket Price Prediction

## 📌 Project Overview
Buying flight tickets can be tricky due to dynamic pricing. This project aims to predict the prices of flight tickets based on various factors like airline, source, destination, route, and timing. The model helps in understanding the key drivers of ticket pricing and provides accurate price estimations.

## 🛠️ Technologies Used
* **Python** (Pandas, NumPy)
* **Data Visualization** (Matplotlib, Seaborn)
* **Machine Learning** (XGBoost, Scikit-Learn)
* **Feature Engineering** (Time-series handling, One-Hot Encoding)

## ⚙️ Key Steps
1.  **Data Cleaning:** Handled missing values and standardized formats for Duration, Arrival, and Departure times.
2.  **Feature Engineering:**
    * Extracted `Day`, `Month`, `Hour`, and `Minute` from timestamp columns.
    * Converted complex duration strings (e.g., "2h 50m") into total minutes.
    * Mapped `Total_Stops` to ordinal values.
3.  **Outlier Removal:** Identified and removed extreme price outliers (> 40k) to stabilize the model.
4.  **Transformation:** Applied **Log Transformation** to the target variable (`Price`) to handle skewed distribution.
5.  **Model Training:** Trained an **XGBoost Regressor** with optimized hyperparameters.

## 📊 Results
The model achieved high accuracy in predicting flight fares:
* **R² Score:** 0.8529 (85.29%)
* **Performance:** The model effectively captures 85% of the variance in ticket prices, providing reliable estimates within a standardized error margin.

## 🚀 How to Run
1.  Clone the repository.
2.  Install dependencies: `pip install pandas numpy scikit-learn xgboost matplotlib seaborn`.
3.  Run the Jupyter Notebook `AirLine.ipynb`.
