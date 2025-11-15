## 📝 Twitter NLP Text Preprocessing
📌 Project Overview

This project collects tweets from the Twitter (X) API using Tweepy, stores them in a structured dataset, and performs essential Natural Language Processing (NLP) text preprocessing operations.
The main purpose is to prepare raw Twitter data so it can be used for:

Sentiment analysis

Machine learning models

Text classification

Topic modeling

Further NLP pipelines

The notebook handles everything from fetching tweets → cleaning text → and organizing data for advanced analysis.

## 🚀 Features

Connect to Twitter API using OAuth

Fetch tweets programmatically from user accounts or keywords

Store tweets in Pandas DataFrame

Apply text preprocessing:

Lowercasing

Tokenization

Removing URLs, mentions, punctuation

Removing special characters

Clean, normalized dataset ready for machine learning

Use NLTK tools for NLP-specific operations

## 📦 Libraries Used (Explained Clearly)

Below is a detailed description of each library used in this project and why it is important:

### 1. tweepy

Purpose: Connect to the Twitter API and fetch tweets.

Why used?

Simple authentication using API keys

Provides functions like api.user_timeline()

Makes it easy to extract tweets programmatically

import tweepy

## 2. pandas

Purpose: Work with datasets in table format.

Why used?

Store tweets in a DataFrame

Organize tweet text, date, username, etc.

Export cleaned data to CSV

import pandas as pd

### 3. nltk

Purpose: Natural Language Processing tools.

Why used?

Tokenization (word_tokenize)

Text cleaning

Removing punctuation / splitting words

You also download punkt, a tokenizer model:

nltk.download('punkt')

### 4. time

Purpose: Manage delays between API calls.

Why used?

Twitter rate limits API requests

Using time.sleep() prevents hitting rate-limit errors

import time

### 5. os

Purpose: Access environment variables.

Why used?

Store Twitter API keys safely

Load keys using os.environ.get()

import os

🔑 Twitter API Usage

Your notebook uses the Twitter API (v1.1 or v2) via Tweepy.
It requires the following credentials:

API Key

API Secret

Access Token

Access Token Secret

Authentication example:

auth = tweepy.OAuthHandler(api_key, api_secret)
auth.set_access_token(access_token, access_token_secret)
api = tweepy.API(auth)


Once authenticated, tweets can be collected using Tweepy functions.

🧹 Text Preprocessing Steps

The notebook performs several essential NLP preprocessing steps:

Convert text to lowercase

Remove URLs, mentions (@user), hashtags

Remove punctuation and special characters

Tokenize using NLTK

Remove extra spaces

Clean tweet text for ML modeling
