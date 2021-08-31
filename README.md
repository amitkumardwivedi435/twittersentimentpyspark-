# twittersentimentpyspark-
Sentiment analysis on streaming twitter data using Spark Structured Streaming & Python

This project is a good starting point for those who have little or no experience with Apache Spark Streaming. We use Twitter data since Twitter provides an API for developers that is easy to access. We present an end-to-end architecture on how to stream data from Twitter, clean it, and apply a simple sentiment analysis model to detect the polarity and subjectivity of each tweet.


Input data: Live tweets with a keyword
Main model: Data preprocessing and apply sentiment analysis on the tweets
Output: A parquet file with all the tweets and their sentiment analysis scores (polarity and subjectivity)

We use Python version 3.7.6 and Spark version 2.4.7. We should be cautious on the versions that we use because different versions of Spark require a different version of Python.
Main Libraries

tweepy: interact with the Twitter Streaming API and create a live data streaming pipeline with Twitter
pyspark: preprocess the twitter data (Python's Spark library)
textblob: apply sentiment analysis on the twitter text data
Instructions

First, run the Part 1: twitter_connection.py and let it continue running.
Then, run the Part 2: sentiment_analysis.py from a different IDE.
Part 1: Send tweets from the Twitter API 

In this part, we use our developer credentials to authenticate and connect to the Twitter API. We also create a TCP socket between Twitter's API and Spark, which waits for the call of the Spark Structured Streaming and then sends the Twitter data. Here, we use Python's Tweepy library for connecting and getting the tweets from the Twitter API. 
Part 2: Tweet preprocessing and sentiment analysis

In this part, we receive the data from the TCP socket and preprocess it with the pyspark library, which is Python's API for Spark. Then, we apply sentiment analysis using textblob, which is Python's library for processing textual data. After sentiment analysis, we save the tweet and the sentiment analysis scores in a parquet file, which is a data storage format.

