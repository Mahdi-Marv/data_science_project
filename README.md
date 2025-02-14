# README for Financial Analysis Project

## Overview
This project investigates the relationship between stock market performance and social media activity, focusing specifically on tweets related to various companies. The project is divided into three parts, each represented by a separate Jupyter notebook. The overall goal is to analyze how social media activity (tweets) correlates with stock market trends and to explore possible insights that could assist in decision-making processes for investors.

## Authors
- **Name:** Mahdi Hajialilue

## Project Structure
The project is divided into the following notebooks:

- **part1.ipynb**: This notebook begins the project with data importation, preliminary analysis, and basic statistics about the datasets.
- **part2Final.ipynb**: This phase builds on the first part with deeper analysis, including sentiment analysis of tweets and potential correlations with stock performance.
- **part3.ipynb**: This final part concludes the analysis with final insights, summarizing the results, and offering recommendations based on the findings from previous parts.

## Libraries Used
The following libraries are essential for data processing, analysis, and visualization:

- `pandas`: A fast, powerful, flexible, and easy-to-use data manipulation library.
- `seaborn`: A Python visualization library based on matplotlib for making statistical graphics.
- `matplotlib`: A comprehensive library for creating static, animated, and interactive visualizations in Python.
- `numpy`: A fundamental package for numerical computing in Python.

## Datasets
The project utilizes several datasets to facilitate the analysis:

1. **entities.csv**: Contains information about entities (such as cashtags) mentioned in tweets.
2. **tweets.csv**: Contains data on the actual tweets, including tweet IDs, user IDs, timestamps, and tweet content.
3. **companies.csv**: Contains a list of companies and their respective stock ticker symbols.
4. **users.csv**: (Commented out in part1.ipynb) Contains information about users who tweeted, such as their user ID, username, and number of followers.

### Dataset Structure
- **entities.csv**:
  - `text`: The content of the tweet containing cashtags (e.g., "$AAPL").
  
- **tweets.csv**:
  - `tweet_id`: Unique identifier for each tweet.
  - `user_id`: Unique identifier for the user who tweeted.
  - `created_at`: Timestamp indicating when the tweet was posted.
  - `text`: The content of the tweet.

- **companies.csv**:
  - `ticker`: Stock ticker symbol for the company.
  - `name`: Name of the company.
  - `tweet_count`: The number of tweets mentioning the company's ticker symbol, calculated during the analysis.

- **users.csv**:
  - `user_id`: Unique identifier for each user.
  - `username`: The username of the individual who posted the tweet.
  - `followers_count`: The number of followers the user has.

## Analysis Overview

### Phase 1: Data Import and Preliminary Analysis
- **Importing Libraries**: Necessary libraries such as `pandas`, `matplotlib`, `seaborn`, and `numpy` are imported at the start of the notebook.
- **Loading Datasets**: The datasets are loaded into Pandas DataFrames for easier manipulation and analysis.
- **Basic Statistics**: The phase focuses on computing the number of tweets mentioning each company's cashtag, which is stored in the `tweet_count` column of the `df_companies` DataFrame.

#### Key Steps in Phase 1:
1. **Computing Cashtag Counts**: The `tweet_count` column is populated by counting the number of tweets mentioning each company's cashtag (e.g., "$AAPL" for Apple).
2. **Visualization**: The results are visualized to show the top 20 most tweeted stocks. This helps identify which companies are most frequently discussed on social media.

### Phase 2: Sentiment Analysis and Correlation with Stock Prices
- **Sentiment Analysis**: This phase involves analyzing the sentiment of the tweets, using a text processing tool such as VADER (Valence Aware Dictionary and sEntiment Reasoner) or a machine learning model to classify the sentiment as positive, negative, or neutral.
- **Correlation with Stock Prices**: The analysis might explore the correlation between tweet sentiments or the number of tweets and stock price movements of the related companies.
- **Visualization**: Visual representations are used to showcase the relationship between social media activity and stock prices, highlighting any noticeable trends.

### Phase 3: Final Insights and Recommendations
- **Insights and Trends**: This phase summarizes key findings, possibly identifying patterns or correlations between tweet activity and stock performance.
- **Final Recommendations**: Based on the analysis, the project might offer insights on how investors could use social media activity to inform their trading decisions.

## Requirements
To run this project, make sure the following Python packages are installed:

- `numpy`
- `pandas`
- `matplotlib`
- `seaborn`

You can install the required libraries using the following command:

```bash
pip install numpy pandas matplotlib seaborn
