# Multiplatform Sentiment Analysis

A multiplatform sentiment analysis project comparing **LightGBM and BiLSTM** for sentiment classification across **Facebook, Instagram, TikTok, Twitter (X), and YouTube**, using **IndoBERTweet embeddings**.

This project was developed as part of my undergraduate thesis in Information Systems at Institut Teknologi Nasional Bandung (ITENAS).

## Project Overview

The project analyzes user comments collected from five social media platforms and evaluates the performance of two classification approaches:

* LightGBM (Machine Learning)
* BiLSTM (Deep Learning)

The overall workflow consists of:

**Data Integration → EDA & Preprocessing → Pseudolabeling → Embedding → Classification & Evaluation**

## Dataset

The `RawData/` directory contains the raw comment datasets collected from:

* Facebook
* Instagram
* TikTok
* X (Twitter)
* YouTube

## Project Structure

```text
multiplatform-sentiment-analysis/
├── README.md
│
├── MultiplatformMergeRawData/
│   ├── fb_comment.csv
│   ├── ig_comment.csv
│   ├── tt_comment.csv
│   ├── twt_comment.csv
│   └── yt_comment.csv
│
└── MultiplatformSentimentAnalysisNotebook/
    ├── 01-integrasi/
    ├── 02-eda-preprocessing/
    ├── 03-pseudolabeling/
    ├── 04-embedding/
    └── 05-classification-evaluation/
```

## Methodology

### 1. Data Collection

Comments were collected from five social media platforms: **Facebook, Instagram, TikTok, X (Twitter), and YouTube**.

Data from Facebook, Instagram, TikTok, and X were collected using a **Chrome browser extension**, while YouTube comments were collected using the **YouTube API**.

### 2. Data Integration

Multiple comment files collected from the same social media platform were combined into a single dataset. For example, several Facebook comment files (`fb1`, `fb2`, `fb3`) were integrated into `fb_comment.csv`.

This process was performed separately for each platform to obtain five consolidated datasets:

* `fb_comment.csv`
* `ig_comment.csv`
* `tt_comment.csv`
* `twt_comment.csv`
* `yt_comment.csv`

### 3. EDA & Preprocessing

Exploratory data analysis and text preprocessing were performed for each social media platform. The preprocessing steps included data cleaning, case folding, noise removal, and text normalization.

### 4. Pseudolabeling

Sentiment labels were generated using a **fine-tuned IndoBERTweet** model as part of the sentiment labeling process.

### 5. Embedding

The preprocessed text was transformed into numerical representations using **IndoBERTweet embeddings**.

### 6. Classification & Evaluation

The resulting data were used to train and compare two classification models:

* **LightGBM**
* **BiLSTM**

Model performance was evaluated using:

* Accuracy
* Precision
* Recall
* F1-score


## Technologies

* Python
* Pandas
* NumPy
* Scikit-learn
* Hugging Face Transformers
* IndoBERTweet
* LightGBM
* TensorFlow / Keras
* Jupyter Notebook

## Thesis

This repository supports my undergraduate thesis on the comparison of LightGBM and BiLSTM for multiplatform sentiment classification using IndoBERTweet embeddings.

More details about the methodology, experimental setup, and results are available in the notebooks.
