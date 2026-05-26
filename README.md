# FinAnalysis AI Chatbot

AI-powered financial analysis platform that combines **real SEC filings, stock market data, financial ratio analysis, and LLM-powered reasoning** into an interactive chatbot experience.

The system pulls structured company financials from the **SEC EDGAR XBRL API**, enriches them with market data from **Yahoo Finance**, computes key financial metrics automatically, and enables users to ask natural-language financial questions through a Streamlit interface powered by **Anthropic Claude**.

---



---

# Overview

FinAnalysis AI acts like a financial research assistant.

Instead of manually reading SEC filings and calculating ratios, users can simply ask:

* “How profitable has Apple been over the past 5 years?”
* “Compare Amazon and Microsoft by revenue growth”
* “Is Tesla’s balance sheet improving?”
* “Which company has the strongest margins?”

The chatbot:

1. Retrieves structured financial data
2. Performs financial analysis
3. Selects the correct analysis tools/functions
4. Generates insights using Claude
5. Automatically renders charts and KPI visualizations

---

# Core Capabilities

## Real Financial Data Pipeline

The platform fetches:

* Income statements
* Balance sheets
* Cash flow statements
* Historical stock prices
* Market capitalization data

### Data Sources

* SEC EDGAR XBRL API
* Yahoo Finance (`yfinance`)

---

## Financial Ratio Engine

Automatically calculates 15+ financial metrics including:

### Profitability Metrics

* Gross Margin
* Operating Margin
* Net Profit Margin
* ROE (Return on Equity)
* ROA (Return on Assets)

### Growth Metrics

* Revenue CAGR
* Earnings Growth
* Free Cash Flow Growth

### Valuation Metrics

* P/E Ratio
* Price-to-Sales
* Market Cap comparisons

### Financial Health Metrics

* Debt Ratios
* Cash Position
* Liquidity indicators

---

## Claude-Powered Financial Chatbot

The chatbot uses:

* Anthropic Claude API
* Tool calling / function calling
* Context-aware financial analysis

Claude dynamically:

* Understands the user’s financial question
* Selects the appropriate analysis function
* Retrieves structured financial insights
* Generates human-readable explanations

---

## Interactive Analytics UI

Built with Streamlit and Plotly.

### Features

* Interactive financial charts
* Dynamic KPI cards
* Revenue trend visualizations
* Margin trend analysis
* Peer comparison charts
* Persistent conversation history
* Quick-action prompts

---

# Supported Companies

Currently configured for:

* Microsoft
* Apple
* Tesla
* Meta
* Amazon
* Netflix
* Alphabet (Google)

Additional companies can easily be added through ticker configuration.

---

# Architecture

## 1. Data Layer

Responsible for:

* SEC API integration
* XBRL parsing
* Market data retrieval
* Financial data normalization

### Technologies

* `requests`
* `pandas`
* `yfinance`

---

## 2. Analysis Layer

Performs:

* Financial ratio calculations
* Trend analysis
* Peer benchmarking
* Profitability analysis
* Balance sheet evaluation

Includes multiple modular analysis functions.

---

## 3. LLM Layer

Claude acts as the reasoning engine.

### Responsibilities

* Tool selection
* Question interpretation
* Financial insight generation
* Contextual responses

### AI Concepts Demonstrated

* Function calling
* Tool use
* AI orchestration
* Retrieval-based analysis
* Structured reasoning

---

## 4. Frontend Layer

Interactive web application built using:

* Streamlit
* Plotly

Provides:

* Real-time visual analytics
* Conversational interface
* Financial dashboards

---

# Tech Stack

| Layer         | Technologies                    |
| ------------- | ------------------------------- |
| Backend       | Python                          |
| Data Pipeline | SEC EDGAR API, yfinance, pandas |
| AI/LLM        | Anthropic Claude API            |
| Visualization | Plotly                          |
| Frontend      | Streamlit                       |
| Environment   | Python 3.10+, python-dotenv     |

---

# Machine Learning / AI Concepts Demonstrated

This project showcases several modern AI engineering concepts:

* LLM tool calling
* AI-powered financial analysis
* Retrieval-augmented reasoning
* Structured financial data pipelines
* Conversational analytics
* Context-aware response generation
* Function orchestration
* Interactive AI systems

---

# Project Structure

```bash
FinAnalysis-AI/
│
├── chatbot.py               # Core chatbot + tool calling logic
├── streamlit_app.py         # Streamlit web application
├── analysis.py              # Financial analysis functions
├── data_pipeline.py         # SEC + Yahoo Finance data pipeline
├── requirements.txt
├── .env
└── README.md
```

---

# Installation

## 1. Clone Repository

```bash
git clone https://github.com/your-username/FinAnalysis-AI.git
cd FinAnalysis-AI
```

---

## 2. Create Virtual Environment

### Windows

```bash
python -m venv .venv
.venv\Scripts\activate
```

### Mac/Linux

```bash
python -m venv .venv
source .venv/bin/activate
```

---

## 3. Install Dependencies

```bash
pip install -r requirements.txt
```

Or manually:

```bash
pip install anthropic requests pandas yfinance streamlit plotly python-dotenv
```

---

## 4. Configure Environment Variables

Create a `.env` file:

```env
ANTHROPIC_API_KEY=your_api_key_here
```

Get your API key from:

[Anthropic Console](https://console.anthropic.com?utm_source=chatgpt.com)

---

# Running the Application

## Streamlit Web App

```bash
streamlit run streamlit_app.py
```

Open:

```text
http://localhost:8501
```

---

## Terminal Chatbot

```bash
python chatbot.py
```

---

# Example Questions

### Company Analysis

* “Give me a snapshot of Netflix”
* “Analyze Apple’s profitability”

### Growth Analysis

* “How fast has Amazon grown revenue?”
* “Which company has the highest CAGR?”

### Comparative Analysis

* “Compare Microsoft and Google margins”
* “Compare all companies by market cap”

### Financial Health

* “Is Tesla’s balance sheet improving?”
* “Which company has the strongest cash position?”

---

# Key Highlights

## End-to-End AI System

This project demonstrates the complete lifecycle of:

* Data ingestion
* Financial processing
* AI reasoning
* Visualization
* Interactive deployment

---

## Real-World Financial Analytics

Uses:

* Real SEC filings
* Real stock market data
* Automated ratio analysis

instead of static datasets.

---

## Modern LLM Engineering

Implements:

* Claude tool calling
* Function orchestration
* Context-aware conversational AI

which are core modern GenAI engineering skills.

---

# Future Improvements

Potential extensions include:

* Multi-company portfolio analysis
* RAG over SEC filings
* Earnings call transcript analysis
* Real-time stock tracking
* AI-generated investment summaries
* Agentic financial workflows
* Multi-LLM support
* Vector database integration

---


