# AI Development Options Module — Summary Notes

> **Source:** `transcriptions/08-summary.md`
> **Module:** 03-ai-development-options

---

## Summary

This module answered the question: "What are your options for building an AI project or ML model on Google Cloud?" The answer is a spectrum: no-code out-of-the-box solutions at one end, DIY code-based approaches at the other. Vertex AI serves as the unified platform for all options. The three main paths covered were AutoML (no- to low-code, your own data, automated training), Pre-trained APIs (low-code, no training data required, Google's pre-built models), and Custom Training (code-based, full control via Python/JAX/Workbench).

---

## Key Concepts

### The Three Core Options (Recap)

- **AutoML**: no- to low-code tool within Vertex AI; automates ML development from data preparation to model training and serving using your own training data.
- **Pre-trained APIs**: ready-made solutions using Google's pre-trained models; no training data needed.
- **Custom Training**: code-based DIY approach using Python, JAX, and Vertex AI Workbench for full control over the ML workflow.

---

## Exam Tips

- All three options live within or connect to **Vertex AI** — it is the unified platform for all ML development on Google Cloud.
- **AutoML** = your own data + no-code UI = automated pipeline.
- **Pre-trained APIs** = no training data + minimal code = immediate AI capability.
- **Custom Training** = full code + full control = most flexibility, most effort.
- The next module (04-ai-development-workflow) covers the step-by-step ML workflow for building a model — the "how" that follows the "what options exist" of this module.
