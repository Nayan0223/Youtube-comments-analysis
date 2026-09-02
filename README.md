<div align="center">

# 📊 YouTube Comments Sentiment & Emoji Analysis

### *Deep-Dive Natural Language Processing & Sentiment Mining on 690,000+ YouTube Comments*

[![Python](https://img.shields.io/badge/Python-3.8%2B-3776AB?style=for-the-badge&logo=python&logoColor=white)](https://www.python.org/)
[![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-F37626?style=for-the-badge&logo=jupyter&logoColor=white)](https://jupyter.org/)
[![Pandas](https://img.shields.io/badge/Pandas-Data_Analysis-150458?style=for-the-badge&logo=pandas&logoColor=white)](https://pandas.pydata.org/)
[![Plotly](https://img.shields.io/badge/Plotly-Interactive_Viz-3F4F75?style=for-the-badge&logo=plotly&logoColor=white)](https://plotly.com/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg?style=for-the-badge)](https://opensource.org/licenses/MIT)
[![Maintenance](https://img.shields.io/badge/Maintained%3F-yes-green.svg?style=for-the-badge)](https://github.com/Nayan0223/Youtube-comments-analysis)

<p align="center">
  <a href="#-project-overview">Overview</a> •
  <a href="#-key-insights--findings">Key Insights</a> •
  <a href="#-visual-gallery">Visual Gallery</a> •
  <a href="#-data-pipeline--architecture">Pipeline</a> •
  <a href="#-tech-stack">Tech Stack</a> •
  <a href="#-quick-start">Quick Start</a> •
  <a href="#-project-structure">Structure</a> •
  <a href="#-future-roadmap">Roadmap</a>
</p>

---

</div>

## 📌 Project Overview

This repository features an end-to-end **Data Analysis & Natural Language Processing (NLP)** pipeline built to analyze viewer sentiment, polarity distributions, and emoji usage patterns across **691,000+ real-world YouTube comments**.

Using **TextBlob**, **WordCloud**, **Emoji 2.0+**, **Seaborn**, and **Plotly**, this project extracts actionable behavioral insights from audience engagement on trending YouTube videos.

---

## ⚡ Key Highlights & Metrics

<div align="center">

| 📁 Dataset Scale | 💬 Analyzed Comments | 😃 Emojis Extracted | 🎯 Sentiment Classes |
| :---: | :---: | :---: | :---: |
| **691,400+ Rows** | **691,373 Cleaned** | **294,549 Emojis** | **Positive / Neutral / Negative** |

</div>

---

## 💡 Key Insights & Findings

### 1. Overall Sentiment Distribution
Viewer feedback on YouTube skews significantly **optimistic and constructive**:

- 🟢 **Positive Comments (~43%)**: Praise, enthusiasm, appreciation, and excitement.
- ⚪ **Neutral Comments (~41%)**: Questions, timestamps, context links, and factual statements.
- 🔴 **Negative Comments (~16%)**: Constructive criticism, disagreement, or discontent.

```
Positive   [██████████████████████] 43%
Neutral    [█████████████████████ ] 41%
Negative   [████████              ] 16%
```

### 2. Top 10 Most Frequent Emojis
A total of **294,549 emojis** were parsed across the entire dataset. The top 10 represent over **50%** of all emoji interactions:

| Rank | Emoji | Meaning / Emotion | Total Occurrences | Share (%) |
| :---: | :---: | :--- | :---: | :---: |
| **#1** | 😂 | Face with Tears of Joy | **36,987** | 12.56% |
| **#2** | 😍 | Smiling Face with Heart-Eyes | **33,453** | 11.36% |
| **#3** | ❤ | Red Heart | **31,119** | 10.56% |
| **#4** | 🔥 | Fire (Hype / Trend) | **8,694** | 2.95% |
| **#5** | 😭 | Loudly Crying Face | **8,398** | 2.85% |
| **#6** | 👏 | Clapping Hands | **5,719** | 1.94% |
| **#7** | 😘 | Face Blowing a Kiss | **5,545** | 1.88% |
| **#8** | 👍 | Thumbs Up | **5,476** | 1.86% |
| **#9** | 💖 | Sparkling Heart | **5,359** | 1.82% |
| **#10** | 💕 | Two Hearts | **5,147** | 1.75% |

---

## 📸 Visual Gallery

<div align="center">

### 1. Sentiment Distribution & Polarity Histogram

| Sentiment Breakdown | Polarity Score Distribution |
| :---: | :---: |
| ![Sentiment Distribution](1_sentiment_distribution.png) | ![Polarity Histogram](4_polarity_histogram.png) |
| *High ratio of positive vs. negative engagement* | *Distribution centered around 0 with positive skew* |

---

### 2. Word Clouds (Positive vs. Negative Sentiment)

![Word Clouds](2_wordclouds.png)
*Left: Positive Lexicon ("love", "awesome", "best", "great") • Right: Negative Lexicon ("hate", "bad", "worst", "terrible")*

---

### 3. Emoji Popularity Ranking

![Top Emojis](3_top_emojis.png)
*Top 10 emojis displaying dominant emotional tone across YouTube comments*

</div>

---

## 🔄 Data Pipeline & Architecture

```mermaid
flowchart TD
    A[📂 UScomments.csv <br/> 691,400 Raw Comments] --> B[🧹 Data Preprocessing & Cleaning]
    B --> B1[Remove Duplicate Headers]
    B --> B2[Handle Null / Mixed Data Types]
    B --> B3[Type Casting: likes & replies to int64]
    
    B3 --> C[⚡ NLP Sentiment Engine <br/> TextBlob Polarity Scoring]
    B3 --> D[😃 Emoji Extraction Engine <br/> emoji.EMOJI_DATA Tokenizer]
    
    C --> E[📊 Polarity Classification]
    E --> E1[Positive: Polarity > 0]
    E --> E2[Neutral: Polarity = 0]
    E --> E3[Negative: Polarity < 0]
    
    E --> F[☁️ WordCloud Generator <br/> Positive vs Negative Lexicons]
    E --> G[📈 Matplotlib & Seaborn Charts]
    
    D --> H[🔢 Frequency Counter <br/> collections.Counter]
    H --> I[📊 Top 10 Ranked Bar Charts]
    H --> J[🌐 Interactive Plotly Dashboards]
```

---

## 🛠️ Tech Stack & Dependencies

<div align="center">

| Domain | Technology / Library | Usage |
| :--- | :--- | :--- |
| **Core Language** | ![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white) | Primary programming language |
| **Data Manipulation** | ![Pandas](https://img.shields.io/badge/Pandas-150458?style=flat-square&logo=pandas&logoColor=white) ![NumPy](https://img.shields.io/badge/NumPy-013243?style=flat-square&logo=numpy&logoColor=white) | Large-scale CSV processing & array operations |
| **NLP & Sentiment** | ![TextBlob](https://img.shields.io/badge/TextBlob-3F51B5?style=flat-square) ![WordCloud](https://img.shields.io/badge/WordCloud-009688?style=flat-square) | Sentiment polarity scoring & token frequency cloud |
| **Emoji Processing** | ![Emoji](https://img.shields.io/badge/Emoji%202.0%2B-FF9800?style=flat-square) | Unicode emoji extraction & ranking |
| **Visualization** | ![Matplotlib](https://img.shields.io/badge/Matplotlib-11557C?style=flat-square) ![Seaborn](https://img.shields.io/badge/Seaborn-3776AB?style=flat-square) ![Plotly](https://img.shields.io/badge/Plotly-3F4F75?style=flat-square&logo=plotly&logoColor=white) | Static charts & interactive visualizations |
| **Environment** | ![Jupyter](https://img.shields.io/badge/Jupyter-F37626?style=flat-square&logo=jupyter&logoColor=white) | Interactive notebook development |

</div>

---

## 🚀 Quick Start

### 1. Clone the Repository
```bash
git clone https://github.com/Nayan0223/Youtube-comments-analysis.git
cd Youtube-comments-analysis
```

### 2. Create and Activate Virtual Environment (Recommended)
```bash
# On macOS / Linux
python3 -m venv venv
source venv/bin/activate

# On Windows
python -m venv venv
venv\Scripts\activate
```

### 3. Install Dependencies
```bash
pip install pandas numpy textblob wordcloud emoji seaborn matplotlib plotly jupyter
```

### 4. Launch Jupyter Notebook
```bash
jupyter notebook YouTube_Comments_Analysis_Fixed.ipynb
```

---

## 📁 Project Structure

```bash
Youtube-comments-analysis/
├── 📄 README.md                            # Comprehensive project documentation
├── 📓 YouTube_Comments_Analysis_Fixed.ipynb# Main analysis notebook (clean & optimized)
├── 📊 UScomments.csv                       # Raw YouTube comments dataset (691K+ rows)
├── 📈 1_sentiment_distribution.png         # Chart: Sentiment distribution
├── ☁️ 2_wordclouds.png                     # Chart: Positive & Negative wordclouds
├── 😃 3_top_emojis.png                     # Chart: Top 10 emojis frequency
└── 📉 4_polarity_histogram.png             # Chart: Polarity distribution histogram
```

---

## 🔧 Robust Engineering Fixes Included

The notebook includes built-in optimizations to resolve common big data and version compatibility issues:

- 🛡️ **Mixed-Type Warnings**: Uses `low_memory=False` and `on_bad_lines='skip'` to seamlessly read 70MB+ CSV files.
- 🧹 **Corrupt Row Scrubbing**: Automatically removes duplicated CSV headers embedded inside data rows.
- ⚡ **Vectorized Sampling**: Optimized processing flow to compute NLP sentiment without memory bottlenecks.
- 📦 **Emoji v2.0+ Compatibility**: Migrated to `emoji.EMOJI_DATA` dictionary lookup (replacing deprecated `UNICODE_EMOJI`).

---

## 🔮 Future Roadmap

- [ ] **Transformer-based Sentiment Model**: Implement fine-tuned `VADER` and `BERT / RoBERTa` models for comparative evaluation.
- [ ] **Interactive Web App**: Build a live [Streamlit](https://streamlit.io/) dashboard for real-time YouTube video URL analysis.
- [ ] **Topic Modeling**: Implement Latent Dirichlet Allocation (LDA) and BERTopic to uncover discussion themes.
- [ ] **Live YouTube API Integration**: Fetch real-time comments using the YouTube Data API v3.

---

## 🤝 Contributing

Contributions, issues, and feature requests are welcome!  
Feel free to check the [issues page](https://github.com/Nayan0223/Youtube-comments-analysis/issues).

1. Fork the project
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

---

## 📄 License

This project is licensed under the **MIT License** — see the [LICENSE](LICENSE) file for details.

---

<div align="center">

### 👤 Author

**Nayan Bharodiya**

[![GitHub](https://img.shields.io/badge/GitHub-Nayan0223-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/Nayan0223)

⭐ *If you found this project helpful, please consider giving it a star!* ⭐

</div>
