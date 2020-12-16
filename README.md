Aim: To develop a multi-class classifier model to efficiently determine hate speech in social media posts.

On different social media platforms, different posts are misclassified as hate speech just due to the presence of offensive language. Therefore the project aims to reduce the misclassification of hate speech due to the presence of offensive language.

The dataset used for this task is the Davidson hate speech and offensive language dataset. It consists of about 25k tweets collected from different users and the different attributes are:
- count = no. of CrowdFlower users who coded each tweet (min - 3, max up to 9).
- hate_speech = no. of CF users that classified tweets to be hate speech.
- offensive_language = no. of CF users that classified tweets to be offensive.
- neither = no. of CF users that classified tweets to be neither offensive nor non-offensive.
- class = class label for majority of CF users. 0 - hate speech 1 - offensive language 2 - neither

Some preprocessing tasks are performed on the tweets in order to bring them into a standard format. The different data preprocessing steps are as follows:
- Remove Twitter Handles (@...)
- Remove URLs (https...)
- Remove extra spaces
- Lowercase the tweet
- Remove special characters
- Stemming
- Tokenization
- Stopword Removal

In order to better identify hate speech, features are generated for each tweet by creating unigram, bigram, trigram features each weighted by its TF-IDF. Additionally, in order to capture the syntactic structure sequences of unigram, bigram, and trigram POS tags weighted by their TF-IDF are created.

The different classifier models implemented are Support Vector Machine (SVM), L1 Logistic Regression, Random Forest, and Naive Bayes.

The different evaluation metrics used to evaluate the performance of the models are confusion matrix, accuracy, precision score, recall score, f1-score, and ROC-AUC curves.

The results show that the approach used in the project reduces the misclassification of posts as hate speech due to the presence of offensive language.
