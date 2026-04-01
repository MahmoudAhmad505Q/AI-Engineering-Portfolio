# 📱 Mobile Price Range Classification (PyTorch)

## 📌 Project Overview
In the fast-paced electronics market, pricing devices accurately based on their hardware specifications is crucial for e-commerce platforms and retailers. This project leverages Deep Learning to classify mobile phones into distinct price ranges based on features like RAM, battery power, camera megapixels, and connectivity options (4G/WiFi).

**Key Achievement:** Designed and trained a Custom Artificial Neural Network (ANN) from scratch using **PyTorch**, achieving a high classification accuracy of **~93.5%**.

## 🛠️ Tech Stack & Tools
* **Deep Learning Framework:** PyTorch (Neural Networks, Custom DataLoaders, Tensors)
* **Data Processing:** Pandas, NumPy, Scikit-Learn (StandardScaler, Train-Test Split)
* **Evaluation Metrics:** Accuracy Score, Confusion Matrix, Classification Report

## 🧠 The Deep Learning Pipeline

### 1. Data Preprocessing & Engineering
* Transformed categorical features (e.g., `dual_sim`, `four_g`, `wifi`, `touch_screen`) into machine-readable formats.
* Applied **Standard Scaling** to normalize hardware specifications, ensuring the Neural Network converges efficiently.
* Converted the cleaned datasets into **PyTorch Tensors** and utilized `DataLoader` for optimized batch processing.

### 2. Neural Network Architecture
* Built a custom multi-layer Artificial Neural Network (ANN) utilizing PyTorch's `nn.Module`.
* Implemented hidden layers with non-linear activation functions (ReLU) to capture complex relationships between hardware specs and price categories.

### 3. Model Training & Evaluation
* Trained the model using `CrossEntropyLoss` and the `Adam` optimizer.
* Evaluated model predictions using `torch.argmax` to determine the highest probability class for each device.
* The model successfully predicts the correct price tier with high precision and recall across all categories.

## 💡 Business Value
This project demonstrates the ability to build robust classification systems that can automatically categorize new inventory, helping businesses automate pricing strategies and optimize their product catalogs based on technical specifications.
