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

* Accuracy:91.99%
* Precision:0.8661
* Recall:0.5803
* F1 Score:0.6949
* Confusion Matrix (for each label)
<img width="558" height="474" alt="image" src="https://github.com/user-attachments/assets/04df685a-9e6b-4754-9c5d-b2aa1dc7335e" />
<img width="561" height="481" alt="image" src="https://github.com/user-attachments/assets/29f9f608-f6f4-4215-875f-0c5e7e5bfd32" />
<img width="562" height="479" alt="image" src="https://github.com/user-attachments/assets/1d31ffb9-b3dd-4c1c-b99b-3412fced2e9f" />
<img width="558" height="471" alt="image" src="https://github.com/user-attachments/assets/ec316222-6e22-4159-826f-72c457b955a9" />
<img width="563" height="475" alt="image" src="https://github.com/user-attachments/assets/731ab7a9-d991-4fe3-9de3-49ec3a34705b" />
<img width="562" height="465" alt="image" src="https://github.com/user-attachments/assets/5587ad17-3965-4d49-8fc8-101f4ab25157" />
---

### 🔹 8. Visualization
* Accuracy vs Iterations graph
<img width="591" height="453" alt="image" src="https://github.com/user-attachments/assets/1c58faa6-8659-44ac-8968-b84629c6066f" />
* Loss Curve
<img width="574" height="457" alt="image" src="https://github.com/user-attachments/assets/62e4d5d5-f070-417d-9aec-6b353a082eae" />
* Bar graph showing toxicity percentages
* <img width="1603" height="899" alt="image" src="https://github.com/user-attachments/assets/858a3904-0e38-4985-9e49-caf7d063cd50" />
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
## Dataset

Due to size limitations, the dataset is not included in this repository.

📥 [Download Dataset](https://drive.google.com/file/d/1a0yvb8bR0hjrdjLg1zxK-nWP29bPpIqQ/view?usp=sharing)
## ▶️ How to Run

1. Install dependencies:

```
pip install pandas scikit-learn gradio nltk
```

2. Mount Google Drive (if using Colab)

3. Run the notebook step-by-step

4. Launch Gradio interface

---

