# House Price Prediction Using Linear Regression

## Project Overview
This project predicts house sale prices using Linear Regression and the House Prices dataset from Kaggle. It covers data cleaning, exploratory data analysis (EDA), feature selection, data preprocessing, model training, and evaluation.

## Objective
To build and evaluate a machine learning model that predicts house prices based on property features such as living area, overall quality, garage capacity, year built, and neighborhood.

## Technologies Used
- Python
- Pandas and NumPy
- Matplotlib and Seaborn
- Scikit-learn
- Jupyter Notebook

## Dataset
**Dataset:** House Prices – Advanced Regression Techniques

**Source:** [Kaggle House Prices Dataset](https://www.kaggle.com/competitions/house-prices-advanced-regression-techniques/data)

The project uses `train.csv`, which contains property information and the target variable `SalePrice`.

## Project Workflow
1. Loaded and explored the dataset.
2. Checked missing values and duplicate records.
3. Performed exploratory data analysis using charts and descriptive statistics.
4. Analyzed correlations between numerical features and sale prices.
5. Selected relevant features for prediction.
6. Split the data into training and testing sets.
7. Handled missing values and encoded categorical variables.
8. Trained a Linear Regression model.
9. Evaluated model performance using RMSE and R².
10. Analyzed actual versus predicted prices and model residuals.
11. Examined model coefficients.
12. Compared Linear Regression with Ridge Regression.
13. Exported evaluation metrics, predictions, and model coefficients to CSV files.

## Model Evaluation
The models are evaluated using:

- **Mean Squared Error (MSE):** Measures the average squared prediction error.
- **Root Mean Squared Error (RMSE):** Measures prediction error in the same units as house prices.
- **R² Score:** Measures how well the model explains variation in house prices.

The final performance values are available in `output/model_evaluation_results.csv`.

## Project Structure
```text
House-Price-Prediction/
├── House_Price_Prediction.ipynb
├── README.md
├── data/
│   └── train.csv
├── screenshots/
└── output/
    ├── model_evaluation_results.csv
    ├── house_price_predictions.csv
    └── linear_regression_coefficients.csv
```

## Results
The notebook generates predictions for the test split and compares Linear Regression with Ridge Regression. The model with the lower RMSE can be considered better on that test split, while R² provides additional information about model fit.

## Conclusion
This project demonstrates an end-to-end machine learning workflow for house price prediction, including data preprocessing, visualization, model training, evaluation, and result export. It also highlights the importance of handling missing data and evaluating prediction errors.

## Limitations
- Model performance depends on the dataset and selected features.
- Linear Regression assumes a linear relationship between the input features and target.
- Predictions may not reflect current real-estate market prices.

## Author
Data Analytics Internship Project – OIBSIP
