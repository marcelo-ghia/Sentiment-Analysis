Sentiment Analysis of Tweets Before and After Russian Invasion of Ukraine

This GitHub repository contains code to analyze the sentiment of tweets before and after the Russian invasion of Ukraine. The goal is to understand the impact of this event on Twitter users and whether following certain Twitter accounts influenced sentiment during this period.

Data

The analysis uses two datasets:

tweets.csv: A dataset of English tweets containing information such as tweet id, author id, creation date, language, text, author username, author description, geo-location, and more.
tweets_v2_30k_followers.csv: A dataset of English tweets from users with at least 30,000 followers, including similar information as the first dataset.

Requirements

To run the code, you need the following Python packages installed:

pandas
glob
json
re
emoji
collections
matplotlib
seaborn
nltk

Setup and Preprocessing

The code performs the following data preprocessing steps:

Loading the tweet datasets and filtering for English tweets only.
Handling retweets by removing tweets from users who follow a specific Twitter account (RT_followers).
Grouping tweets by author id and counting the number of tweets per author to create a histogram.
Sentiment Analysis
Sentiment analysis is performed using the opinion lexicon from the Natural Language Toolkit (nltk). The code counts the positive and negative words in each tweet and calculates a sentiment score. It then aggregates the sentiment scores at the year/month level to analyze trends.

Difference-in-Difference Estimation

The code estimates the causal effect of following a specific Twitter account (Russia Today) on sentiment before and after the Russian invasion of Ukraine using the difference-in-difference method. This involves comparing the sentiment of users who follow Russia Today with those who don't, before and after the invasion.

Results

The results of the sentiment analysis and difference-in-difference estimation are visualized using line plots, allowing you to observe any changes in sentiment over time and assess the impact of following Russia Today on Twitter users.

Files in the Repository

Final_Project_Notebook.ipynb: Jupyter Notebook containing the entire analysis code.
Corpus_data_final.csv: Cleaned dataset used for analysis (English tweets).
Corpus_data_RT_final.csv: Cleaned dataset of tweets from users with at least 30,000 followers.

Instructions

To run the analysis, make sure you have the required Python packages installed and download the dataset files. Then, simply execute the code in the Jupyter Notebook Final_Project_Notebook.ipynb in your local environment.

Feel free to explore the code, modify it, and adapt it for your own analyses. If you find this repository helpful, consider starring it to show your appreciation!

For any questions or feedback, please open an issue in the repository, and I'll be happy to assist you.
