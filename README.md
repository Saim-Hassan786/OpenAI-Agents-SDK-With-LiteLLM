# 🧠 OpenAI Agents SDK with LiteLLM

## Overview

This project demonstrates how to build intelligent, agentic applications by combining the **OpenAI Agents SDK** with **LiteLLM**, a lightweight abstraction layer for interacting with various LLM providers. It explores the core theoretical underpinnings of building *agent-based systems* and how **LiteLLM** enables model-agnostic flexibility.

---

## 🧩 What Is an Agent?

In the context of AI, an **agent** is an autonomous entity capable of perceiving its environment, reasoning, and taking actions to achieve specific goals. Agents differ from traditional models in that they:

* Maintain **state** across interactions.
* Make **decisions** based on context and prior knowledge.
* May utilize **tools**, **memory**, and **guardrails**.
* Can be **chained** or **composed** into complex workflows.

> The OpenAI Agents SDK formalizes this architecture, making it easier to implement **modular**, **composable**, and **safe** AI agents.

---

## 🧪 Why LiteLLM?

**LiteLLM** is a powerful wrapper around various language model APIs such as:

* OpenAI (`gpt-4`, `gpt-3.5`)
* Anthropic (`claude`)
* Google (`gemini`)
* Cohere, Mistral, Together.ai, and more

With **LiteLLM**, you gain:

* **Model Interoperability** — Swap models with minimal code change
* **Unified Interface** — Use one API to call multiple providers
* **Observability & Tracing** — Built-in logging and monitoring
* **Cost Control** — Supports rate limiting and budget caps

---

## 🧠 Architecture

```plaintext
User Query
   ↓
[Agent] ← Tools, State, Memory
   ↓
LiteLLM (abstraction layer)
   ↓
LLM Provider (OpenAI / Gemini / Claude)
   ↓
Response → Guardrails → Agent → Final Output
```

### Key Concepts

| Concept            | Description                                                                           |
| ------------------ | ------------------------------------------------------------------------------------- |
| **Agent**          | Logical unit responsible for interpreting inputs and generating meaningful responses. |
| **Runner**         | A utility to run agents synchronously or asynchronously.                              |
| **Guardrails**     | Safety and validation checks that filter or flag harmful or unwanted outputs.         |
| **Output Models**  | `pydantic` classes used to structure and constrain agent outputs.                     |
| **Tool Use**       | Agents can call external APIs or functions (optional).                                |
| **LiteLLM Client** | Injected into the agent to replace default OpenAI calls.                              |

---

## ⚙️ Use Cases

* Customer support agents
* Research assistants
* Workflow automators
* Personal knowledge workers
* Content generators with validation

---

## 📘 Theoretical Insights

### **Model Agnosticism with LiteLLM**

LiteLLM allows agents to be decoupled from any single LLM provider:

* Test prompts across providers (OpenAI vs Gemini vs Claude)
* Fall back to cheaper or faster models when needed
* Avoid vendor lock-in


## ✅ Summary

The combination of **OpenAI Agents SDK** and **LiteLLM** offers a robust framework for building smart, secure, and adaptable AI agents. With model abstraction, output control, and safety guardrails, it empowers developers to bring intelligent agents into real-world applications reliably.


