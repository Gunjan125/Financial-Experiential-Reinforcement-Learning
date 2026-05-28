# 📈 Experiential Reinforcement Learning for Stock Market Trading using LLMs

An AI-powered autonomous trading framework that combines Large Language Models (LLMs), financial news understanding, semantic memory retrieval, and reinforcement-style learning to simulate a self-improving trading agent.

---

# 🚀 Project Overview

Traditional trading systems rely heavily on:

* Technical indicators
* Statistical analysis
* Fixed rule-based strategies

This project introduces a different approach where an AI agent:

* Reads financial news
* Understands market context
* Makes trading decisions
* Reflects on outcomes
* Learns from past experiences
* Improves future decisions over time

The system mimics human-like experiential learning using reflection and memory.

---

# ✨ Features

* 📊 News-based stock trading simulation
* 🧠 LLM-powered trading decisions
* 💭 Reflection-based learning
* 🔍 Semantic memory retrieval using FAISS
* 📈 Real DJIA market data integration
* ⚡ GPU accelerated inference
* 🔄 Adaptive learning loop
* 📚 Experience internalization

---

# 🛠️ Tech Stack

* Python
* PyTorch
* Hugging Face Transformers
* Sentence Transformers
* FAISS
* Pandas
* NumPy
* yFinance

---

# 🤖 Models Used

## Embedding Model

```python
sentence-transformers/all-MiniLM-L6-v2
```

Used for:

* Reflection embeddings
* Semantic similarity search
* Memory retrieval

---

## Language Models

### Initial Model

```python
mistralai/Mistral-7B-Instruct-v0.3
```

### Final Trading Agent

```python
Qwen/Qwen2.5-7B-Instruct
```

Used for:

* Trading decisions
* Reflection generation
* Strategy improvement

---

# 📂 Dataset

The project uses:

* Financial news headlines
* DJIA historical stock prices

Dataset includes:

* Banking news
* Economic events
* Market movements
* Corporate announcements
* Financial sentiment

---

# 🏗️ System Architecture

```text
Financial News
       ↓
State Representation
       ↓
LLM Decision Making
       ↓
Trading Simulation
       ↓
Reward Feedback
       ↓
Reflection Generation
       ↓
Semantic Memory Storage
       ↓
Improved Future Decisions
```

---

# 🔥 Key Components

## 1. ReflectionMemory

Stores useful reflections using vector embeddings.

### Features

* Semantic search
* FAISS indexing
* Similar experience retrieval

---

## 2. TradingEnv

Custom trading simulation environment.

### Supports

* Buy
* Sell
* Hold
* Portfolio tracking
* Reward calculation

---

## 3. ERLAgent

Main intelligent trading agent.

### Responsibilities

* Analyze financial news
* Generate trading actions
* Reflect on outcomes
* Internalize successful strategies

---

# 🔄 Workflow

## Step 1 — Load Financial News

```python
df = pd.read_csv('Combined_News.csv')
```

---

## Step 2 — Download DJIA Prices

```python
yf.download('^DJI')
```

---

## Step 3 — Merge News + Market Data

```python
df = df_news.merge(prices, on='Date')
```

---

## Step 4 — Generate Trading Action

Example output:

```json
{
  "decision": "buy",
  "fraction": 0.6
}
```

---

## Step 5 — Simulate Trade

The environment calculates:

* Portfolio value
* Profit/Loss
* Reward

---

## Step 6 — Generate Reflection

Example:

> "Positive banking news correlated with upward market movement. Increase buying confidence during similar situations."

---

## Step 7 — Store Successful Experiences

Useful reflections are embedded and stored in memory for future retrieval.

---

# 🧠 Memory-Augmented Intelligence

Before making a new decision, the agent retrieves:

* Similar past experiences
* Relevant reflections
* Successful strategies

This improves future trading decisions.

---

# 📊 Sample Output

```text
Day 32 | r1=+0.0069  r2=+0.0069  Stored=True  Return= +0.57%
```

### Explanation

| Metric      | Meaning                     |
| ----------- | --------------------------- |
| r1          | Initial reward              |
| r2          | Reflection-improved reward  |
| Stored=True | Reflection stored in memory |
| Return      | Portfolio return            |

---

# ⚡ GPU Optimization

The project includes memory optimization:

```python
torch.cuda.empty_cache()
gc.collect()
```

Also uses:

* Half precision inference
* Automatic device mapping

---

# 📦 Installation

## Clone Repository

```bash
git clone https://github.com/yourusername/erl-stock-trading.git
cd erl-stock-trading
```

---

## Install Dependencies

```bash
pip install -q --upgrade \
sentence-transformers \
faiss-cpu \
rank_bm25 \
accelerate \
transformers \
torch \
yfinance
```

---

# ▶️ Run the Project

```bash
python main.py
```

---

# 📈 Future Improvements

* Multi-stock trading
* Real-time market streaming
* Technical indicators integration
* Sentiment analysis pipeline
* Risk management module
* PPO/DQN hybrid learning
* Financial dashboard
* Fine-tuned finance-specific LLMs

---

# 🔬 Research Concepts Used

* Reinforcement Learning
* Reflection-based Learning
* Memory-Augmented AI
* Retrieval-Augmented Generation (RAG)
* Financial NLP
* Autonomous AI Agents
* Semantic Search
* LLM Reasoning

---

# 📌 Why This Project Matters

This project explores the future of:

* Self-improving AI systems
* Reflection-driven intelligence
* Autonomous reasoning agents
* AI-powered financial decision making

It combines:

* LLMs
* Reinforcement-style learning
* Vector memory
* Financial reasoning
* Autonomous adaptation

into one unified system.

---

# 👩‍💻 Author

Gunjan Soni
Computer Science Student | AI/ML Enthusiast | Research Explorer

---

# 📜 License

This project is licensed under the MIT License.

---

# 🙌 Acknowledgements

* Hugging Face
* Qwen Team
* Mistral AI
* Sentence Transformers
* FAISS by Meta
* Yahoo Finance

