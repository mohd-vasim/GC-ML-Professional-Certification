# AI Agents — Notes

> **Source:** `transcriptions/07-ai-agents.md`
> **Module:** 02-generative-ai

---

## Summary

This lesson traces the evolution of Gen AI from conversational chatbots to AI agents capable of taking autonomous action, and then to multi-agent Agentic AI systems. An AI agent is defined by three components — model (brain), tools (hands/feet/senses), and orchestration layer (nervous system) — and is distinguished from foundation models by its ability to access external resources, take action, and learn from feedback. The lesson uses an insurance claims automation use case to ground these concepts.

---

## Key Concepts

### Evolution of Gen AI: Chatbot → Agent → Agentic AI

Foundation models (and tools like Vertex AI Studio) produce conversational AI that answers questions. This is useful but limited: the AI can't access external systems or take action on its own. An **AI agent** extends this by connecting to external applications and databases, taking actions, and receiving feedback. **Agentic AI** goes further — it coordinates multiple agents in a unified system to handle complex, multi-step tasks across domains (e.g., coordinating separate insurance, underwriting, and claims agents).

### What is an AI Agent

An AI agent is an application that combines: an AI model for reasoning, tools for external interaction, and an orchestration layer for coordination. It is **goal-oriented**, **autonomous**, and can operate across multiple steps without human intervention per step.

### The Three Components of an AI Agent

- **Model (brain)**: one or more foundation models that serve as the decision-making center. Handles reasoning, planning, and determining what steps are needed.
- **Tools (hands, feet, senses)**: APIs that connect the agent to the outside world. They perform actions (POST an email, PATCH a ticket) and gather information (GET weather data). Tools use standard HTTP verbs: GET, POST, PATCH, DELETE.
- **Orchestration layer (nervous system)**: the cyclical coordination loop. It takes the model's decisions, uses tools to act, receives feedback from those actions, and feeds results back to the model to inform the next step.

### Agentic AI vs. Single AI Agent

A single AI agent handles a bounded task. Agentic AI systems coordinate multiple agents — each with its own specialization — to solve complex, multi-faceted problems. The orchestration at the agentic AI level is more complex and involves agent-to-agent delegation.

---

## Google Cloud Products & Tools Mentioned

| Product / Tool | What it does in this context |
|---|---|
| Vertex AI Studio | Background context — the Gen AI development tool that inspired the need for agents |
| Agent Builder | Mentioned as the tool for building AI agents on Google Cloud (detailed in next lesson) |

---

## How Concepts Relate

AI agents are the bridge between Gen AI as a content generator and Gen AI as an operational system. The three-component model (model → tools → orchestration) maps directly to the three-layer stack from the module's first lesson: models come from the foundation layer, tools interface with external systems, and the orchestration layer is what Agent Builder and Gemini Enterprise provide. Understanding these components is essential for scenario questions where you must identify which agent component is responsible for a given behavior.

---

## Exam Tips

- **Model = brain** (reasoning/planning); **Tools = hands/feet/senses** (external action/data); **Orchestration = nervous system** (coordination loop).
- Tools interact with external systems via standard APIs: GET (fetch data), POST/PATCH/DELETE (take action).
- Agentic AI ≠ a single AI agent: agentic AI coordinates multiple agents for multi-step complex tasks.
- Foundation models alone cannot connect to external applications — that's the job of the agent architecture.
- The evolution is: chatbot (conversational) → AI agent (actionable) → Agentic AI (multi-agent, autonomous coordination).

---

## Questions to Follow Up

- How does the orchestration layer in an AI agent relate to Vertex AI Pipelines — are they the same concept at different levels?
- For the PMLE exam, what scenarios test knowledge of the model vs. tools vs. orchestration distinction?
