# AI on Google Cloud — Notes

> **Source:** `transcriptions/02-ai-on-google-cloud.md`
> **Module:** 01-ai-foundation

---

## Summary

This lesson explains why Google is a credible AI partner (track record with Search, Maps, and Workspace; leadership in generative AI research; commitment to responsible AI) and then draws a clear distinction between predictive AI and generative AI. It provides a practical decision framework for choosing between the two, and introduces Google Cloud's three-layer AI architecture — infrastructure, development, and applications — that the rest of the course is built around.

---

## Key Concepts

### Predictive AI (Traditional / Discriminative AI)

Predictive AI learns patterns from existing labeled or historical data in order to classify or forecast. It is the workhorse of classical machine learning: given past customer purchases, predict whether a new customer will buy. It answers "what will happen?" or "what category does this belong to?" The key constraint is that it works best when you already have representative historical data with known outcomes.

### Generative AI

Generative AI goes further than prediction — it creates net-new content (text, image, video, code) that mirrors the style and patterns it was trained on. It also enables taking action, not just producing a number. Where predictive AI says "this customer is 80% likely to churn," generative AI can write the retention email. It doesn't just analyze; it creates and acts.

### When to Use Each

The lesson offers a simple decision tree: if your goal is **forecasting or classification**, start with predictive AI. If your goal is **content generation, summarization, or automation**, use generative AI. Critically, the two can be chained: predictive AI produces a structured result (a customer segment score), which becomes the context fed into a generative AI prompt. Neither is universally better — the right tool depends on the business outcome you're targeting.

### Google Cloud Three-Layer AI Architecture

Google Cloud's AI stack has three layers:
- **AI Infrastructure** — compute (CPUs, GPUs, TPUs), networking, storage.
- **AI Development** — Vertex AI as the central platform, powered by foundation models like Gemini; integrates with BigQuery for data access.
- **AI Applications & Solutions** — out-of-the-box tools for business users who don't write code (e.g., pre-built APIs, Agent Builder).

This layering means you can engage at whatever level of abstraction fits your skills: use a pre-built API, fine-tune a foundation model, or build a custom model from scratch.

---

## Google Cloud Products & Tools Mentioned

| Product / Tool | What it does in this context |
|---|---|
| Vertex AI | End-to-end AI development platform; the central hub of the development layer |
| Gemini | Google's foundation model powering generative capabilities within Vertex AI |
| BigQuery | Data warehouse that integrates with Vertex AI for seamless data-to-AI workflows |
| NotebookLM | AI-powered research/note tool; cited as an example of Google leveraging its own AI |

---

## How Concepts Relate

The predictive vs. generative distinction is not just academic — it maps directly to the two halves of the course (modules 3–4 cover predictive AI; module 2 covers generative AI). Both types of AI sit on top of the same Google Cloud infrastructure layer and are built and deployed through the same Vertex AI development layer. Understanding where a business problem falls on the predictive/generative spectrum is the first decision an ML engineer makes before choosing tools, models, or training strategies.

---

## Exam Tips

- **Predictive AI = analyzes and predicts** from historical data. **Generative AI = creates new content and takes action.**
- You can combine both: predictive AI output → generative AI prompt. This is a common real-world pattern worth remembering for scenario questions.
- The three Google Cloud AI layers in order: **AI Infrastructure → AI Development → AI Applications & Solutions**. Vertex AI lives in the development layer.
- Responsible AI is a first-class concern for Google — expect questions on AI principles and ethics in the PMLE exam.

---

## Questions to Follow Up

- Where exactly does AutoML sit in the three-layer architecture? Is it part of the development layer (Vertex AI) or the applications layer?
- What specific responsible AI principles does Google publish, and which of those are testable on the PMLE exam?
- Can Gemini be used independently of Vertex AI, or is Vertex AI always the access point on Google Cloud?
