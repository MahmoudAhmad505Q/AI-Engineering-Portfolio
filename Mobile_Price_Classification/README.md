# 📱 Mobile Price Range Classification

## 📌 Project Overview
Unlike typical regression problems, this project is a **Classification Task**. The goal is to categorize mobile phones into one of four price ranges (0: Low Cost, 1: Medium, 2: High, 3: Very High) based on features like RAM, Battery Power, and Camera quality.

## 🛠️ Technologies Used
* **Python** (Pandas, Scikit-Learn)
* **Machine Learning** (Support Vector Machine - SVM)
* **Data Visualization** (Seaborn Heatmaps)

## ⚙️ Key Methodology
1.  **Data Analysis:** Explored relationships between hardware specs (RAM, Battery) and price categories.
2.  **Scaling:** Applied `StandardScaler` to normalize features, which is crucial for distance-based algorithms like SVM.
3.  **Modeling:** Implemented **SVC (Support Vector Classifier)** with a linear kernel.

## 📊 Results
* **Accuracy:** ~95%+ 
* **Confusion Matrix:** Shows very few misclassifications, proving the model's reliability in distinguishing between price tiers.
