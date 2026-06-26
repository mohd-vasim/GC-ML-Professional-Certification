# Foundation Models — Notes

> **Source:** `transcriptions/02-foundation-models.md`
> **Module:** 02-generative-ai

---

## Summary

Foundation models are large-scale models trained on massive datasets that form the backbone of all Gen AI applications. This lesson covers how they are created through training, how Google's model family is organized (Gemini for general-purpose, specialty models for specific tasks), and the critical concept of multimodal AI — the ability to process and generate across text, images, audio, and video simultaneously. It also introduces the distinction between pre-trained (horizontal) and fine-tuned (vertical) models, and the three ways developers can interact with these models on Google Cloud.

---

## Key Concepts

### What a Foundation Model Is

A foundation model is created by training on enormous amounts of existing content, resulting in a model with a very large number of parameters (now in the trillions). Parameters represent the model's capacity to learn patterns; more parameters generally means a more capable model. Foundation models are pre-trained for general use and can then be fine-tuned for specific tasks with a much smaller domain-specific dataset.

### Google's Model Family

Google trains two categories of models: general-purpose (Gemini family) and specialized. The Gemini family includes Gemini Pro (complex reasoning), Gemini Flash (speed-optimized, low-latency), and Gemini Flash-Lite (cost-efficient batch processing). Specialized models include Imagen (image generation), Veo (video), and embeddings models (semantic search). This list changes rapidly — always check Google documentation.

### Multimodal AI

A multimodal model like Gemini can process and generate across multiple data types simultaneously: text, images, audio, and video. This is a fundamental shift from earlier single-modality models. Multimodal capability enables complex reasoning about real-world scenarios that involve multiple input types at once — for example, assessing home insurance risk using property photos, weather data, inspection reports, and disaster videos simultaneously.

### Horizontal vs. Vertical AI

Foundation models trained for broad applicability are called **horizontal AI** (e.g., LLMs for content creation, summarization, Q&A). Models fine-tuned on domain-specific data for niche tasks are called **vertical AI** (e.g., a model fine-tuned for disease diagnosis or financial modelling). The K-12 → medical school analogy captures this: general education is pre-training, specialization is fine-tuning.

### Three Ways to Access Models

Developers can interact with Google's foundation models via: (1) **Google Cloud Console UI** — no-code, for exploration; (2) **Gen AI APIs with cURL** — low-code; (3) **SDKs in Python or Java** — code-based, integrated with Colab and Vertex AI Workbench.

---

## Google Cloud Products & Tools Mentioned

| Product / Tool | What it does in this context |
|---|---|
| Gemini Pro | Most capable Gemini variant; ideal for complex reasoning tasks |
| Gemini Flash | Speed- and latency-optimized; suited for high-volume real-time applications |
| Gemini Flash-Lite | Most cost-efficient; for batch tasks where speed is not critical |
| Imagen | Specialized model for image generation |
| Veo | Specialized model for video processing |
| Embeddings models | Used for semantic search and data representation in Gen AI pipelines |
| Colab | Notebook environment for code-based SDK access to foundation models |
| Vertex AI Workbench | Jupyter-based development environment integrated with Vertex AI |

---

## How Concepts Relate

Foundation models sit at the base of the three-layer Gen AI stack; they are what development tools like Vertex AI Studio and applications like Gemini Enterprise are built on top of. Understanding that models can be general-purpose or specialized, and horizontal or vertical, is essential for choosing the right model for a given problem. Multimodality is the key differentiator that makes Gemini broadly applicable — it can substitute for several single-modality specialty models when multiple input types are involved.

---

## Exam Tips

- **Gemini is multimodal** — it's the correct answer for scenarios requiring processing of mixed data types (text + images + video together).
- Gemini Pro = complex tasks; Gemini Flash = low latency / high volume; Gemini Flash-Lite = cost-sensitive batch.
- A **pre-trained model** learns general patterns from large data; a **fine-tuned model** adds domain expertise from smaller labeled data.
- Horizontal AI = general purpose (LLMs); Vertical AI = industry/domain-specific fine-tuned models.
- Three access methods: UI (no-code) → API/cURL (low-code) → SDK (code-based). Know which is appropriate for which user type.
- "The number of parameters has increased from millions to trillions" — this signals model capability growth.

---

## Questions to Follow Up

- When would you choose Imagen over Gemini for image-related tasks — what are the tradeoffs?
- How do embeddings models fit into RAG pipelines, and how does this relate to Vertex AI Feature Store?
