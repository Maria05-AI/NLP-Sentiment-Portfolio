# 🇸🇦 Arabic Sentiment Analysis

## Overview
This project serves as an experimental lab. Unlike standard projects that use ready-made datasets, I wanted to experience the challenge of **building an Arabic NLP model from scratch**.
I constructed a balanced dataset of product reviews and built a pipeline to process Arabic text, handling specific challenges like letter normalization.

## How It Works
1.  **Preprocessing:** A custom function normalizes Arabic characters (unifying 'أ/إ/آ' to 'ا', and 'ة' to 'ه').
2.  **Vectorization:** Uses **N-grams (1,2)** to capture context (e.g., understanding "not good" vs "good").
3.  **Model:** Naive Bayes classifier.

## Challenges & Learnings (The "Negation" Issue)
One of the most interesting findings in this experiment was the **"Negation Handling"** challenge.

* **The Scenario:** When testing the sentence *"Customer service is not good"* (خدمة العملاء ليست جيدة).
* **The Result:** The model classified it as **Positive**.
* **Why?** Since the dataset is small (~60 samples), the model weighted the word "Good" (جيدة) heavily as a positive indicator and didn't fully grasp the negating effect of "Not" (ليست) due to the limited examples of negation in the training data.
* **Conclusion:** This highlights the limitation of Bag-of-Words models on small datasets and demonstrates why Large Language Models (LLMs) or Deep Learning are preferred for production environments.

## Demo Output
The model features an interactive terminal loop for live testing also for interactive testing:

![Arabic Output Example](NLP-Sentiment-Portfolio/Arabic-Sentiment-Analysis/output)

## Tech Stack
* Python
* Scikit-Learn (Naive Bayes)
* Pandas & Re (Regex)
