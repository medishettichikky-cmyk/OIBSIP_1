# Credit Card Fraud Detection Using Machine Learning

## Project Overview
This project uses machine learning to identify potentially fraudulent credit card transactions from a highly imbalanced dataset. It compares Logistic Regression and Random Forest classifiers and evaluates their ability to detect fraudulent transactions.

## Objective
To build a fraud detection pipeline, handle class imbalance, evaluate model performance using suitable metrics, and explore the challenges of deploying fraud detection at scale.

## Technologies Used
- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Jupyter Notebook

## Dataset
**Dataset:** Credit Card Fraud Detection

**Source:** [Kaggle Credit Card Fraud Detection Dataset](https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud)

The dataset contains 284,807 transactions, including 492 fraudulent transactions.

The target column is `Class`:
- `0` — Legitimate transaction
- `1` — Fraudulent transaction

The dataset includes transaction amounts, elapsed transaction times, and anonymized numerical features (`V1` to `V28`).

## Project Workflow
1. Loaded and inspected the dataset.
2. Checked missing values, duplicate rows, and descriptive statistics.
3. Analyzed the percentage of fraudulent transactions.
4. Visualized transaction amounts for fraud and legitimate transactions.
5. Explored approximate transaction time patterns.
6. Explained why accuracy can be misleading for imbalanced datasets.
7. Split the data into training and testing sets using stratification.
8. Handled class imbalance using `class_weight="balanced"`.
9. Trained Logistic Regression and Random Forest models.
10. Evaluated precision, recall, F1-score, and ROC-AUC.
11. Visualized confusion matrices and ROC curves.
12. Examined Random Forest feature importance and Logistic Regression coefficients.
13. Compared model performance and exported results.
14. Discussed scalability for high-volume transaction processing.

## Models Used

### 1. Logistic Regression
A classification algorithm used as a baseline model to estimate the probability of a transaction being fraudulent.

### 2. Random Forest Classifier
An ensemble learning algorithm that combines multiple decision trees to identify patterns in transaction data.

## Handling Class Imbalance
Fraudulent transactions represent only a small percentage of the dataset. Both models use `class_weight="balanced"` to give greater weight to the minority class during training.

The data is split using stratification to preserve the approximate proportion of fraudulent transactions in the training and testing sets.

## Evaluation Metrics
- **Precision:** Measures how many transactions predicted as fraud are actually fraudulent.
- **Recall:** Measures how many actual fraudulent transactions are detected.
- **F1-score:** Balances precision and recall.
- **ROC-AUC:** Measures how effectively the model ranks fraudulent transactions above legitimate ones.
- **Confusion Matrix:** Shows correct predictions and classification errors.

Accuracy alone is not sufficient because a model can achieve high accuracy while missing most fraudulent transactions.

## Results
The model evaluation results are saved in `output/model_comparison.csv`.

Additional output files include:
- `output/random_forest_feature_importance.csv`
- `output/logistic_regression_coefficients.csv`
- `output/fraud_predictions.csv`

The most suitable model should be selected based on the actual evaluation results, particularly fraud recall, precision, F1-score, ROC-AUC, and the business cost of false positives and false negatives.

## Scalability Considerations
Processing one million transactions per hour requires approximately 278 transactions per second on average.

A production system could use streaming technologies, optimized model inference, monitoring, periodic retraining, and load testing to support high transaction volumes. Actual performance would need to be verified on suitable infrastructure.

## Project Structure

```text
Fraud-Detection/
├── Fraud_Detection.ipynb
├── README.md
├── data/
│   └── creditcard.csv
├── screenshots/
└── output/
    ├── model_comparison.csv
    ├── random_forest_feature_importance.csv
    ├── logistic_regression_coefficients.csv
    └── fraud_predictions.csv
```

## Conclusion
This project demonstrates a machine learning workflow for detecting fraudulent credit card transactions. It covers exploratory data analysis, class imbalance handling, model training, evaluation, feature analysis, and scalability considerations.

The final model should be chosen using measured test results and the acceptable balance between missed fraud and false alarms.

## Limitations
- The dataset contains anonymized features whose original meanings are not provided.
- Class weighting does not guarantee successful fraud detection.
- Transaction time is recorded as elapsed seconds, not a calendar timestamp.
- Results from this dataset may not generalize to other transaction systems.
- Production performance requires separate testing and monitoring.

## References
- [Kaggle Credit Card Fraud Detection Dataset](https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud)
- [Scikit-learn Logistic Regression](https://scikit-learn.org/stable/modules/generated/sklearn.linear_model.LogisticRegression.html)
- [Scikit-learn Random Forest Classifier](https://scikit-learn.org/stable/modules/generated/sklearn.ensemble.RandomForestClassifier.html)
- [Scikit-learn Model Evaluation](https://scikit-learn.org/stable/modules/model_evaluation.html)

## Author
OIBSIP Data Analytics Internship — Task 3