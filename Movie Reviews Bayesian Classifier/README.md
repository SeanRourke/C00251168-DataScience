# Movie Reviews Bayesian Classifier Project

## Dataset

Dataset containing 50,000 movie reviews from IMDb (Internet Movie Database). The dataset contains 25,000 positive reviews and 25,000 negative reviews. Dataset obtained from Kaggle at https://www.kaggle.com/datasets/lakshmi25npathi/imdb-dataset-of-50k-movie-reviews.

Dataset contains the columns:

- review: The review that was written about a movie
- sentiment: Whether the review was positive or negative (values of 'positive' or 'negative')

## Preprocessing

The review column often contained the HTML tag \<br />. This was removed from the datasets to reduce noise as they are irrelevant to the sentiment. 

Row 34813 could not have the HTML tag removed for some unknown reason (an Excel error occurred when attempted), so the row was removed entirely.

## Tools and Tech Used

This project is written in Python in a Jupyter Notebook.
Excel was used for the pre-processing of the dataset.

## Findings

From performing operations on this dataset, I have found that using Naive Bayes Classifiers is quite good at sentiment analysis of movie reviews. This can be seen in the accuracy score of 0.85. Across both positive and negative predictions, the model had a weighted average of 0.85 for precision, recall and f1 score. The precision number was slightly better for positive sentiment at 0.87 compared to the negative sentiment's 0.83, whereas the negative sentiment produced better results for both recall (0.88 - 0.82) and f1 score (0.85 - 0.84). The difference in f1 score informs us that the model is slightly more accurate when identifying negative sentiment.

When running the model using tfidf vectoriser instead of count vectoriser, the accuracy score goes up from 0.85 to 0.86. the other accuracy measurements all saw improvement as well except for the negative sentiment recall score which saw no change.

When cleaning the reviews of non-alphanumeric characters the accuracy scores for the tfidf vectoriser version saw improvement whereas the count vectoriser saw no change.

From these results we can see that the best method to use for sentiment analysis for this dataset is processing the text to remove non-alphanumeric characters and then using a tfidf vectoriser.