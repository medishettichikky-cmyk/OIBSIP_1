# Task 4: Sentiment Analysis Using Machine Learning

## Project Overview

This project uses Natural Language Processing (NLP) and machine learning to classify customer reviews into three sentiment categories: Positive, Negative, and Neutral.

The project uses the Women's Clothing E-Commerce Reviews dataset from Kaggle. Sentiment labels are created from product ratings, and two machine learning classifiers are trained and evaluated.

## Objectives

- Load and inspect the customer review dataset.
- Analyze the distribution of sentiment classes.
- Clean and preprocess review text.
- Convert text into numerical features using TF-IDF.
- Split the dataset into training and testing sets using an 80:20 ratio.
- Train Naive Bayes and Logistic Regression classifiers.
- Evaluate models using accuracy, precision, recall, F1-score, and confusion matrices.
- Visualize sentiment distribution and generate WordClouds.
- Examine up to five misclassified reviews.
- Compare model performance and discuss real-world applications.

## Dataset

**Source:** Kaggle — Women's Clothing E-Commerce Reviews

**Dataset link:** https://www.kaggle.com/datasets/nicapotato/womens-ecommerce-clothing-reviews

The dataset contains customer reviews and product ratings.

### Sentiment Label Creation

The sentiment categories are derived from product ratings:

- **Negative:** Ratings 1 and 2
- **Neutral:** Rating 3
- **Positive:** Ratings 4 and 5

These labels are rating-based proxies and may not always reflect the exact sentiment expressed in the review text.

## Tools and Technologies

- Python
- Pandas
- NumPy
- Scikit-learn
- Matplotlib
- Seaborn
- WordCloud
- Jupyter Notebook

## Project Workflow

1. Load and inspect the dataset.
2. Check missing values, duplicate records, and rating distribution.
3. Create positive, negative, and neutral sentiment labels.
4. Preprocess text by converting it to lowercase, removing URLs, HTML tags, punctuation, digits, and stopwords, and tokenizing words.
5. Visualize sentiment distribution using a bar chart.
6. Generate WordClouds for each sentiment category.
7. Extract text features using TF-IDF.
8. Split the data into training and testing sets using an 80:20 ratio.
9. Train Multinomial Naive Bayes and Logistic Regression models.
10. Evaluate the models using classification metrics and confusion matrices.
11. Compare model performance.
12. Analyze misclassified reviews.
13. Export evaluation results and predictions.

## TF-IDF Feature Extraction

TF-IDF stands for Term Frequency–Inverse Document Frequency. It converts text into numerical features that machine learning models can process.

It gives importance to words based on their frequency in a review and how common they are across the collection of reviews. The TF-IDF vectorizer is fitted on the training data and then applied to the test data to avoid data leakage.

## Machine Learning Models

### 1. Multinomial Naive Bayes

A probabilistic classification algorithm commonly used for text classification. It predicts sentiment based on the learned relationships between text features and sentiment labels.

### 2. Logistic Regression

A supervised machine learning algorithm used for classification. It learns patterns in TF-IDF features to predict positive, negative, and neutral sentiment.

## Model Evaluation

Both models are evaluated using:

- **Accuracy:** Overall proportion of correct predictions.
- **Precision:** Reliability of positive predictions for each class.
- **Recall:** Proportion of actual examples correctly identified.
- **F1-score:** Balance between precision and recall.
- **Confusion Matrix:** Comparison of actual and predicted sentiment classes.

Macro-averaged precision, recall, and F1-score are used to compare performance across all sentiment classes.

## Visualizations

The project includes:

- Sentiment distribution bar chart.
- WordCloud for negative reviews.
- WordCloud for neutral reviews.
- WordCloud for positive reviews.
- Confusion matrices for both classifiers.
- Model performance comparison chart.

## Error Analysis

Up to five misclassified reviews are examined by comparing their actual sentiment labels with model predictions.

Potential reasons for errors include ambiguous wording, mixed opinions, negation, limited context, and differences between rating-based labels and the sentiment expressed in text.

## Project Structure

```text
Sentiment-Analysis/
├── Sentiment_Analysis.ipynb
├── README.md
├── data/
│   └── sentiment_data.csv
├── screenshots/
└── output/
    ├── model_evaluation_results.csv
    ├── best_model_predictions.csv
    └── sentiment_distribution.csv
```

## Results

The notebook compares Naive Bayes and Logistic Regression using accuracy, macro precision, macro recall, and macro F1-score.

The model with the highest macro F1-score is selected as the best-performing model for this experiment. Actual evaluation values and misclassification examples are available in the notebook and exported output files.

## Real-World Applications

- Analyzing customer feedback on e-commerce platforms.
- Identifying common complaints and satisfaction trends.
- Monitoring customer opinions about products and services.
- Helping businesses understand customer experience.
- Supporting customer feedback analysis and service improvement.

## Limitations and Future Improvements

The sentiment labels are derived from product ratings and may not perfectly represent the meaning of the review text. TF-IDF-based models may also struggle with sarcasm, context, and complex language.

Future improvements could include testing additional classifiers, using lemmatization, tuning model parameters, and evaluating against manually labeled sentiment data.

## Conclusion

This project demonstrates an end-to-end sentiment analysis workflow using text preprocessing, TF-IDF feature extraction, machine learning classification, evaluation metrics, visualizations, and error analysis.

It provides a practical introduction to NLP and shows how customer reviews can be analyzed to understand opinions and support business decisions.

## Author

Pallavi Waghmare

## Internship

Oasis Infobyte (OIBSIP) — Data Analytics Internship
