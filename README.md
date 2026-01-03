# Spam-Email-Detection-ML
Project aimed to address the issue of spam emails using Machine Learning based spam email detection system.The system processes raw email text, converts it into numerical form, and applies a trained model to classify incoming emails.

Email spam has become a significant problem in digital communication, leading to wasted time, security risks, and reduced productivity. Spam emails often contain unwanted advertisements, phishing links, or malicious content. Manually filtering such emails is inefficient and impractical, especially with the growing volume of emails exchanged daily. This project aims to address this issue by developing an automated email spam detection system using Machine Learning.

Methodology

1.Dataset Loading and Preprocessing
The dataset consists of labeled emails categorized as spam or ham. Labels are converted into numerical values for machine learning compatibility. Only relevant columns (email text and labels) are retained.

2.Text Cleaning
Email text is cleaned by:

Converting text to lowercase
Removing special characters and numbers
Eliminating extra spaces
This step improves model accuracy by reducing noise and standardizing input data.

3. Feature Extraction using TF-IDF
Since machine learning models cannot process raw text, the cleaned emails are transformed into numerical vectors using the TF-IDF (Term Frequency–Inverse Document Frequency) technique. TF-IDF assigns higher importance to meaningful and less frequent words, improving spam detection performance.

4. Model Training
The transformed data is used to train a Multinomial Naive Bayes classifier, which is well-suited for text classification problems due to its probabilistic nature and efficiency.

5.Pipeline Integration
A Scikit-learn Pipeline is used to combine text cleaning, vectorization, and model training into a single workflow. This ensures consistency, prevents data leakage, and simplifies deployment.

6.Model Evaluation
The trained model is evaluated using:

Accuracy score
Confusion matrix
Precision, recall, and F1-score
These metrics help assess the effectiveness of the spam detection system.

7.Model Export and Deployment Readiness
The complete pipeline is serialized using pickle, allowing the trained model to be reused for real-time spam classification without retraining.
