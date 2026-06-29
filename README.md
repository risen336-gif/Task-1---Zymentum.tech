# Sentiment Analysis on Product Reviews using Machine Learning

## Overview

This project focuses on **Sentiment Analysis of Product Reviews** using **Natural Language Processing (NLP)** and **Machine Learning** techniques. The system analyzes customer product reviews and classifies them into three sentiment categories:

* Positive 😊
* Negative 😡
* Neutral 😐

The main objective of this project is to understand how machine learning models can process textual data, extract meaningful patterns, and perform sentiment classification.

---

## Objective

The goal of this project is to build a machine learning model that can automatically analyze product reviews and predict whether the sentiment expressed in the review is positive, negative, or neutral.

This project helps in learning:

* Natural Language Processing (NLP)
* Text preprocessing techniques
* Feature extraction using TF-IDF
* Classification using Machine Learning
* Model evaluation techniques

---

## Dataset

The dataset used for this project contains product reviews and their corresponding sentiment labels.

### Dataset Columns

* **review** → Customer product review text
* **sentiment** → Sentiment label (Positive / Negative / Neutral)

Example:

| Review                        | Sentiment |
| ----------------------------- | --------- |
| Amazing product, worth buying | Positive  |
| Very poor quality             | Negative  |
| Product is okay               | Neutral   |

---

## Technologies Used

* Python
* Pandas
* NumPy
* NLTK
* Scikit-learn
* Matplotlib
* Seaborn
* Jupyter Notebook / Google Colab

---

## Project Workflow

### 1. Load Dataset

The product review dataset was loaded using Pandas and inspected for missing values and structure.

### 2. Text Cleaning

Text data was cleaned by:

* Converting text to lowercase
* Removing punctuation
* Removing numbers
* Removing URLs
* Removing extra spaces

Example:

Before:
WOW!!! Product is 100% GOOD!!!

After:
wow product is good

---

### 3. Stopword Removal

Common English stopwords such as:

* the
* is
* and
* of

were removed because they add noise and usually do not contribute significantly to sentiment prediction.

Example:

Before:
this product is very good

After:
product good

---

### 4. Feature Extraction using TF-IDF

Machine learning models cannot process raw text directly.

Therefore, **TF-IDF (Term Frequency-Inverse Document Frequency)** was used to convert text reviews into numerical vectors.

TF-IDF helps identify important words by giving higher weights to meaningful terms and lower weights to common words.

---

### 5. Train-Test Split

The dataset was divided into:

* Training Data (80%)
* Testing Data (20%)

Purpose:

* Training set → Used to train the model
* Testing set → Used to evaluate model performance

---

### 6. Model Training

A **Logistic Regression** classifier was used to train the sentiment classification model.

Reasons for choosing Logistic Regression:

* Efficient for text classification
* Fast training
* Good baseline performance
* Works well with sparse TF-IDF features

---

### 7. Model Evaluation

The trained model was evaluated using the following metrics:

#### Accuracy

Measures overall correctness of predictions.

Accuracy = Correct Predictions / Total Predictions

#### Precision

Measures how many predicted sentiments were actually correct.

#### Recall

Measures how many actual sentiments were correctly identified.

#### F1 Score

Harmonic mean of Precision and Recall.

---

### 8. Confusion Matrix

A confusion matrix was generated to analyze prediction performance.

The confusion matrix helps identify:

* Correct predictions
* False positives
* False negatives
* Misclassified classes

This provides deeper insight into model behavior.

---

### 9. Custom Sentiment Prediction

A custom prediction function was implemented.

Users can enter any product review, and the system predicts sentiment instantly.

Example:

Input:
This product is amazing and worth buying

Output:
Positive

Input:
Terrible quality, waste of money

Output:
Negative

---

## Results

The machine learning model successfully classified product reviews into sentiment categories.

### Performance Metrics

* Accuracy: High classification accuracy achieved
* Precision: Good prediction reliability
* Recall: Effective sentiment detection
* F1 Score: Balanced performance across classes

The model showed strong performance for positive and negative reviews and reasonable performance for neutral reviews.

---

## Findings

Key findings from this project:

1. Text preprocessing significantly improved model performance.
2. Removing stopwords reduced noise in the dataset.
3. TF-IDF effectively transformed textual data into meaningful numerical features.
4. Logistic Regression performed well for sentiment classification.
5. Confusion matrix provided clear insights into misclassifications.
6. Neutral sentiment was slightly harder to classify compared to positive and negative sentiments.

---

## Challenges Faced

Some challenges encountered during development:

* Handling noisy text data
* Dealing with punctuation and special characters
* Class imbalance (if dataset contains more positive reviews)
* Correctly identifying neutral sentiment

---

## Future Improvements

Possible enhancements for this project:

* Use larger datasets
* Apply stemming and lemmatization
* Try advanced models:

  * Naive Bayes
  * Support Vector Machine (SVM)
  * LSTM
  * BERT
* Deploy as a web application
* Build a real-time review analyzer

---

## Conclusion

This project successfully demonstrated how **Natural Language Processing** and **Machine Learning** can be used for sentiment analysis on product reviews.

By combining:

* Text preprocessing
* Stopword removal
* TF-IDF vectorization
* Logistic Regression classification

the model was able to predict sentiment effectively.

This project strengthened practical knowledge in:

* NLP
* Feature Engineering
* Machine Learning
* Model Evaluation

---

## Repository Structure

```bash
Sentiment-Analysis-Product-Reviews/
│
├── dataset/
│   └── product_reviews_cleaned.csv
│
├── notebook/
│   └── sentiment_analysis.ipynb
│
├── README.md
│
└── requirements.txt
```

---

## How to Run

1. Clone the repository

```bash
git clone <your-repository-link>
```

2. Install dependencies

```bash
pip install -r requirements.txt
```

3. Run notebook/script

```bash
python sentiment_analysis.py
```

---

## Author

**Risen Stanley Raj**
AI & Machine Learning Student
Machine Learning Internship — Task 5
