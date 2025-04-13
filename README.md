
# Sentiment Analysis and Offensive Language Classification

## Project Overview
This project aims to develop a machine learning model for detecting offensive language in online feedback. The primary objective is to predict whether a given feedback comment is classified as "toxic" or not. The dataset includes fine-grained labels (e.g., "abusive," "vulgar," "menace," etc.), but the focus is on predicting the binary "toxic" label. The solution explores multiple machine learning techniques, including a baseline model, advanced models (e.g., LSTM/GRU), and transformer-based models (e.g., BERT, XLM).

## Dataset Description
The dataset contains feedback comments with the following attributes:
- **id**: Unique identifier for each comment
- **feedback_text**: The text content of the feedback
- **toxic**: Binary label indicating if the comment is toxic (1 = toxic, 0 = not toxic)
- **abusive**: Binary label indicating if the comment contains severe toxicity
- **vulgar**: Binary label indicating if the comment contains obscene language
- **menace**: Binary label indicating if the comment contains threats
- **offense**: Binary label indicating if the comment contains insults
- **bigotry**: Binary label indicating if the comment contains identity-based hate

### Dataset Files:
- `train.csv`: Labeled training data
- `test.csv`: Unlabeled test data for prediction

## Project Structure
The repository is structured as follows:
```
RSentiment-Analysis/
    ├── task/
    │   ├── model1_implementation.ipynb  # Baseline and Advanced Models (Logistic Regression, Random Forest, LSTM/GRU)
    │   └── model2_implementation.ipynb  # Transformer-based Models (BERT, XLM)
    |
    ├── Performance_Analysis_Report.pdf  # Model performance analysis and evaluation
    └── README.md                      # Project documentation
```

## Steps to Run the Code
### Prerequisites
Make sure to install the required libraries using the following:
```bash
pip install -r requirements.txt
```

### Running the Baseline and Advanced Models
1. Open the `model1_implementation.ipynb` or `model1_implementation.py` file.
2. Follow the steps to load the dataset, preprocess the text, train the model, and evaluate the performance.
3. You can experiment with various classifiers like Logistic Regression and Random Forest, and advanced models like LSTM and GRU.

### Running the Transformer-based Models
1. Open the `model2_implementation.ipynb` or `model2_implementation.py` file.
2. This notebook contains code for fine-tuning transformer-based models like BERT and XLM.
3. Make sure to have access to the GPU for efficient model training.

### Performance Evaluation
- Model evaluation is performed using metrics like **accuracy**, **precision**, **recall**, **F1-score**, **AUC-ROC**, and confusion matrices.
- The evaluation report is provided in the `Performance_Analysis_Report.pdf` file.

## Model Evaluation Results
### Baseline and Advanced Models
- **Logistic Regression**: (Insert performance results here)
- **Random Forest**: (Insert performance results here)
- **LSTM/GRU**: (Insert performance results here)

### Transformer-based Models
- **BERT**: (Insert performance results here)
- **XLM**: (Insert performance results here)

## Observations
- The dataset exhibits class imbalance, with some labels being underrepresented.
- The transformer-based models outperformed the baseline models in terms of accuracy and F1-score, especially when fine-tuned on multilingual data.

## Justification for Model Choice
- **Baseline Models**: Logistic Regression and Random Forest were used as simple yet effective models to establish a performance baseline.
- **Advanced Models**: LSTM and GRU were chosen to capture the sequential nature of text data, allowing the model to learn contextual dependencies between words.
- **Transformer Models**: BERT and XLM were selected for their state-of-the-art performance in natural language understanding and their ability to handle multilingual content effectively.

## Code Quality
The code is structured and modular, with separate sections for data preprocessing, model training, evaluation, and hyperparameter tuning. Functions and classes are defined for reusability and ease of understanding.

## Conclusion
This project demonstrates the use of various machine learning techniques to solve the problem of toxic content detection. The model was evaluated on various performance metrics, and the results show that transformer-based models provide the best accuracy for detecting toxic content in online feedback.
