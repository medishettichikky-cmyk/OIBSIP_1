# Wine Quality Prediction Using Machine Learning

## Project Overview
This project uses machine learning classification algorithms to predict wine quality based on physicochemical properties such as acidity, alcohol content, density, sulphates, and pH.

The project compares three classification models: Random Forest, Stochastic Gradient Descent (SGD), and Support Vector Classifier (SVC).

## Objective
To analyze wine characteristics, understand the distribution of quality ratings, build classification models, and compare their performance using appropriate evaluation metrics.

## Technologies Used
- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Jupyter Notebook

## Dataset
**Dataset:** UCI Wine Quality — Red Wine

**Source:** [UCI Machine Learning Repository](https://archive.ics.uci.edu/dataset/186/wine+quality)

The project uses `winequality-red.csv`, containing physicochemical measurements and the original wine quality score.

## Project Workflow
1. Loaded and inspected the dataset.
2. Checked missing values, duplicates, data types, and summary statistics.
3. Analyzed the distribution of the original wine quality scores.
4. Visualized chemical feature distributions.
5. Created a correlation heatmap.
6. Grouped quality scores into Low, Medium, and High categories.
7. Examined class imbalance.
8. Split the dataset into training and testing sets using stratification.
9. Trained Random Forest, SGD, and SVC classifiers.
10. Evaluated models using accuracy, precision, recall, F1-score, classification reports, and confusion matrices.
11. Visualized Random Forest feature importance.
12. Compared model performance.
13. Exported predictions, evaluation metrics, and feature importance to CSV files.

## Quality Categories
The original numerical quality scores are grouped as follows:

- **Low:** Quality score 5 or below
- **Medium:** Quality score 6
- **High:** Quality score 7 or above

This grouping simplifies the classification task. However, the categories may still be imbalanced.

## Models Used

### 1. Random Forest Classifier
Uses multiple decision trees to identify patterns in wine characteristics and predict quality categories.

### 2. SGD Classifier
Uses stochastic gradient-based optimization to learn a classification model.

### 3. Support Vector Classifier (SVC)
Uses support vector machines to find decision boundaries between the quality categories.

## Evaluation Metrics
The models are evaluated using:

- **Accuracy:** Proportion of correctly classified samples.
- **Precision:** Proportion of predicted class labels that are correct.
- **Recall:** Proportion of actual class samples correctly identified.
- **F1-score:** Balance between precision and recall.
- **Confusion Matrix:** Displays correct predictions and misclassifications.

Macro F1-score is used to compare performance across classes, particularly when class distribution is imbalanced.

## Results
The model comparison results are saved in `output/model_comparison.csv`.

Random Forest feature importance is saved in `output/random_forest_feature_importance.csv`, and test-set predictions are saved in `output/wine_quality_predictions.csv`.

The most suitable model should be selected after reviewing the actual evaluation results, with attention to macro F1-score and recall for each class.

## Project Structure

```text
Wine-Quality-Prediction/
├── Wine_Quality_Prediction.ipynb
├── README.md
├── data/
│   └── winequality-red.csv
├── screenshots/
└── output/
    ├── model_comparison.csv
    ├── random_forest_feature_importance.csv
    └── wine_quality_predictions.csv
```

## Conclusion
This project demonstrates a complete classification workflow, from data exploration and feature engineering to model training, evaluation, and comparison.

It also highlights the importance of class imbalance, stratified splitting, appropriate evaluation metrics, and careful model selection.

## Limitations
- Grouping numerical quality scores simplifies the original rating system.
- Class imbalance may affect the classification performance.
- Feature importance does not establish causation.
- Results on this dataset may not generalize to all wines.

## References
- [UCI Wine Quality Dataset](https://archive.ics.uci.edu/dataset/186/wine+quality)
- [Scikit-learn Random Forest Classifier](https://scikit-learn.org/stable/modules/generated/sklearn.ensemble.RandomForestClassifier.html)
- [Scikit-learn SGD Classifier](https://scikit-learn.org/stable/modules/generated/sklearn.linear_model.SGDClassifier.html)
- [Scikit-learn SVC](https://scikit-learn.org/stable/modules/generated/sklearn.svm.SVC.html)

## Author
OIBSIP Data Analytics Internship — Task 2