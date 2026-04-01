# QuantEdge AI

## Table of Contents

- Overview[#Overview]
- What it does
- Preview (CLI & UI)
- How to run
- TODO

---

## Overview

QuantEdge AI is a project where I explored how AI can be used to analyze financial data and support basic trading decisions.

The system is built using multiple agents, where each handles a specific task like sentiment analysis, valuation, or risk evaluation. These outputs are then combined to simulate a simple decision-making process. In simple terms, it uses LLMs to analyze patterns and generate basic investing insights.

---

## What it does

- Takes financial data as input
- Uses AI models (LLMs) to analyze it from different perspectives
- Combines results like sentiment, fundamentals, and technical signals
- Produces a basic investing insight or decision

In simple terms, it acts like a basic AI-powered analyst that looks at data and gives a structured output.

---

## Preview (CLI & UI)

QuantEdge AI can be used in two ways:

- Command line (CLI) for direct execution
- Web interface (UI) for a more user-friendly experience

---

### Terminal (CLI)

The CLI version runs directly in the terminal and shows the analysis output step by step.

- Supports API-based models (like OpenAI)
- Can also run using local models (like Ollama)

- AAPL (Apple)
- MSFT (Microsoft)
- NVDA (Nvidia)

![Terminal Output](https://github.com/rashidmohamedali2909-ctrl/QuantEdge-AI/blob/3519e56316ef3864249ac93298e4b13b5ece4e83/terminal1.png)

![Terminal Output](./assets/terminal2.png)

![Terminal Output](./assets/terminal3.png)

---

### Frontend (UI)

The frontend provides a simple interface to run the system and view results more easily.

- Clean and interactive UI
- Easier to use compared to CLI

⚠️ Note: Currently, the UI works only with an OpenAI API key.

![Frontend UI](./assets/ui.png)
