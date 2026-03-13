# Explainable_Alpha_Agent-Quality_Scorecard
This agent focuses on Fundamental Analysis. It scans a universe of stocks to find companies with high "moats" and sustainable growth.

# Project Blueprint: The Explainable Alpha Agent 📈

> Build an agent that analyzes financial data from your Google Drive to identify long-term investment opportunities — with a clear **"audit trail"** of its reasoning.

---

## 📌 What We're Building

An agent that:

1. **Reads** raw financial statements (CSV/Excel) from your Google Drive via a custom MCP server
2. **Calculates** key metrics like Return on Invested Capital (`ROIC`) and Free Cash Flow (`FCF`) margins
3. **Reasons** through qualitative "moat" factors using a Hugging Face model
4. **Generates** a final `Buy / Hold / Avoid` recommendation based on long-term alpha potential

---

## 🗺️ Phase Roadmap

| Phase | Title | Goal | Input | Output | Key Tech |
|---|---|---|---|---|---|
| **1** | The Brain 🧠 | Load a high-reasoning model in Colab | HF Token, GPU | Loaded LLM | `transformers`, `bitsandbytes` (4-bit quantization) |
| **2** | The Bridge 🌉 | Create a "server" that lets the LLM "see" your Drive | Drive Path | MCP Server | `mcp` Python SDK, `google.colab` drive mount |
| **3** | The Skills 🛠️ | Define tools for financial calculation and retrieval | Raw CSV / Data | Clean Metrics | Python functions as "Tools", Financial Ratios ($ROIC$, $FCF$) |
| **4** | The Loop 🔄 | Connect the brain to the tools to analyze a ticker | User Ticker | Thesis + Score | `langchain` or a lightweight custom loop |
