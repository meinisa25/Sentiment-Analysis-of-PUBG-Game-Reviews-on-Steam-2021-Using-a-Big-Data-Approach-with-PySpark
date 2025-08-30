# **Sentiment Analysis of PUBG Game Reviews on Steam (2021) Using a Big Data Approach with PySpark**

---

## 📱 **About the Project**

This project focuses on analyzing the sentiment of user reviews of *PlayerUnknown’s Battlegrounds (PUBG)* on the Steam platform in 2021. With the rapid growth of the gaming industry, Steam has become the world’s largest digital game distributor with more than 67 million active monthly players and over 7,600 accessible games.  

User reviews serve as a valuable source of information to understand player perceptions of game quality. Sentiment analysis is used in this project to classify reviews into **positive, negative, and neutral categories**.  

---

## 📋 Dataset

- **Source**: User reviews of PUBG from Steam (2021).  
- **Size**: 1,644,255 rows of review data.
  
---

## 📂 Methodology

### a. Data Collection and Preparation
The dataset of PUBG reviews was downloaded from the Steam platform (2021).  
- **Size**: 40,848,659 rows and 23 columns.  
- **Content**: Includes information such as `app_id`, `app_name`, user reviews (`review`), review creation time, user recommendations (`recommended`), and user profile details.  
- The dataset represents a large volume of user feedback, offering a rich source for sentiment analysis.  

The dataset was then loaded into the **PySpark environment** for efficient large-scale processing. Data exploration was conducted to understand structure, features, and sentiment distribution. Data cleaning was also applied, including duplicate removal, handling missing values, and data validation.

### b. PySpark Implementation
PySpark, part of **Apache Spark**, was used for distributed data processing.  
- Operations for manipulation and aggregation.  
- This allowed scalable analysis while maintaining processing efficiency.  

### c. Text Preprocessing
To prepare raw reviews for sentiment analysis:  
1. Tokenization into individual words.  
2. Conversion to lowercase.  
3. Removal of punctuation and special characters.  
4. Stopword removal to reduce noise.  
5. Lemmatization/stemming for consistent word forms.  

### d. Sentiment Analysis
Sentiment labeling was performed using **VADER (Valence Aware Dictionary and Sentiment Reasoner)**, which assigns sentiment scores and categorizes reviews into:  
- Positive  
- Neutral  
- Negative  

### e. Model Training
- The dataset was split into **training (80%)** and **testing (20%)** sets.  
- **TF-IDF (Term Frequency–Inverse Document Frequency)** was applied to convert text into numerical feature vectors.  
- Two models were trained for sentiment classification:  
  - **Naive Bayes**  
  - **Logistic Regression**  

### f. Model Performance Evaluation
Evaluation was conducted using multiple metrics:  
- Accuracy  
- Precision  
- Recall  
- F1-score  

Additionally:  
- **Confusion matrices** were generated for both training and testing sets.  
- **Cross-validation** was applied to ensure consistent model performance and prevent overfitting.  

### g. Model Comparison
The performances of **Naive Bayes** and **Logistic Regression** were compared using the evaluation metrics.  
- **Result**: Logistic Regression outperformed Naive Bayes, achieving higher accuracy (94% vs 75%) and proving more suitable for sentiment classification in this context.  
- The best-performing model (Logistic Regression) was selected for final sentiment prediction on PUBG reviews.  

---

## 🖥 Tools & Libraries

![Python](https://img.shields.io/badge/-Python-3776AB?style=flat&logo=python&logoColor=white)  
![PySpark](https://img.shields.io/badge/-PySpark-E25A1C?style=flat&logo=apachespark&logoColor=white)  
![VADER](https://img.shields.io/badge/-VADER-4B0082?style=flat&logo=python&logoColor=white)  
![Scikit-learn](https://img.shields.io/badge/-ScikitLearn-F7931E?style=flat&logo=scikit-learn&logoColor=white)  
![Pandas](https://img.shields.io/badge/-Pandas-150458?style=flat&logo=pandas&logoColor=white)  
![Matplotlib](https://img.shields.io/badge/-Matplotlib-11557C?style=flat&logo=python&logoColor=white)  

---

## 📊 Results

- **Logistic Regression**: ~94% accuracy.  
- **Naive Bayes**: ~75% accuracy.
  
✅ Logistic Regression significantly outperformed Naive Bayes in classifying user review sentiments, proving more suitable for this sentiment analysis task.  
