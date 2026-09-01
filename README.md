# 📊 YouTube US Comments — Sentiment & Emoji Analysis

A data analysis project that performs **sentiment analysis** and **emoji analysis** on YouTube US comments dataset using Python.

---

## 📁 Dataset

- **UScomments.csv** — Contains 691,000+ YouTube comments with the following columns:
  - `video_id` — YouTube video ID
  - `comment_text` — The comment text
  - `likes` — Number of likes on the comment
  - `replies` — Number of replies

---

## 🔍 What This Project Does

1. **Data Cleaning** — Removes null values and fixes mixed data type issues
2. **Sentiment Analysis** — Uses `TextBlob` to calculate polarity score for each comment
3. **Sentiment Distribution** — Bar chart showing Positive / Neutral / Negative breakdown
4. **Polarity Histogram** — Distribution of polarity scores across comments
5. **Word Clouds** — Separate word clouds for Positive and Negative comments
6. **Emoji Analysis** — Extracts and ranks the top 10 most used emojis with an interactive Plotly chart

---

## 📊 Results

| Sentiment | % of Comments |
|-----------|--------------|
| Positive  | ~43%         |
| Neutral   | ~41%         |
| Negative  | ~16%         |

**Top Emojis:** 😂 😍 ❤ 🔥 😭 👏 😘 👍 💖 💕

---

## 🛠️ Libraries Used

```
pandas
numpy
textblob
wordcloud
emoji
seaborn
matplotlib
plotly
collections
```

---

## 🚀 How to Run

1. Clone this repository:
```bash
git clone https://github.com/Nayan0223/youtube-comments-analysis.git
```

2. Install dependencies:
```bash
pip install pandas numpy textblob wordcloud emoji seaborn matplotlib plotly
```

3. Open the notebook:
```bash
jupyter notebook YouTube_Comments_Analysis_Fixed.ipynb
```

---

## 📸 Output Charts

| Chart | Description |
|-------|-------------|
| `1_sentiment_distribution.png` | Bar chart of Positive / Neutral / Negative comments |
| `2_wordclouds.png` | Word clouds for positive and negative comments |
| `3_top_emojis.png` | Top 10 most used emojis |
| `4_polarity_histogram.png` | Distribution of polarity scores |

---

## 👤 Author

**Nayan0223**  
GitHub: [@Nayan0223](https://github.com/Nayan0223)
