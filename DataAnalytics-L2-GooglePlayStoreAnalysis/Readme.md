# Google Play Store Analysis and Sentiment Analysis

## Project Overview

This project analyzes the Google Play Store ecosystem using Python. It explores app categories, ratings, installs, size, pricing, estimated revenue, and user review sentiment to identify useful insights for app developers.

This project was completed as part of the **Oasis Infobyte (OIBSIP) Data Analytics Internship — Task 4**.

## Objectives

- Clean and prepare real-world Google Play Store datasets.
- Analyze app distribution and category competition.
- Explore app ratings and average ratings by category.
- Investigate the relationship between app size and installs.
- Compare free and paid applications.
- Estimate potential gross revenue for paid apps.
- Perform sentiment analysis on user reviews.
- Compare sentiment across app categories.
- Build an interactive visualization.
- Generate data-driven insights for app developers.

## Technologies Used

- Python
- pandas
- NumPy
- Matplotlib
- Seaborn
- TextBlob
- Plotly
- Jupyter Notebook

## Datasets

The datasets were obtained from the Kaggle **Google Play Store Apps** dataset.

Dataset link: https://www.kaggle.com/datasets/lava18/google-play-store-apps

Two CSV files are used:

**1. `googleplaystore.csv`**

Contains app information such as:
- App name
- Category
- Rating
- Size
- Number of installs
- Type (free or paid)
- Price
- Reviews and other app attributes

**2. `googleplaystore_user_reviews.csv`**

Contains user review information such as:
- App name
- Translated review text
- Sentiment
- Sentiment polarity
- Sentiment subjectivity

The original datasets are kept separately in the `data` folder.

## Project Workflow

### 1. Data Loading and Inspection
- Loaded the apps and user reviews datasets separately.
- Inspected rows, columns, data types, missing values, and duplicates.

### 2. Data Cleaning
- Removed duplicate records.
- Handled missing app names and review text.
- Converted installs and prices into numeric formats.
- Converted app sizes into megabytes.
- Validated rating values between 1 and 5.
- Prepared clean datasets for analysis.

### 3. Category Analysis
- Analyzed the number of apps in each category.
- Identified categories with the largest number of listed apps.
- Explored potential competition between categories.

### 4. Ratings Analysis
- Visualized the distribution of app ratings.
- Calculated average ratings by category.
- Compared categories with relatively high and low average ratings.

### 5. App Size and Installs
- Created a scatter plot of app size against installs.
- Calculated Pearson correlation to investigate their linear relationship.

### 6. Pricing Analysis
- Compared free and paid applications.
- Visualized paid app prices.
- Estimated potential gross revenue by category using listed prices and reported installs.

### 7. Sentiment Analysis
- Used TextBlob to calculate review sentiment polarity.
- Classified reviews as positive, negative, or neutral.
- Compared average sentiment and negative-review percentages across app categories.

### 8. Interactive Visualization
- Created an interactive Plotly scatter plot comparing category app counts, average ratings, and review sentiment.
- Saved the visualization as an HTML file.

### 9. Key Insights
- Examined category competition.
- Compared category ratings.
- Investigated negative user sentiment to identify potential user-experience improvement opportunities.

## Visualizations

The project includes:
- App distribution by category
- Top app categories
- Rating distribution
- Average rating by category
- App size versus installs
- Free versus paid app comparison
- Paid app price distribution
- Estimated revenue by category
- Overall review sentiment
- Sentiment by category
- Interactive Plotly category dashboard

## Output Files

The notebook exports the following analysis results into the `output` folder:

- `cleaned_googleplaystore.csv`
- `reviews_with_sentiment.csv`
- `category_distribution.csv`
- `category_ratings.csv`
- `free_vs_paid.csv`
- `estimated_revenue_by_category.csv`
- `sentiment_by_category.csv`
- `category_dashboard_data.csv`
- `interactive_category_dashboard.html`

## Key Business Applications

The analysis can help app developers:
- Understand which categories have more competing applications.
- Compare average ratings across categories.
- Explore how app size relates to reported installs.
- Understand the prevalence of free and paid apps.
- Identify categories where user reviews indicate possible improvement opportunities.
- Develop hypotheses for market research and product planning.

## Limitations

- The datasets represent a historical snapshot and may not reflect the current Google Play Store.
- Missing values may affect some category comparisons.
- TextBlob provides approximate sentiment classifications and may misinterpret sarcasm or context.
- The size-versus-installs correlation does not establish causation.
- Estimated revenue is illustrative, not actual revenue. It assumes listed price multiplied by reported installs and does not account for refunds, promotions, repeat installs, or platform fees.
- Category-level conclusions should be considered alongside review counts and additional market research.

## Project Structure

```text
Google-Play-Store-Analysis/
│
├── data/
│   ├── googleplaystore.csv
│   └── googleplaystore_user_reviews.csv
│
├── Google_Play_Store_Analysis.ipynb
├── README.md
│
├── screenshots/
│   ├── 01_Dataset_Overview.png
│   ├── 02_Data_Cleaning.png
│   ├── 03_Category_Distribution.png
│   ├── 04_Top_Categories.png
│   ├── 05_Rating_Distribution.png
│   ├── 06_Average_Rating_By_Category.png
│   ├── 07_Size_vs_Installs.png
│   ├── 08_Free_vs_Paid.png
│   ├── 09_Paid_Price_Distribution.png
│   ├── 10_Estimated_Revenue.png
│   ├── 11_Overall_Sentiment.png
│   ├── 12_Sentiment_By_Category.png
│   ├── 13_Interactive_Dashboard.png
│   ├── 14_Key_Insights.png
│   └── 15_Exported_Results.png
│
└── output/
    ├── cleaned_googleplaystore.csv
    ├── reviews_with_sentiment.csv
    ├── category_distribution.csv
    ├── category_ratings.csv
    ├── free_vs_paid.csv
    ├── estimated_revenue_by_category.csv
    ├── sentiment_by_category.csv
    ├── category_dashboard_data.csv
    └── interactive_category_dashboard.html
```

*Note: The screenshots and output files listed above should be present only after you create them by running the notebook.*

## Conclusion

This project demonstrates an end-to-end exploratory data analysis workflow using Python. By combining app-level analysis with review sentiment, the project provides insights into category competition, ratings, pricing patterns, and user opinions.

The findings can support initial product research, while further customer research and verified business data are needed before making launch or revenue decisions.

## Author

OIBSIP Data Analytics Internship  
Task 4 — Google Play Store Analysis and Sentiment Analysis