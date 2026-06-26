# Generative AI Module — Summary Notes

> **Source:** `transcriptions/09-summary.md`
> **Module:** 02-generative-ai

---

## Summary

This module covered Google's comprehensive Gen AI development architecture across three layers: foundation models, development tools, and applications. Starting with foundation models (Gemini family, specialty models, multimodal capabilities), it progressed through Vertex AI Studio's prompt-to-production lifecycle (prompt design, engineering, evaluation, deployment, and tuning), then introduced AI agents as the next evolution of Gen AI — moving from conversational to actionable AI — and concluded with a practical guide to building agents on Google Cloud using tools from Gemini Enterprise (no-code) to Vertex AI Agent Builder and ADK (pro-code).

---

## Key Concepts

### Three-Layer Gen AI Stack (Recap)

Foundation models → Gen AI development (Vertex AI Studio, Agent Builder, Model Garden) → Gen AI applications (Gemini Enterprise, NotebookLM). Each layer serves a different user and purpose.

### Prompt-to-Production Lifecycle (Recap)

Two halves: (1) Prompt engineering — design, evaluate, refine using Vertex AI Studio features (templates, parameters: temperature/Top K/Top P, side-by-side comparison); (2) Deployment and tuning — auto-generated code via SDK/API, Cloud Run deployment, grounding/RAG for accuracy, model tuning options (prompt design → parameter-efficient → full fine-tuning).

### AI Agents (Recap)

Three components: model (brain), tools (external action), orchestration layer (coordination loop). Evolution: chatbot → AI agent → Agentic AI (multi-agent coordination).

### Agent Building Decision Tree (Recap)

No-code (Gemini Enterprise) → low-code templates (Agent Garden + Builder) → pro-code custom (ADK). Tool choice driven by user type and required flexibility.

---

## Exam Tips

- The module's key services to know: Vertex AI Studio, Vertex AI Agent Builder, ADK, Agent Engine, Gemini Enterprise, NotebookLM, Model Garden.
- Grounding addresses model currency (outdated data); tuning addresses model competence (domain behavior).
- AI agents require three components — any exam question asking which component "manages sequence of actions" = orchestration layer; "connects to resources" = tools; "comprehends logic" = model.
- Full fine-tuning requires the most compute; prompt design requires the least (and doesn't change parameters).
