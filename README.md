# Sentiment Analysis of Tweets on Apple and Google

##  Project Overview
This project applies natural language processing (NLP) and machine learning to classify sentiment in tweets directed at Apple and Google products. The purpose is to empower brands with real-time insights into customer perceptions, enabling better product decisions, faster customer service, and more targeted marketing.

> Conducted by **Group 3** .

---

##  Problem Statement
Brands like Apple and Google face an overwhelming volume of customer feedback on platforms like Twitter. Manually tagging and responding to this data is inefficient and often delayed. The core challenge addressed in this project is:

> **Can we accurately classify tweet sentiments as Positive, Negative, Neutral, or No Emotion using machine learning?**

---

##  Objectives
- Automatically classify tweets into sentiment categories.
- Explore the linguistic patterns behind sentiments.
- Compare traditional and deep learning models for sentiment classification.
- Deliver business insights for actionable decision-making.

---

##  Dataset
- 9,000+ tweets related to Apple and Google products.
- Labeled into:
  - Positive emotion
  - Negative emotion
  - No emotion toward brand
  - I can't tell
- Includes metadata like tweet text and associated brand/product.

---

##  Data Cleaning and Preprocessing
The tweets were cleaned and standardized using:

- **Tokenization**: NLTK's `word_tokenize()` for accurate word separation.
- **Stopword Removal**: NLTK's `stopwords` to remove common English words.
- **Lemmatization**: `WordNetLemmatizer()` to reduce words to base form.
- **Regex Cleaning**: Removed URLs, mentions, hashtags, and special characters.

> Result: Cleaned text optimized for machine learning with reduced noise.

---

## 🛠 Feature Engineering
- **TF-IDF Vectorization**: Captures importance of words per document.
- **Bigram Inclusion**: Improves context via 2-word phrases.
- **Label Encoding**: Converted sentiment classes into numeric format (0–3).

---

##  Models Used
- Baseline Logistic Regression
-  Tuned Logistic Regression (L1 regularization)
- Random Forest
- XGBoost
- LSTM (Long Short-Term Memory)

---

##  Model Evaluation
- **Best Model**: Tuned Logistic Regression
- **Accuracy**: 67%
- **F1 Macro Score**: 0.42
- **Cross-validation**: 5-fold stratified K-fold
- **ROC-AUC Score**: 0.87

---

