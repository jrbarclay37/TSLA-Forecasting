# TSLA-Forecasting

## Table of Contents

- [Overview](#overview)
- [Data Collection](#data-collection)
- [Sentiment Analysis](#sentiment-analysis)
- [Forecasting](#forecasting)

## Overview

This repository contains the jupyter notebooks for using sentiment data from the most eccentric investing community on Reddit, [r/wallstreetbets](https://www.reddit.com/r/wallstreetbets/), to predict the price of TSLA.

The analysis is separated into three categories:

1. Data Collection - scraping user comments from Reddit using PRAW and collecting TSLA's daily closing prices from yahoo finance.

2. Sentiment Analysis - engineering scores from user comments to measure investor sentiment.

3. Forecasting - predicting the future price of TSLA using technical indicators and features from sentiment analysis.

## Data Collection

**Reddit**

We will be working with the `scraping_reddit_comments.ipynb` notebook to scrape user comments from r/wallstreetbets. You will need to install python's Reddit API wrapper, `PRAW`.

```console
pip install praw
```

You will also need to [register](https://www.reddit.com/prefs/apps/) an account in order to access the API.

To learn more about the `PRAW` API wrapper, please refer to the [official documentation](https://praw.readthedocs.io/en/latest/).

To mitigate Reddit's slow response times, we also leverage `pushshift.io`. This is a project that warehouses all of Reddit's data, allowing us to query the data more efficiently with significantly faster response times.

To learn more about `pushshift.io`, please refer to the [official documentation](https://pushshift.io/api-parameters/).

**Yahoo Finance**

We will be collecting historical data on TSLA's daily closing prices using `query_tsla_data.ipynb`. You will need to install `yfinance`.

```console
pip install yfinance
```

To learn more about the `yfinance` library, please refer to the [official documentation](https://pypi.org/project/yfinance/).

Additionally, we will use the `TA-Lib` to compute our technical indicators to be used as features in our model. 

```console
pip install TA-Lib
```

To learn more about the `TA-Lib` library, please refer to the [official documentation](https://mrjbq7.github.io/ta-lib/doc_index.html).

## Sentiment Analysis

In this section, we will be analyzing our user comments from Reddit and using NLP techniques to engineer scores that measure investor sentiment towards TSLA. This all takes place in the `sentiment_analysis.ipynb` notebook.

## Forecasting

Bringing everything together, we use our sentiment scores and technical indicators to predict the future price of TSLA in the `tsla_forecasting.ipynb` notebook. We use a simple ARIMA model as our baseline and then attempt to improve performance using the following models:
- Random Forest
- XGBoost
- LSTM
