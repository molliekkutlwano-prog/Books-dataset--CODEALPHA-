CodeAlpha Data Analytics Internship — End-to-End Portfolio

Author: Kutlwano Mmoloki Gabanthate

Environment: Google Colab (Python, pandas, numpy, requests, BeautifulSoup, matplotlib, seaborn)

Completed Tasks: Task 1 (Web Scraping), Task 2 (Exploratory Data Analysis), and Task 4 (Sentiment Analysis)

Overview

This repository presents a connected, end-to-end data analytics workflow completed for the CodeAlpha Data Analytics Internship. Rather than treating each task as an isolated exercise, Task 1, Task 2, and Task 4 are structured as a cohesive pipeline:

Task 1 (Web Scraping): Collects and structures book catalogue records from books.toscrape.com into a clean CSV dataset.

Task 2 (Exploratory Data Analysis — EDA): Audits data hygiene, tests for outliers via the Interquartile Range (IQR) rule, engineers analytical features, and evaluates price and rating relationships.

Task 4 (Sentiment Analysis): Scores unstructured reader feedback into Positive, Neutral, and Negative categories using negation-aware polarity scoring and exports a visual breakdown.

Why These Three Tasks Were Selected

Task 1 (Web Scraping): Demonstrates data acquisition from live HTML pages, regular expression price parsing, boolean availability flags, and star-rating normalisation rather than relying solely on pre-packaged datasets.

Task 2 (Exploratory Data Analysis): Directly consumes the Task 1 dataset to validate data quality, check statistical spread and outliers, and test hypotheses around pricing and star ratings.

Task 4 (Sentiment Analysis): Complements quantitative tabular analysis with Natural Language Processing (NLP) on qualitative review text, showing how unstructured feedback can be turned into measurable metrics and visual insights.

Repository Structure

CodeAlpha_DataAnalytics/
├── README.md
├── task1_web_scraping.py
├── task2_eda.py
├── task4_sentiment_analysis.py
├── codealpha_full_project_report.pdf
└── outputs/
    ├── task1_books_dataset.csv
    ├── task2_eda_books_enriched.csv
    ├── task4_sentiment_results.csv
    └── task4_sentiment_chart.png


Key Results by Task

1. Task 1: Web Scraping (task1_books_dataset.csv)

Records Scraped: 60 books across 3 catalogue pages (6 columns).

Data Quality: 0 missing values across all columns (page, title, price_gbp, in_stock, availability_raw, rating_stars).

Price & Rating Baseline: Prices range from £12.84 to £57.31, with an average rating of 3.00 stars and 100% in-stock availability (True).

2. Task 2: Exploratory Data Analysis (task2_eda_books_enriched.csv)

Hygiene Audit: Confirmed 0 missing values (0.0%), 0 exact duplicate rows, and 0 duplicate book titles across all 60 rows.

Summary Statistics & IQR Outliers:

price_gbp: Mean £35.00, median £33.48, standard deviation £14.55, min £12.84, max £57.31.

IQR check (Q1 = £22.04, Q3 = £50.14, IQR = £28.10, fences [£-20.11, £92.30]): 0 price outliers detected.

Price Tiers & Correlation:

Budget (<=£25): 21 books (35.0%)

Mid-Range (£25-£45): 18 books (30.0%)

Premium (>£45): 21 books (35.0%)

Correlation (rating_stars vs. price_gbp): r = -0.027 (negligible linear relationship; higher star ratings do not correspond to higher average prices).

3. Task 4: Sentiment Analysis (task4_sentiment_results.csv & task4_sentiment_chart.png)

Reviews Analysed: 12 reader reviews (0 missing values) scored with negation-aware polarity logic.

Average Polarity Score: +0.50

Sentiment Breakdown:

Positive: 6 reviews (50.0%)

Negative: 4 reviews (33.3%)

Neutral: 2 reviews (16.7%)
