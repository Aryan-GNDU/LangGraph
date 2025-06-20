# 🧠 LangGraph (SQL Agent)

This project implements an intelligent **SQL Agent** using [LangGraph](https://github.com/langchain-ai/langgraph) — a powerful framework for building multi-agent and stateful LLM systems.

The agent is capable of interpreting natural language queries and translating them into executable SQL commands for querying a relational database (e.g., MySQL or PostgreSQL).

---

## 🚀 Features

- 🔄 Converts natural language to SQL using an LLM-powered graph
- 📊 Executes queries against a live SQL database
- 🧠 Leverages LangGraph for modular, stateful decision-making
- 🧩 Easily extendable to support multiple databases or query types
- 🪵 Includes logging and error handling

---

## 🏗️ Architecture

- **LangGraph Node:** Handles natural language input, decision-making, and LLM-based SQL generation.
- **SQL Executor Node:** Executes generated SQL queries and returns results.
- **State Machine:** Manages flow between understanding, generating, and executing.

```mermaid
graph TD;
    A[User Query] --> B[LangGraph Interpreter];
    B --> C[SQL Query Generator];
    C --> D[SQL Executor];
    D --> E[Results to User];
