# 🎬 Cinema-Cluster: Advanced Content Grouping using NLP & Unsupervised ML

![Python](https://img.shields.io/badge/Python-3.12-blue?style=flat-square&logo=python)
![Scikit-Learn](https://img.shields.io/badge/Scikit--Learn-Latest-orange?style=flat-square&logo=scikit-learn)
![NLP](https://img.shields.io/badge/NLP-TF--IDF-red?style=flat-square)

## 🌟 Overview
How does Netflix group thousands of titles to suggest the perfect "Next Watch"? This project explores the power of **Unsupervised Machine Learning** to categorize movies and TV shows based on their textual DNA (Descriptions, Cast, and Genres). 

The highlight of this repository is the comparative analysis between **Hard Clustering ($K$-Means)** and **Soft Clustering (Gaussian Mixture Models - GMM)**, demonstrating how AI handles the "gray areas" of cinema genres.

---

## 🧠 Technical Pipeline

1.  **Text Engineering:** * Feature Aggregation: Concatenated `description`, `cast`, and `listed_in`.
    * Vectorization: **TF-IDF** (Term Frequency-Inverse Document Frequency) with 1,000 max features.
2.  **Dimensionality Reduction:** * **TruncatedSVD:** Reduced features from 1,000 to 100 to handle sparse matrices efficiently.
    * **PCA:** Projected high-dimensional data into a 2D space for visualization.
3.  **Optimization:** * Used the **Elbow Method** and **Silhouette Analysis** to determine the optimal $k=3$.

---

## 📊 Key Findings

By analyzing the clusters, we identified three distinct content "continents":

* **Cluster 0 (Global Cinema):** Dominated by International Movies and Independent Dramas.
* **Cluster 1 (Family & Reality):** A mix of Children’s content, Comedies, and Documentaries.
* **Cluster 2 (The Stand-up Hub):** A highly specialized cluster containing nearly 100% Stand-Up Comedy.

### ⚖️ The "Soft Clustering" Edge (GMM vs. KMeans)
In a test with an ambiguous description: *"A story about a man and a car in a city."*
* **$K$-Means:** Forced a hard assignment to **Cluster 2**.
* **GMM:** Revealed the true nature of the text, showing a **51.2% / 48.8%** probability split between two clusters. This proves the model's ability to recognize "hybrid" content.

---

## 🛠️ Tech Stack & Environment
* **Machine:** HP Victus 15 (RTX 4050, i5-13420H)
* **OS:** WSL 2 (Ubuntu 24.04)
* **Libraries:** `pandas`, `scikit-learn`, `nltk`, `matplotlib`

---

## 📈 Visualizations
The project includes detailed plots for:
* **Inertia & Silhouette Scores** for $k$ optimization.
* **Centroid Visualization** in the feature space.
* **GMM Probability Maps** using 2D PCA projection.

---

## 🚀 Future Roadmap
* [ ] Implement **BERT/Sentence-Transformers** for deeper semantic analysis.
* [ ] Build a **Streamlit** Web App for real-time movie classification.
* [ ] Integrate the **OpenSooq** dataset for localized car price/description clustering.

---
**Developed by:** Mahmoud Ahmad  
*Passionate about AI Engineering and Data Science.*
