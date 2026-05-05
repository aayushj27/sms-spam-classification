# sms-spam-classification
SMS Spam Detection and Classification A Python-based NLP project designed to classify SMS messages as 'Spam' or 'Ham' (legitimate). Features comprehensive data preprocessing, handling of imbalanced datasets through oversampling, and implementation of Multinomial Naive Bayes and Decision Tree models.

This repository contains an end-to-end Machine Learning project to identify spam SMS messages. The project utilizes the SMSSpamCollection dataset, which consists of over 5,500 labeled messages.

🚀 Project Overview
Spam detection is a classic NLP task where we aim to distinguish between unsolicited messages and legitimate user communications. This project implements a robust pipeline that includes data visualization, text cleaning, feature engineering, and model evaluation.

🛠️ Tech Stack
Core: Python, NumPy, Pandas  
NLP: NLTK (Stopwords, WordNetLemmatizer), Scikit-Learn (TfidfVectorizer)  
Visualization: Matplotlib, Seaborn  
Models: Multinomial Naive Bayes, Decision Tree Classifier

📋 Key Features
Dataset Balancing: Addressed data imbalance (initially ~4,825 Ham vs. ~747 Spam) by performing manual oversampling to create a balanced training set.  
Feature Engineering:
word_count: Analyzing message length distributions.  
contains_currency_symbols: Identifying symbols like £, $, or ₹ commonly found in spam.  
contains_number: Checking for phone numbers or prize amounts.  
Text Preprocessing: Automated removal of non-alphabetic characters, lowercasing, stopword removal, and lemmatization.  
Vectorization: Utilized TF-IDF (Term Frequency-Inverse Document Frequency) to transform text into numerical vectors.

📊 Performance
The models are evaluated using:
Confusion Matrices: To visualize True Positives and False Positives.  
Classification Reports: Metrics for Precision, Recall, and F1-score.  
Cross-Validation: 10-fold cross-validation to ensure model stability.

💻 Usage
To run the classification:
Ensure SMSSpamCollection is in the root directory.  
Run the preprocessing and training cells in the provided notebook.  
Use the predict_spam() function to test custom messages:
Python
sample = "URGENT! You have won a 1 week FREE membership..."
if predict_spam(sample):
    print('Spam')
else:
    print('Ham')
