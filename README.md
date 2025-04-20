# dsc-phase-04-group-3-project

## Project Summary

This project focuses on **sentiment classification of tweets** related to Apple and Google products using supervised machine learning. The dataset includes over **9,000 labeled tweets** across three sentiment classes: **positive, negative, and neutral**. The goal was to build an effective model to predict sentiment from tweet text — a tool that can support **brand monitoring, customer engagement, and reputation management**.

### Data Understanding  
Initial exploration revealed a **class imbalance**, with **negative tweets dominating** the dataset. This skew called for special handling, such as **class weighting** and careful evaluation metrics beyond simple accuracy.

### Data Preparation  
Preprocessing steps included removing URLs, mentions, stopwords, and lowercasing text. We used **regular expressions and NLTK** for cleaning, and **CountVectorizer** and **TF-IDF** for feature extraction. **TF-IDF** was particularly effective in capturing key sentiment-indicating terms.

### Modeling  
We experimented with several models: **Logistic Regression (baseline and tuned)**, **Random Forest**, **XGBoost**, and **LSTM**. The **tuned Logistic Regression model**, combined with **TF-IDF features** and validated using **Stratified K-Fold cross-validation**, achieved a strong balance between **interpretability, accuracy, and robustness**.

The **LSTM model** demonstrated potential due to its ability to understand sequential data, but the tuned version suffered from **overfitting**, performing worse on validation despite high training accuracy.

### Evaluation & Recommendations  
The **tuned Logistic Regression model** emerged as the best overall performer, achieving **67.0% accuracy** and a more balanced **F1-Macro Score of 0.42**. While deep learning models like LSTM reached higher training performance, they lacked generalization

## Problem statement
- Companies want to understand how customers feel about their products and services on social media. This project uses tweets to classify the sentiment expressed towards different companies or products

## Objectives
1. Classify tweets based on sentiment (positive, negative, neutral)
2. Understand key drivers of sentiment.
3. Provide insights to help companies improve products/services or public perception.

4. ### Value Proposition

Track user emotions at scale across different products.

Enable faster decision-making based on customer feedback.

Reduce reliance on manual sentiment tagging.

## Research Questions
1. Which words or phrases are most commonly associated with positive or negative sentiments?
2. What is the distribution of sentiments across different companies/products?
3. How accurately can we classify tweet sentiments using traditional ML and deep learning models?
  1.  Improve product features,

  2.   Respond to user frustrations more quickly,

  3.  Guide marketing strategies.


