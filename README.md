# Email-Spam-Classifier
This project implements an Email Spam Classification system using the Multinomial Naive Bayes (MNB) algorithm, a probabilistic model well-suited for text classification tasks. The goal of the project is to automatically distinguish between spam and legitimate (ham) emails using Natural Language Processing techniques.

The system follows a complete machine learning pipeline, including text preprocessing (cleaning, normalization, stopword removal), tokenization, and feature extraction using Bag of Words / TF-IDF vectorization. The processed data is then used to train a Multinomial Naive Bayes classifier for efficient and reliable spam detection.

Model performance was evaluated using Accuracy and Precision, highlighting the model’s effectiveness in correctly identifying spam emails while minimizing false positives.

🧠 How This Model Works
Building this classifier involved a complete Natural Language Processing (NLP) pipeline. Since computers cannot understand raw text, the project follows these four critical steps:
1. Data Preprocessing
Raw emails are messy. To help the model focus on the most important information, the text undergoes:
 * Tokenization: Breaking sentences into individual words.
 * Lowercasing: Converting everything to lowercase so "SPAM" and "spam" are treated the same.
 * Stopword Removal: Removing common words like "is," "the," and "and" that don't help in identifying spam.
2. Feature Extraction (Vectorization)
This is the most important step. We use a Bag of Words model via CountVectorizer.
 * It creates a table where every column is a unique word from the dataset, and every row is an email.
 * The cells are filled with the frequency of that word in that specific email.
3. The Algorithm: Multinomial Naive Bayes
I chose Multinomial Naive Bayes because it is a classic, high-performance algorithm for text classification. It uses Bayes' Theorem, which calculates the probability of an event based on prior knowledge.
 * Why it's "Naive": It assumes that every word in an email is independent of the others. Even though this isn't true in human language, it works surprisingly well for catching spam keywords!
4. Training and Testing
The dataset was split into two parts:
 * Training Set (80%): Used to "teach" the model the probability of words appearing in spam.
 * Testing Set (20%): Used to evaluate the model on data it has never seen before to ensure it can generalize to new emails.
🛠 Project Workflow
 * Exploratory Data Analysis (EDA): Visualized the distribution of spam vs. ham messages.
 * Model Building: Implemented the Scikit-Learn pipeline.
 * Evaluation: Created a Confusion Matrix to track False Positives and False Negatives.
 * Deployment Prep: Exported the model using pickle for real-time use.
 * 
This project demonstrates:

Practical implementation of an end-to-end ML workflow

Application of NLP techniques for real-world text classification

Understanding of probabilistic learning models

Performance evaluation of classification systems

It serves as a foundational project in machine learning and showcases the application of statistical methods to solve real-world filtering problems.
