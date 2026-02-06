# 🇺🇸 English Sentiment Analysis

## Overview
Building upon the insights from the Arabic experiment, this project represents the **Production-Grade** approach. Here, I utilized the famous **IMDB Dataset** (containing 50,000 movie reviews) to train a robust Logistic Regression model.

## Key Differences (Small vs. Big Data)
Unlike the manual Arabic dataset, using 50k samples allowed the model to:
1.  **Generalize Better:** It accurately classifies words it hasn't explicitly memorized by understanding context.
2.  **Handle Nuances:** It successfully distinguishes between sarcasm and genuine praise in many cases.
3.  **High Accuracy:** Achieved **~87% accuracy** on the test set.

## Demo Output
like the previous one i made a live testing and interactive testing:

![English Output Example](./english_output.png)

## Tech Stack
* **Algorithm:** Logistic Regression (Industry standard for baseline benchmarks).
* **Vectorization:** TF-IDF (Term Frequency-Inverse Document Frequency).
* **Dataset:** IMDB Movie Reviews (50k).
