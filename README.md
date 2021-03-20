# TSLA-Forecasting

**This project is still under construction**

## Table of Contents

- [Overview](#overview)
- [Data Collection](#data-collection)
- [Sentiment Analysis](#sentiment-analysis)
- [Forecasting](#forecasting)

## Overview

This repository contains the jupyter notebooks for using investor sentiment data from a popular community on Reddit, r/wallstreetbets, to predict the price of TSLA.

The analysis is separated into three categories:

1. Data Collection - scraping user comments from Reddit using PRAW and collecting TSLA's daily closing prices from yahoo finance.

2. Sentiment Analysis - engineering scores from user comments to measure investor sentiment.

3. Forecasting - predicting the future price of TSLA using technical indicators and features from sentiment analysis.

## Data Collection

**Reddit**

We will be working with the `scraping_reddit_comments.ipynb` notebook to scrape user comments from r/wallstreetbets. You will need to install python's Reddit API wrapper, `PRAW`.

```console
pip install praw .
```

You will also need to register an account in order to access the API. You can do that [here](https://www.reddit.com/prefs/apps/).

To learn more about the PRAW API wrapper, please refer to the [official documentation](https://praw.readthedocs.io/en/latest/).

**Yahoo Finance**

We will be collecting historical data on TSLA's daily closing prices using `query_tsla_data.ipynb`. You will need to install `yfinance`.

```console
pip install yfinance .
```

To learn more about the yfinance library, please refer to the [official documentation](https://pypi.org/project/yfinance/).

```console
pip install .
```

## Sentiment Analysis

Insert `description` here.

## Forecasting

Use the following models:
- ARIMA (baseline)
- Random Forest
- XGBoost
- LSTM






