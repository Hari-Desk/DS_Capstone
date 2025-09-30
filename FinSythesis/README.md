FinSythesis

A Multi-Agent GenAI Framework for Stock Price Forecasting with Sentiment and Market Signals

📌 Overview

FinSythesis is a multi-agent, Retrieval-Augmented Generation (RAG) pipeline designed for financial decision-making.
It simulates the workflow of a trading firm, where specialized AI agents (Fundamentals, Sentiment, News, Technical, Trader, and Risk/Portfolio Manager) collaborate and debate to produce Buy / Hold / Sell recommendations.

The system integrates real-time APIs (Finnhub, yfinance) and cached datasets for reproducibility, while leveraging LangChain, LangGraph, and modern LLMs (OpenAI, Google, Anthropic) for reasoning.

⚙ Installation
1. Clone the Repository
git clone https://github.com/Hari-Desk/DS_Capstone.git
cd DS_Capstone/FinSythesis

2. Create and Activate Environment
conda create -n finsythesis python=3.10
conda activate finsythesis

3. Install Dependencies
pip install -r requirements.txt

🔑 Configuration

Set your API keys as environment variables before running:

export FINNHUB_API_KEY=your_finnhub_api_key
export OPENAI_API_KEY=your_openai_api_key
export GOOGLE_API_KEY=your_google_api_key


Optional: Edit config.py to change agent settings (e.g., LLM provider, debate rounds, offline/online mode).

🚀 Running the Application

Run the CLI:

python -m cli.main


Example (Tesla on May 10, 2024):

python -m cli.main --ticker TSLA --date 2024-05-10


This will:

Retrieve fundamentals, sentiment, news, and technical indicators.

Generate analyst reports.

Run a multi-agent debate (bullish, bearish, neutral perspectives).

Produce a final trade decision and investment plan.

📂 Outputs

After execution, you will find:

fundamentals_report.md – Company metrics and financials.

news_report.md – Global and sector-specific news.

sentiment_report.md – Reddit/social sentiment analysis.

market_report.md – Macro and micro market conditions.

final_trade_decision.md – Consolidated Buy/Hold/Sell recommendation.

investment_plan.md – Risk-adjusted trading strategy.

⚡ Notes

Use --offline to run with cached data (ensures reproducibility).

Use --online to fetch live financial data from APIs.

Different LLM providers (OpenAI, Google Gemini, Anthropic) can be swapped in via config.py.