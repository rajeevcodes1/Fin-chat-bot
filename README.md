# FinAnalysis AI Chatbot

An AI-powered financial analysis chatbot that pulls real data from SEC EDGAR and Yahoo Finance, calculates key financial ratios, and lets users ask natural language questions through a Streamlit web interface backed by Claude (Anthropic).

---
## Video Demo: 
https://youtu.be/OK2bGdPo6vU


https://github.com/user-attachments/assets/ae098892-2579-4e81-b0df-89a15e557b79


## What It Does

- Fetches 5 years of financial data directly from the **SEC EDGAR XBRL API** for 7 companies(and More!!)
- Enriches the dataset with **historical stock prices and market data** via Yahoo Finance
- Calculates **15+ financial ratios** including margins, ROE, ROA, CAGR, and valuation multiples
- Provides a **Claude-powered chatbot** that answers natural language financial questions using tool calling
- Renders **interactive charts** automatically based on the user's question

---

## Skills Demonstrated

- REST API integration and JSON parsing 
- Financial data wrangling with pandas
- LLM tool use/function calling (Anthropic Claude)
- Interactive data visualization (Plotly)
- End-to-end application development (data → analysis → UI)

---

## Companies Covered 

Microsoft · Apple · Tesla · Meta · Amazon · Netflix · Alphabet (Google)
You can add the companies that you are interested too! 

---

## Tech Stack

| Layer | Tools |
|---|---|
| Data pipeline | SEC EDGAR XBRL API, `yfinance`, `pandas` |
| LLM backend | Anthropic Claude API (tool use/function calling) |
| Web UI | Streamlit, Plotly | google colab | or terminal-based
| Environment | Python 3.10+, `python-dotenv` |

---

## Key Features

**Data pipeline** — `chatbot.py`
- Pulls structured financial data (income statement, balance sheet, cash flow) from SEC EDGAR
- Handles both duration and instant XBRL concepts
- Merges with historical market data and computes all ratios automatically

**Analysis layer** — 7 plain-text analysis functions covering snapshots, profitability, growth, balance sheet health, peer comparisons, and trend detection

**Chatbot** — Claude selects the right analysis function via tool calling and returns a human-readable response with data-backed insights

**Streamlit UI** — `streamlit_app.py`
- Context-aware KPI cards that update based on the company being discussed
- Charts auto-render alongside answers (revenue trends, margin lines, balance sheet breakdown, peer comparisons)
- Conversation history with quick-action prompt buttons

---

## Setup

**1. Clone or download the project**

**2. Create a virtual environment**
```bash
python -m venv .venv
source .venv/bin/activate        # Mac / Linux
.venv\Scripts\activate           # Windows
```

**3. Install dependencies**
```bash
pip install anthropic requests pandas yfinance streamlit plotly python-dotenv
```
or
```
pip install -r requirements.txt
```

**4. Add your Anthropic API key**

Create a `.env` file in the project folder:
```
ANTHROPIC_API_KEY=sk-ant-...
```

Get a key at [console.anthropic.com](https://console.anthropic.com)

---

## Running the Web App

**Streamlit UI**
```
streamlit run streamlit_app.py
```
Then open [http://localhost:8501](http://localhost:8501)

**Terminal chatbot**
```
python chatbot.py
```

---


## Sample Questions

- *"Give me a snapshot of Netflix"*
- *"How profitable has Apple been over the past 5 years?"*
- *"Which company has the highest net profit margin?"*
- *"How fast has Amazon grown its revenue?"*
- *"Is Tesla's balance sheet improving?"*
- *"Compare all companies by market cap"*

---

