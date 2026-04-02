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

 The following stocks can be analysed for free without any financial dataset api 
   - AAPL (Apple)
   - MSFT (Microsoft)
   - NVDA (Nvidia)

Output Scheenshots (in terminal):
![Terminal Output](https://github.com/rashidmohamedali2909-ctrl/QuantEdge-AI/blob/3519e56316ef3864249ac93298e4b13b5ece4e83/terminal1.png)

![Terminal Output](https://github.com/rashidmohamedali2909-ctrl/QuantEdge-AI/blob/ffa595e58fc2f723bbb8823efef917d175d5b859/terminal2.png)

![Terminal Output](https://github.com/rashidmohamedali2909-ctrl/QuantEdge-AI/blob/5a22792131881d56b26d787acaf1611a10f2719b/terminal3.png)

---

### Frontend (UI)

The frontend provides a simple interface to run the system and view results more easily.

- Clean and interactive UI
- Easier to use compared to CLI

⚠️ Note: Currently, the UI works only with an OpenAI API key.

![Frontend UI](./assets/ui.png)

---

## How to run

#### 1. Clone and install

### 1. Clone the Repository

```bash
git clone https://github.com/rashidmohamedali2909-ctrl/QuantEdge-AI.git
cd QuantEdge-AI
```

### 2. Set up API keys

Create a `.env` file for your API keys:
```bash
# Create .env file for your API keys (in the root directory)
cp .env.example .env
```

Open and edit the `.env` file to add your API keys:
```bash
# For running LLMs hosted by openai (gpt-4o, gpt-4o-mini, etc.)
OPENAI_API_KEY=your-openai-api-key

# For getting financial data to power the AI analyser
FINANCIAL_DATASETS_API_KEY=your-financial-datasets-api-key
```
### Run in Terminal (CLI)

You can run the AI Hedge Fund directly via terminal. This approach offers more granular control and is useful for automation, scripting, and integration purposes.

#### Quick Start

1. Install Poetry (if not already installed):
```bash
curl -sSL https://install.python-poetry.org | python3 -
```

2. Install dependencies:
```bash
poetry install
```

#### Run the AI Hedge Fund 
```bash
poetry run python src/main.py --ticker AAPL,MSFT,NVDA
```

You can also specify a `--ollama` flag to run the AI hedge fund using local LLMs where you no need any api key.

```bash
poetry run python src/main.py --ticker AAPL,MSFT,NVDA --ollama
```

You can optionally specify the start and end dates to make decisions over a specific time period.

```bash
poetry run python src/main.py --ticker AAPL,MSFT,NVDA --start-date 2024-01-01 --end-date 2024-03-01
```

## Run using Ollama (No API key)

You can run QuantEdge AI using local models with Ollama. This does not require any API key.


### 1. Install Ollama

Download Ollama from:

https://ollama.com

- Install it like a normal application  
- After installation, open terminal and verify:

```bash
ollama --version

If installed correctly, it will show the version.


next download any model from the list shown below.

![Available Models](https://github.com/rashidmohamedali2909-ctrl/QuantEdge-AI/blob/9f7686c1c33fe041059525db6447e41558a1ed9d/models.png)
