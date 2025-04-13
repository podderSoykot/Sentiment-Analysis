# Offensive Language Classification

## 🔍 Project Overview

This project focuses on developing machine learning models to detect various types of toxic content in online feedback. The primary objective is to predict whether a given comment is toxic, considering that a comment may exhibit multiple forms of toxicity.

## 📂 Dataset Description

The dataset comprises:

- **train.csv**: Contains labeled training data with the following columns:
  - `id`: Unique identifier for each comment
  - `feedback_text`: The feedback to be classified
  - `toxic`: 1 if the comment is toxic
  - `abusive`: 1 if the comment contains severe toxicity
  - `vulgar`: 1 if the comment contains obscene language
  - `menace`: 1 if the comment contains threats
  - `offense`: 1 if the comment contains insults
  - `bigotry`: 1 if the comment contains identity-based hate

- **test.csv**: Contains unlabeled data for prediction.

**Note**: While the training data includes multiple labels, the final evaluation focuses solely on the binary "toxic" label.

## 🛠️ Model Implementation Details

### Baseline & Advanced Models (`task/model1_implementation.ipynb`)

- **Preprocessing**:
  - Tokenization
  - Lowercasing
  - Removal of stop words, special characters, and punctuation
  - Lemmatization

- **Feature Extraction**:
  - TF-IDF Vectorization

- **Models**:
  - Logistic Regression
  - Random Forest Classifier

### Transformer-Based Models (`task/model2_implementation.ipynb`)

- **Preprocessing**:
  - Utilized Hugging Face's `transformers` library for tokenization and encoding.

- **Model**:
  - Fine-tuned BERT (Bidirectional Encoder Representations from Transformers) for sequence classification.


---

## 📑 Performance_Analysis_Report.pdf Outline

**Title**: Performance Analysis Report - Offensive Language Classification

**1. Introduction**

- Overview of the project objectives.
- Importance of detecting toxic content in online platforms.

**2. Dataset Overview**

- Description of the dataset structure.
- Distribution of labels and handling of class imbalance.

**3. Exploratory Data Analysis (EDA)**

- Visualization of label distribution across toxicity types.
- Analysis of sentence lengths and word distributions.
- Identification of common words and phrases associated with toxicity.

**4. Preprocessing Techniques**

- Detailed steps of text preprocessing.
- Justification for chosen preprocessing methods.

**5. Model Development**

- Description of baseline and advanced models.
- Architecture and training details of the transformer-based model.

**6. Evaluation Metrics**

- Presentation of accuracy, precision, recall, F1-score, and AUC-ROC for each model.
- Confusion matrices illustrating model performance.
- ROC curves comparing model capabilities.

**7. Model Optimization**

- Hyperparameter tuning strategies employed.
- Impact of different optimizers and learning rates on model performance.

**8. Multilingual Considerations**

- Challenges faced with multilingual data.
- Performance analysis of models on non-English inputs.

**9. Conclusion**

- Summary of findings.
- Recommendations for future improvements.

**10. References**

- List of resources and libraries used.

---

Feel free to customize the `README.md` and the report outline further to align with your specific implementations and findings. If you need assistance in generating specific sections or visualizations, let me know!
::contentReference[oaicite:0]{index=0}
 


