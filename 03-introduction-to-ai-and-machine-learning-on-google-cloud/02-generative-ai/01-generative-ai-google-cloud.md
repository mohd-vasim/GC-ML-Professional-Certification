# Generative AI on Google Cloud — Notes

> **Source:** `transcriptions/01-generative-ai-google-cloud.md`
> **Module:** 02-generative-ai

---

## Summary

This lesson introduces Generative AI (Gen AI) as a type of AI that creates multimodal content — text, code, images, speech, video, and 3D — and can take autonomous actions through AI agents. Google is positioned as a foundational partner in this space, tracing its lineage from the 2017 Transformer architecture to the 2023 Gemini model. The lesson frames Google's Gen AI offering as a three-layered stack: foundation models, development tools, and end-user applications.

---

## Key Concepts

### What is Generative AI

Gen AI generates content and takes action in response to prompts. Unlike traditional ML, which predicts or classifies, Gen AI produces new artifacts across multiple modalities. It also powers AI agents that can autonomously automate workflows, book travel, schedule appointments, and make decisions — extending AI from passive answers to active execution.

### Google's Gen AI History

Google's research leadership includes the 2017 Transformer paper (the architecture underlying all modern LLMs), followed by Gemini in 2023 — a multimodal model that advances toward Artificial General Intelligence. Recent practical releases include NotebookLM (AI-powered research tool) and Gemini Enterprise (no-code AI agent builder).

### The Three-Layer Gen AI Stack

Google structures its Gen AI platform in three layers: (1) **Foundation models** — large-scale models like Gemini that understand language, images, and video; (2) **Gen AI development tools** — Vertex AI Studio, Agent Builder, and Model Garden for prototyping, deploying agents, and fine-tuning; (3) **Gen AI applications** — Gemini Enterprise and NotebookLM for business users who need no-code solutions. Each layer builds on the one below it.

---

## Google Cloud Products & Tools Mentioned

| Product / Tool | What it does in this context |
|---|---|
| Gemini | Multimodal foundation model launched in 2023; the intelligence layer for most Gen AI on Google Cloud |
| Vertex AI Studio | Development interface to prototype, tune, and deploy Gen AI applications |
| Agent Builder | Tool for designing and managing AI agents |
| Model Garden | Repository of Google and third-party foundation models |
| NotebookLM | AI research assistant for analyzing documents and generating insights |
| Gemini Enterprise | No-code platform for business users to build and host AI agents |

---

## How Concepts Relate

Generative AI requires a foundation model as its core intelligence — in Google's case, primarily Gemini. That model is accessed and customized through development tools like Vertex AI Studio, which abstract the complexity of model training and deployment. Business users who don't need customization can skip straight to applications like Gemini Enterprise or NotebookLM. The three-layer framing is key: knowing which layer a product lives in clarifies its intended user and use case.

---

## Exam Tips

- Gen AI differs from predictive AI: it **generates** new content and can **take action**, not just predict.
- The Transformer architecture (2017, Google) is the foundation of modern LLMs — know this provenance.
- Google's Gen AI stack has exactly **three layers**: foundation models → development → applications.
- Gemini Enterprise is the **no-code** application tier; Vertex AI Studio is the **low-code** development tier.
- AI agents extend Gen AI from conversational to **actionable** — this distinction is exam-relevant.

---

## Questions to Follow Up

- How does Gemini's multimodal capability compare to earlier single-modality models for specific PMLE exam question types?
- What specific capabilities distinguish Agent Builder from Vertex AI Studio for exam scenario questions?
