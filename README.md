# 🧠 Advanced Toxic Comment Analyzer (NLP + Machine Learning)

---

## 📌 Overview

This project is an **NLP-based multi-label text classification system** that detects different types of toxic comments.
It uses **TF-IDF + Logistic Regression** along with **Gradio UI** to analyze and visualize toxicity in user input.

---

## 🎯 Problem Statement

Online platforms face issues with harmful and abusive comments. This project builds an automated system to classify comments into multiple toxicity categories.

---

## 📊 Dataset

* **Dataset Used:** Jigsaw Toxic Comment Dataset
* **Input:** `comment_text`
* **Output Labels:**

  * toxic
  * severe_toxic
  * obscene
  * threat
  * insult
  * identity_hate

---

## ⚙️ Technologies Used

* Python
* Scikit-learn
* NLTK
* Pandas, NumPy
* Matplotlib, Seaborn
* Gradio
* Google Colab

---

## 🧠 Methodology

### 🔹 1. Data Loading

* Dataset loaded from Google Drive
* Exploratory analysis using value counts

---

### 🔹 2. Text Preprocessing

* Convert text to lowercase
* Remove special characters using regex
* Remove stopwords
* Apply lemmatization using WordNet

---

### 🔹 3. Feature Extraction

* Used **TF-IDF Vectorization**
* Converted text into numerical feature vectors
* Limited to top 5000 features

---

### 🔹 4. Model Building

* Used **Logistic Regression**
* Applied **MultiOutputClassifier** for multi-label classification

---

### 🔹 5. Training

* Dataset split:

  * 80% Training
  * 20% Testing

---

### 🔹 6. Prediction

* Model predicts multiple labels simultaneously
* Probabilities converted to percentage for better interpretation

---

### 🔹 7. Evaluation Metrics

* Accuracy
* Precision
* Recall
* F1 Score
* Confusion Matrix (for each label)

---

### 🔹 8. Visualization

* Confusion Matrix using heatmaps
* Accuracy vs Iterations graph
* Loss Curve
* Bar graph showing toxicity percentages

---

### 🔹 9. User Interface

* Built using **Gradio**
* User enters a comment
* Output:

  * Toxicity percentage table
  * Graph visualization

---

## 📈 Results

* Model successfully classifies toxic comments
* Achieved high accuracy (~90%)
* Loss decreases over iterations
* Good generalization (train ≈ test accuracy)

---

## 📊 Example Output

**Input:**

```
You are stupid idiot
```

**Output:**

| Category | Percentage |
| -------- | ---------- |
| toxic    | 92%        |
| insult   | 85%        |
| threat   | 5%         |

---

## 🚀 Features

✔ Multi-label classification
✔ Real-time prediction using UI
✔ Graph-based visualization
✔ Efficient and lightweight model

---

## ⚠️ Limitations

* Cannot fully understand sarcasm
* Depends on dataset quality
* May misclassify complex sentences

---

## 🔮 Future Improvements

* Use Deep Learning models (LSTM, BERT)
* Improve accuracy with larger dataset
* Deploy as web/mobile application
* Add real-time moderation system

---

## 🏁 Conclusion

This project demonstrates how **NLP and Machine Learning** can be used to detect toxic comments effectively. The system provides accurate predictions along with visualization, making it useful for real-world applications like content moderation.

---

## ▶️ How to Run

1. Install dependencies:

```
pip install pandas scikit-learn gradio nltk
```

2. Mount Google Drive (if using Colab)

3. Run the notebook step-by-step

4. Launch Gradio interface

---

