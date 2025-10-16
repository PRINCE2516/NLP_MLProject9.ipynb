# NLP_MLProject9.ipynb


🎬 Movie Review Sentiment Analysis – Theoretical Explanation
1️⃣ Problem Statement

The goal of this project is to automatically determine the sentiment of a movie review – whether it is positive 👍 or negative 👎.

Sentiment analysis is a key task in Natural Language Processing (NLP).

The challenge is to convert textual data into a form that a computer can understand and analyze.

2️⃣ Dataset Overview

The dataset used is NLTK’s movie_reviews corpus.

It contains 2000 reviews:

1000 positive reviews

1000 negative reviews

Each review is a plain text file.

Positive reviews generally contain words like “amazing”, “outstanding”, while negative reviews have words like “boring”, “terrible”.

3️⃣ Text Preprocessing

Before analyzing text, it must be cleaned and processed:

a) Tokenization ✂️

Breaking text into individual words or tokens.

For example: “I love this movie” → ["I", "love", "this", "movie"].

Tokens are the building blocks for NLP.

b) Stopword Removal ❌

Stopwords are very common words like “the, is, and” that don’t carry sentiment meaning.

Removing stopwords reduces noise and improves classifier performance.

c) Punctuation Removal

Symbols like . , ! ? do not add meaning in sentiment classification.

Removing them simplifies the dataset.

4️⃣ Feature Extraction – Bag-of-Words 👜

Bag-of-Words (BoW) is a method to represent text as numerical features.

Each document (review) is represented as a dictionary of words, where the key is the word and the value indicates presence or frequency.

Example: “I love this movie” → {“love”:1, “movie”:1}.

BoW ignores word order, but captures the important words that indicate sentiment.

5️⃣ Word Frequency Analysis 📊

Counting word occurrences gives insight into which words are most informative.

Words like “film, movie, good, bad” appear frequently.

Rare words often carry strong sentiment, e.g., “outstanding”, “insulting”.

Visualizations like histograms or log-log plots show distribution of word frequencies.

6️⃣ Creating Labeled Features

Each review is converted into a feature dictionary using BoW.

Paired with its label:

Positive review → "pos"

Negative review → "neg"

These labeled features are used to train a classifier.

7️⃣ Model Selection – Naive Bayes Classifier 🎯

Naive Bayes is a probabilistic classifier based on Bayes’ theorem.

Assumes that the presence of each word is independent of others (naive assumption).

Despite its simplicity, Naive Bayes performs very well for text classification, especially with BoW features.

How it works:

Calculate the probability of a review being positive or negative based on the words it contains.

Assign the class with the highest probability.

8️⃣ Training and Testing

Dataset is split into:

Training set: Used to teach the classifier patterns in words → sentiment.

Test set: Used to evaluate how well the classifier generalizes to new, unseen reviews.

Typical results:

Training accuracy: ~98% (classifier learns the training data well)

Test accuracy: ~71% (realistic performance on unseen data)

9️⃣ Most Informative Words 🔍

After training, the classifier identifies words that are strong indicators of sentiment.

Examples:

Positive: “outstanding”, “astounding”, “fascination”

Negative: “insulting”, “ludicrous”, “uninvolving”

These words carry the strongest sentiment signals.

🔟 Key Insights

BoW + Naive Bayes is simple yet effective for sentiment classification.

Stopword removal significantly improves accuracy.

The model captures sentiment using presence of important words, ignoring word order.

Frequent words are not always informative; rare words can carry strong sentiment signals.

Future Enhancements 🚀

Use TF-IDF weighting instead of simple presence to reduce impact of frequent neutral words.

Experiment with bigram or trigram models to capture word sequences.

Apply more advanced models like Logistic Regression, SVM, LSTM, or BERT for improved accuracy.
