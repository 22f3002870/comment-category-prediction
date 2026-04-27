# comment-category-prediction
Kaggle ML project for multi-class text classification using TF-IDF and Logistic Regression

#  Comment Category Prediction (Kaggle)

## 📌 Problem Statement

Predict the category (0–3) of user comments using text and metadata.

This is a **multi-class text classification problem** with imbalanced classes.

---

## 📊 Dataset Overview

* Train: 198,000 rows
* Test: 102,000 rows
* Features:

  * Text: `comment` (most important)
  * Numerical: upvotes, downvotes, interaction flags
  * Categorical: race, religion, gender (dropped)

---

## 🔍 Key Insights (EDA)

* ⚠️ Severe class imbalance → used **F1-score (macro)**
* ❌ 73% missing values in categorical features → dropped
* 📉 Highly skewed numerical data → scaled
* 🧠 Text dominates prediction power

---

## ⚙️ Feature Engineering

* `comment_len`
* `word_count`
* TF-IDF (word + character level)

---

## 🤖 Models Used

| Model               | F1 Score   |
| ------------------- | ---------- |
| Logistic Regression | 0.7856     |
| SGD Classifier      | 0.7716     |
| Naive Bayes         | 0.305      |
| ✅ Final Model       | **0.8026** |

---

## 🏆 Best Model

* Dual TF-IDF (word + char)
* Logistic Regression (C=0.8)
* class_weight = balanced

---

## 💡 Key Learnings

* Text features > metadata
* Removing noisy features improved performance
* Character n-grams handle misspellings

---

## 📁 Project Structure

```
notebooks/
data/
outputs/
images/
```

---

## ▶️ How to Run

```bash
pip install -r requirements.txt
```

Open notebook and run all cells.

---

## 📌 Future Improvements

* Try BERT / Transformer models
* Better handling of class imbalance
* Hyperparameter tuning with GridSearch

---

## 👨‍💻 Author

Parkhi Yadav

