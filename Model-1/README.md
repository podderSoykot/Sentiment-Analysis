# Resume Classification using Logistic Regression and TF-IDF

## 📌 Project Overview
This project focuses on automatic classification of resumes into predefined job categories using natural language processing (NLP) techniques. The goal is to streamline the hiring pipeline by categorizing resumes efficiently.

## 📂 Dataset Description
The dataset contains resumes with corresponding job categories as labels. Each resume is a block of unstructured text. Key steps include:
- Text cleaning (stopwords removal, punctuation, etc.)
- Feature extraction using TF-IDF Vectorizer
- Model training using Logistic Regression

## 🧠 Model Implementation
**Model 1**: Logistic Regression with TF-IDF
- Preprocessing includes stopword removal, tokenization, and lowercasing
- TF-IDF features limited to 800 tokens
- Logistic Regression used as the baseline model

## 🧪 Evaluation Metrics
The following metrics are used to evaluate model performance:
- **Accuracy**
- **Precision**
- **Recall**
- **F1-Score**
- **AUC-ROC**
- **Confusion Matrix**

## ✅ Results
| Metric        | Score   |
|---------------|---------|
| Accuracy      | 87%     |
| Precision     | 85%     |
| Recall        | 86%     |
| F1-score      | 85%     |
| AUC-ROC       | 0.91    |

## 🚀 How to Run
1. Clone this repository.
2. Navigate to the `task/` directory.
3. Open `model1_implementation.ipynb` in Jupyter Notebook or Jupyter Lab.
4. Run each cell in order to perform EDA, preprocessing, training, and evaluation.