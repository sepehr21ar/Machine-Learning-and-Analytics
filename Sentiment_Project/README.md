
Persian Book Review Sentiment Analysis
(تحلیل احساسات دیدگاه‌های کتاب — پروژه نهایی)

A compact end-to-end notebook that scrapes Persian book reviews from Taaghche, preprocesses Persian text with Hazm, performs EDA, vectorizes text, and trains classical ML models (Logistic Regression & Random Forest) for sentiment classification.

Notebook: Sentiment_Project/final_project.ipynb  
(permalink) https://github.com/sepehr21ar/Machine-Learning-and-Analytics/blob/5b18047d5fa32e7d8bbfb4a060864fd2ff7e3521/Sentiment_Project/final_project.ipynb

---

## Project Overview

This notebook demonstrates a full pipeline for Persian sentiment analysis:
- Web scraping (Selenium) to collect user reviews and star ratings from Taaghche.
- Labeling reviews using rating thresholds (>=4 → positive, <3 → negative; 3-star reviews excluded).
- Persian text normalization, tokenization, lemmatization and stopword removal using Hazm.
- Exploratory Data Analysis (text length stats, class balance, wordclouds and frequent words).
- Feature extraction using CountVectorizer / TfidfVectorizer (1-2 grams).
- Training and evaluating Logistic Regression and Random Forest classifiers with stratified splits and cross-validation.

Key outputs included in the notebook:
- saved raw CSV: data/raw_reviews.csv
- saved cleaned CSV: data/cleaned_reviews.csv
- vectorized matrices and trained models (in-memory in the notebook)

Results summary (from the run in the notebook):
- Logistic Regression — CV f1-score (5-fold avg): ~0.80 (reported), Test accuracy ~0.716
- Random Forest — Test accuracy ~0.706
(See notebook for full classification reports and confusion matrices.)

---

## Files & Paths (used in notebook)

- Notebook: Sentiment_Project/final_project.ipynb
- Raw data (after scraping): C:/Users/Sepehr/SentimentProject/data/raw_reviews.csv
- Cleaned data: C:/Users/Sepehr/SentimentProject/data/cleaned_reviews.csv

If you run locally, update BASE_DIR and paths at the top of the notebook to match your environment.
