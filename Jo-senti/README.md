# 🇯🇴 Jo-Senti: Jordanian Dialect Sentiment Analyzer

![Python](https://img.shields.io/badge/Python-3.8%2B-blue)
![Scikit-Learn](https://img.shields.io/badge/Library-Scikit--Learn-orange)
![NLP](https://img.shields.io/badge/NLP-Arabic-green)
![Status](https://img.shields.io/badge/Status-Completed-success)

> **Jo-Senti** is a smart hybrid sentiment analysis system designed specifically for the **Jordanian Arabic dialect**. It uniquely combines classical Machine Learning with linguistic rules to accurately detect sentiment in slang, social media comments, and complex negations.

---

## 📸 Demo

![App Interface](https://via.placeholder.com/800x400?text=App+Screenshot+Placeholder)

---

## 💡 The Problem
Standard NLP models struggle with Arabic dialects, especially Jordanian slang. They often fail due to:
* **Negation Complexity:** Phrases like *"Mesh Battal"* (Not bad) are mathematically treated as double negatives or misclassified.
* **Slang Blindness:** Cultural terms like *"Kafu"* (Great/Brave) or *"Nashmi"* are unknown to general pre-trained models.
* **Rich Morphology:** The diverse forms of Arabic words confuse simple vectorizers.

## 🛠️ The Solution: A Hybrid Approach
This project implements a **2-layer decision logic** to ensure high accuracy:

1.  **Layer 1: Golden Keyword & Phrase Matching (Rule-Based)**
    * The system scans for specific Jordanian cultural terms (e.g., *'Bishahi'*, *'Kafu'*) and compound phrases (e.g., *'Ya3teek Al Afyah'*).
    * This layer acts as an override to ensure 100% accuracy on known dialect terms.

2.  **Layer 2: Machine Learning (Logistic Regression)**
    * If no keywords are found, the text is processed via a custom **ISRI Stemming** pipeline and TF-IDF Vectorization.
    * A tuned Logistic Regression model (Accuracy ~86.4%) predicts the sentiment probability.

---

## 🚀 Features

* ✅ **Dialect-Aware:** Specifically tuned for Jordanian terms like "Nashmi", "Zaki", "Kharafi".
* ✅ **Phrase Support:** Correctly interprets compound negations (e.g., "Mesh Battal" -> Positive).
* ✅ **Smart Cleaning:** Custom preprocessing pipeline that removes stop words while preserving dialect semantics.
* ✅ **Interactive UI:** Built-in Jupyter Widget for real-time testing and visualization.

---

## 💻 Tech Stack

* **Language:** Python 3.x
* **ML Core:** Scikit-Learn, Pandas, NumPy
* **NLP Tools:** NLTK (Stopwords, Stemming), Regex
* **Dataset:** [AJGT (Arabic Jordanian General Tweets)](https://huggingface.co/datasets/komari6/ajgt_twitter_ar)
* **Interface:** IPyWidgets

---

## 📂 Project Structure

```bash
Jo-Senti/
│
├── jo-Senti.ipynb         # Main Jupyter Notebook (Training Pipeline + UI App)
├── jo_senti_model.pkl     # Trained Logistic Regression Model
├── tfidf_vectorizer.pkl   # TF-IDF Vectorizer Artifact
└── README.md              # Project Documentation
