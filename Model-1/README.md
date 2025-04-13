
# Toxic Comment Classification – Logistic Regression with TF-IDF

## 📌 Project Overview

This project addresses the challenge of classifying toxic content in online feedback using machine learning. The task is a multi-label classification problem where each comment can have one or more types of toxicity, including `abusive`, `vulgar`, `menace`, `offense`, and `bigotry`.

The main objective is to build a model that accurately detects whether a piece of content is toxic or not, using both fine-grained category information and text features extracted via TF-IDF. The final output is a binary "toxic" classification used for evaluation.

---

## 📂 Dataset Description

The dataset consists of two files:

- `train.csv`: Labeled training data with the following columns:
  - `id`: Unique identifier
  - `feedback_text`: Text of the comment
  - `toxic`: Target binary label
  - `abusive`, `vulgar`, `menace`, `offense`, `bigotry`: Supplementary binary labels

- `test.csv`: Unlabeled data on which predictions are to be made.

**Note**: Although the model uses all labels for training, only the `toxic` label is used for final evaluation.

---

## 🔧 Model Implementation Details

This notebook implements a **baseline model** using:

- **Text Vectorization**: TF-IDF (Term Frequency-Inverse Document Frequency)
- **Model**: Logistic Regression

### Key Steps:
1. **EDA**: Visualizations of toxicity distribution and common word patterns
2. **Preprocessing**: Lowercasing, removing stop words, lemmatization, etc.
3. **TF-IDF Vectorization**: Conversion of text into numeric features
4. **Model Training**: Logistic Regression fitted on TF-IDF features
5. **Evaluation**: Using Accuracy, Precision, Recall, F1-Score, Confusion Matrix, and AUC-ROC

---

## ▶️ Steps to Run the Code

1. Clone the repository:
   ```bash
   git clone https://github.com/podderSoykot/Sentiment-Analysis.git
   cd Sentiment-Analysis/Model-1
   ```

2. Install the dependencies:
   ```bash
   pip install -r requirements.txt
   ```

3. Launch Jupyter Notebook and run:
   ```bash
   jupyter notebook Logisticregression_with_Tfidf.ipynb
   ```

---

## 📈 Model Evaluation Results

| Metric        | Score    |
|---------------|----------|
| Accuracy      | ~0.91    |
| Precision     | ~0.90    |
| Recall        | ~0.89    |
| F1-Score      | ~0.89    |
| AUC-ROC       | ~0.92    |

> 📌 These scores are approximate and may vary depending on random state or preprocessing tweaks.

---

## 📌 Additional Observations

- **Class Imbalance**: Addressed using weighted Logistic Regression.
- **Multilingual Challenge**: The current baseline model focuses on English text; multilingual performance may be limited.
- **Extendability**: The modular pipeline makes it easy to replace the classifier or switch to word embeddings or transformers for enhanced accuracy.

---

## ✅ Future Improvements

- Integrate multilingual transformers (like XLM-Roberta) for better generalization.
- Use SMOTE or other resampling techniques to further address class imbalance.
- Add explainability tools like SHAP to understand model predictions.

---

Feel free to explore other advanced models in the [`Model-2`](../Model-2) directory.
