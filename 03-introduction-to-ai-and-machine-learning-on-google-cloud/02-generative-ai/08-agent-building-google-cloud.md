# Agent Building on Google Cloud — Notes

> **Source:** `transcriptions/08-agent-building-google-cloud.md`
> **Module:** 02-generative-ai

---

## Summary

This lesson provides a practical guide to building AI agents on Google Cloud, navigating the full ecosystem of tools across three tiers: no-code (Gemini Enterprise / Agentspace), low-code (Vertex AI Agent Builder with Agent Garden and customizable templates), and pro-code (Agent Development Kit / ADK for custom development). It also introduces NotebookLM as a no-code personal research agent and presents a decision tree for choosing the right tool based on ease-of-use and flexibility requirements.

---

## Key Concepts

### Google's AI Agent Ecosystem (Three Tiers)

The agent-building ecosystem mirrors the overall Gen AI three-layer stack, but through an agent lens:
- **Foundation layer**: Vertex AI Model Garden — provides the brain (foundation models) for any agent.
- **Development layer**: Vertex AI Agent Builder — low-code and pro-code tooling for developers and ML engineers, includes ADK, Agent Engine, and Agent Garden.
- **Application layer**: Gemini Enterprise (Agentspace) and Customer Engagement Suite — no-code options for business users.

### Gemini Enterprise (Agentspace)

Agentspace is Google's enterprise AI hub combining multimodal search, AI agents, and company data in a secure environment. It breaks down data silos by letting employees query all organizational data formats (documents, images, videos) through a single interface. It also provides pre-built agents and a no-code agent designer for custom workflows. Core capability: intelligent, multimodal search with cited answers.

### NotebookLM

NotebookLM is an AI-powered personal research assistant available as part of Agentspace. It accepts multiple document formats (PDF, text, markdown, audio, Google Drive files, YouTube links) and allows users to ask questions, get summaries, create study guides, and even generate audio podcasts from source materials. It is free to the general public at notebooklm.google.com.

### Vertex AI Agent Builder Components

For custom agent development:
- **Agent Garden**: repository of agent samples, blueprints, and source code to accelerate development.
- **Agent Development Kit (ADK)**: open-source Python framework for building production-ready agents with custom logic and deep integrations.
- **Agent Engine**: fully managed runtime for deploying, scaling, and monitoring agents in production — handles infrastructure.

### Decision Tree for Tool Selection

| Use case | Best tool | User type |
|---|---|---|
| Ready-to-use, minimal setup | Gemini Enterprise / Conversational Agents | Business users |
| Start from a template, some customization | Agent Garden + Agent Builder (low-code) | Data scientists, analysts |
| Full custom logic, deep integrations | ADK / build from scratch (pro-code) | Software/ML engineers |

---

## Google Cloud Products & Tools Mentioned

| Product / Tool | What it does in this context |
|---|---|
| Vertex AI Model Garden | Source of foundation models that power agent reasoning |
| Vertex AI Agent Builder | End-to-end platform for agent development (design to deployment) |
| Agent Development Kit (ADK) | Open-source Python framework for pro-code custom agents |
| Agent Engine | Managed runtime for deploying and scaling agents |
| Agent Garden | Library of reusable agent samples and blueprints |
| Gemini Enterprise / Agentspace | No-code enterprise agent hub with multimodal search |
| Customer Engagement Suite | For building conversational agents like customer service chatbots |
| NotebookLM | No-code personal AI research assistant |

---

## How Concepts Relate

The tool decision hinges on two axes: ease-of-use and flexibility. Gemini Enterprise maximizes ease-of-use but limits flexibility; ADK maximizes flexibility but requires coding expertise. Agent Garden + Agent Builder sits in the middle — pre-built blueprints that can be customized. NotebookLM is a specialized no-code agent for research tasks within Agentspace. For the PMLE exam, matching a scenario's technical requirements and user profile to the appropriate tool tier is the key skill.

---

## Exam Tips

- **Gemini Enterprise** = no-code, business users, out-of-the-box — correct answer for "minimize setup" scenarios.
- **ADK** = pro-code, maximum flexibility, deep integration with legacy systems — correct answer when custom logic and specific integrations are required.
- **Agent Engine** = managed deployment runtime — distinct from Agent Builder (development) and ADK (framework).
- **NotebookLM** is part of Agentspace (Gemini Enterprise ecosystem), not a separate standalone Vertex AI product.
- **Agent Garden** provides reusable blueprints — use it before building from scratch to check if a pre-built component exists.
- Customer Engagement Suite is the correct tool for **conversational agents** like customer service chatbots (not general-purpose agents).

---

## Questions to Follow Up

- Is ADK a Google-proprietary framework or does it support integration with open-source agent frameworks like LangChain or LlamaIndex?
- How does Agent Engine's managed runtime compare to deploying agents on Cloud Run for scalability and cost?
