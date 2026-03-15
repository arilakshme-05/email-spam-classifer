#Email Spam Classifier
A machine learning application built in Python that automatically detects whether an incoming message is Spam or Ham (legitimate). This project uses Natural Language Processing (NLP) techniques to transform text into numerical data and classifies it using the Naive Bayes algorithm.

#Features
Text Vectorization: Uses TfidfVectorizer to convert raw text into a matrix of TF-IDF features.
Automatic Stop-Word Removal: Filters out common English words (like "the", "a", "is") that don't add predictive value.
Binary Classification: Categorizes messages into two classes: 0 (Ham) and 1 (Spam).
Performance Metrics: Provides Accuracy Score and a detailed Classification Report (Precision, Recall, F1-Score).

#Technologies Used
Python 3
Pandas: For data manipulation and analysis.
Scikit-Learn: For machine learning modeling and evaluation.
Google Colab: As the development environment.

#Dataset Structure
The model expects a CSV or TSV file with the following structure:
label: The category of the message (ham or spam).
message: The actual text content of the email or SMS.

#How It Works
Data Loading: The dataset is loaded into a Pandas DataFrame.
Label Encoding: Categorical labels (ham, spam) are mapped to numerical values (0, 1).
Data Splitting: The data is split into Training (80%) and Testing (20%) sets to ensure the model generalizes well.
Feature Extraction: TfidfVectorizer calculates the importance of words across the dataset.
Training: The MultinomialNB (Naive Bayes) classifier learns the probability of specific words appearing in spam vs. ham messages.
Evaluation: The model is tested against unseen data to measure its reliability.

#Results
The classifier currently outputs:
Accuracy Score: The percentage of correct predictions.
Precision/Recall: Detailed breakdown of how well the model identifies each specific class.
