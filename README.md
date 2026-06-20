# Agentic AI Trading Dashboard 
# 🤖 Autonomous Multi-Signal Trading Agent

An AI-powered stock market analysis and trading decision system that combines **financial news sentiment analysis**, **machine learning**, **deep learning**, and **agentic decision-making** to generate BUY, SELL, or HOLD recommendations.

---

## 📌 Project Overview

The Autonomous Multi-Signal Trading Agent is an intelligent financial analysis platform designed to assist investors in understanding market conditions and making data-driven decisions.

Instead of relying on a single indicator, the system gathers information from multiple sources:

* Historical stock price data
* Technical indicators
* Financial news headlines
* Sentiment analysis
* Machine Learning predictions
* Deep Learning forecasts

The agent then combines all these signals and produces a final recommendation.

The system follows an Agentic AI workflow:

**Observe → Plan → Execute → Reflect → Decide**

This mimics how a human analyst evaluates market information before making an investment decision.

---

# 🎯 Problem Statement

Investors often struggle with:

* Information overload
* Conflicting market signals
* Emotional decision making
* Lack of technical expertise

This project aims to solve these problems by creating an automated system that:

1. Collects market data
2. Understands financial news
3. Predicts future stock prices
4. Evaluates conflicting signals
5. Produces a final recommendation

---

# 🚀 Features

### 📈 Historical Market Data Collection

The system automatically downloads stock market data using Yahoo Finance.

Collected data includes:

* Open Price
* High Price
* Low Price
* Close Price
* Volume

The application uses a multi-layer fallback architecture to ensure reliable data retrieval.

---

### 📰 News Collection

The agent fetches recent news headlines related to the selected company using Google News RSS feeds.

Examples:

* Company announcements
* Earnings reports
* Acquisitions
* Market developments

---

### 😊 Sentiment Analysis

The system analyzes whether the news is:

* Positive
* Negative
* Neutral

It uses:

#### FinBERT

FinBERT is a financial-domain version of BERT trained specifically on financial text.

Example:

**Headline:**
"Company reports record quarterly profits"

Result:

Positive sentiment

---

#### VADER + TextBlob

If FinBERT is unavailable, the system automatically switches to:

* VADER Sentiment Analysis
* TextBlob Sentiment Analysis

This ensures robustness.

---

### 📝 News Summarization

The project uses Facebook's BART model to generate concise summaries of multiple news headlines.

Benefits:

* Saves reading time
* Highlights key market developments
* Provides quick understanding of current events

---

### 🌲 Random Forest Prediction

The system trains a Random Forest Regression model using technical indicators.

Input Features:

* SMA 20
* EMA 20
* RSI
* Returns

Output:

Predicted future stock price

Evaluation Metrics:

* R² Score
* Mean Absolute Error (MAE)

---

### 🧬 LSTM Deep Learning Prediction

An LSTM (Long Short-Term Memory) neural network is used to learn patterns from historical stock prices.

Why LSTM?

Traditional models struggle with sequential financial data.

LSTM can:

* Learn long-term dependencies
* Capture trends
* Identify time-series patterns

---

### ⚡ Multi-Signal Decision Engine

The agent combines three signals:

| Signal               | Source                   |
| -------------------- | ------------------------ |
| Sentiment Signal     | Financial News           |
| Random Forest Signal | ML Prediction            |
| LSTM Signal          | Deep Learning Prediction |

Each signal votes:

* +1 = BUY
* 0 = HOLD
* -1 = SELL

The final decision is calculated using weighted voting.

---

### 🔄 Conflict Resolution

Market indicators often disagree.

Example:

* Sentiment = BUY
* Random Forest = SELL
* LSTM = BUY

The agent detects conflicts and automatically adjusts signal weights to reduce bias.

This makes the decision process more realistic and reliable.

---

### 📊 Backtesting Engine

The project includes a built-in backtesting framework.

The system:

1. Simulates trades
2. Tracks portfolio value
3. Compares performance against Buy-and-Hold strategy

Outputs include:

* Portfolio value
* Number of trades
* Total return
* Alpha generation

---

### 📋 Explainable AI

Every decision is logged.

Users can view:

* Data collection steps
* Model training process
* Sentiment results
* Conflict handling
* Final reasoning

This improves transparency and trust.

---

# 🏗 System Architecture

```text
User Input
     │
     ▼
Company Search
     │
     ▼
Market Data Collection
     │
     ▼
News Collection
     │
     ▼
Sentiment Analysis
(FinBERT / VADER)
     │
     ▼
News Summarization
(BART)
     │
     ▼
Random Forest Model
     │
     ▼
LSTM Model
     │
     ▼
Signal Aggregation
     │
     ▼
Conflict Resolution
     │
     ▼
Final BUY / SELL / HOLD Decision
     │
     ▼
Backtesting
```

---

# 🛠 Technologies Used

### Programming Language

* Python

### Frontend

* Streamlit

### Data Processing

* Pandas
* NumPy

### Visualization

* Matplotlib

### Financial Data

* Yahoo Finance API (yfinance)

### Web Scraping

* Requests
* BeautifulSoup

### NLP Models

* FinBERT
* BART
* VADER
* TextBlob

### Machine Learning

* Scikit-Learn
* Random Forest Regressor

### Deep Learning

* TensorFlow
* Keras
* LSTM

---

# 📦 Installation

Clone the repository:

```bash
git clone https://github.com/yourusername/autonomous-trading-agent.git

cd autonomous-trading-agent
```

Install dependencies:

```bash
pip install -r requirements.txt
```

Run the application:

```bash
streamlit run app.py
```

---

# 📈 Example Workflow

1. User searches for a company.
2. Agent downloads stock data.
3. News headlines are collected.
4. Sentiment analysis is performed.
5. News is summarized.
6. Random Forest model predicts future prices.
7. LSTM predicts future prices.
8. Signals are aggregated.
9. Conflicts are resolved.
10. Final recommendation is generated.
11. Backtesting evaluates strategy performance.

---

# 📊 Sample Output

Current Price: ₹1500

Random Forest Forecast: ₹1580

LSTM Forecast: ₹1605

Sentiment: Bullish

Decision: BUY

Confidence: 82%

---

* AI in Finance
* Investment Research
