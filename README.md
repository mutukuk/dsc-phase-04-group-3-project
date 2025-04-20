# dsc-phase-04-group-3-project

## Sentiment classification of tweets related to Apple and Google products.

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
4. Value Proposition

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

## Installation
1. Clone the repository
https://github.com/mutukuk/dsc-phase-04-group-3-project.git

# Conclusion (insights, business value, future work)

###  Best Performing Model:
Our final recommendation is to use the Logistic Regression model with tuned hyperparameters and TF-IDF features. It balances performance and interpretability and achieved the highest F1-score in our validation.
- **Logistic Regression** with an accuracy of **68.08%**, followed closely by **LSTM** (67.48%).
- Despite similar scores, LSTM shows **higher potential** for improvement with further tuning.

###  Challenges Encountered:
- Severe **class imbalance**, especially for class `0` and `1`.
- Difficulty capturing sarcasm, slang, and short-form social expressions in classical models.
- Traditional models perform well but lack **contextual understanding** of language.

###  Stratified K-Fold Evaluation:
To ensure our model performance wasn't biased by a single train-test split, we applied **Stratified K-Fold Cross-validation** (5-fold) on Logistic Regression:

- **Fold Accuracies**: [0.6698, 0.6878, 0.6889, 0.6867, 0.6702]
- **Average Accuracy**: **0.6807**
  
This confirms model **robustness and consistency** across different splits.

###  Business Value:
Brands can leverage sentiment classification to:
- Monitor customer satisfaction in real-time.
- Understand brand perception across demographics.
- Respond rapidly to negative sentiments before they escalate.
- Tailor marketing campaigns based on real user emotion.

##  Final Conclusion & Business Insights

###  Best Performing Model:

Our final recommendation is to use the **Logistic Regression model with tuned hyperparameters and TF-IDF features**. It consistently offers the best trade-off between **interpretability, performance, and robustness**.

- **Logistic Regression (Tuned)**:  
  Achieved an accuracy of **67.0%** with an improved **F1-Macro Score of 0.42**, highlighting a better **balance across all sentiment classes**.  
  > *This model was tuned after evaluating baseline models and was selected due to its strong balance of simplicity and performance.*

- **LSTM (Untuned)**:  
  Reached a **68.4% validation accuracy**, outperforming the tuned version in generalization.  
  Despite being untuned, it demonstrated strong potential due to its **contextual learning capabilities**, especially with sequential data.

- **LSTM (Tuned)**:  
  Although hyperparameter tuning significantly boosted **training accuracy to 91.8%**, it introduced **severe overfitting** — with validation loss increasing and performance dropping after Epoch 3.  
  > *We opted for the untuned LSTM in our reporting due to better real-world generalization.*

- **XGBoost**:  
  Delivered strong baseline results and matched Logistic Regression in overall accuracy (≈66%).  
  However, it slightly lagged behind in class-wise performance, especially on the underrepresented classes.  
  > *XGBoost's strength lies in its handling of structured data, but it showed less interpretability and marginal improvements over simpler models.*

- **Random Forest**:  
  Demonstrated decent accuracy and class handling but was **slightly behind** Logistic Regression and LSTM in both **class balance** and **generalization**.

---

###  Additional Observations

- **Feature Importance**:  
  TF-IDF analysis revealed insightful keywords tied to each sentiment.  
  Negative sentiments were often linked with words like *“nut,” “fight,” “care”*, while positive sentiments clustered around *“love,” “awesome,” “cool.”*

- **Class Imbalance**:  
  A significant skew in class distribution — particularly the **underrepresentation of negative sentiment** — posed a challenge.  
  Future iterations can explore **oversampling, class weighting, or focal loss** to address this.

- **Model Validation**:  
  We used **Stratified K-Fold cross-validation** to validate models like Logistic Regression. This helped confirm the model's **robustness and generalizability** across different subsets of data.

  ###  Footnote on Metrics:
> We chose to report the **F1-Macro Score** especially for the tuned Logistic Regression model, as it gives a better view of **how well the model performs across all classes** — not just the dominant ones.  
> This decision was driven by the **noticeable class imbalance** in our dataset.  
> F1-Macro is also a useful secondary metric alongside accuracy, especially in imbalanced classification tasks.

---

###  Business Implications

- **Real-time Sentiment Monitoring**:  
  This model can be deployed to monitor customer sentiment in real time, enabling **faster feedback loops** and **better customer experience** management.

- **Targeted Marketing**:  
  By analyzing sentiment trends and influential words, businesses can **personalize campaigns**, adjust messaging, and improve engagement.

- **Brand Reputation Management**:  
  Early identification of **negative sentiment** clusters allows brands to **act proactively**, safeguarding their reputation and public image.



