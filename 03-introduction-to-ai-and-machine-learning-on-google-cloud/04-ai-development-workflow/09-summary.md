# AI Development Workflow Module — Summary Notes

> **Source:** `transcriptions/09-summary.md`
> **Module:** 04-ai-development-workflow

---

## Summary

This module covered the three-stage ML workflow end-to-end: data preparation (upload + feature engineering), model development (training + evaluation), and model serving (deployment + monitoring). Two paths to implement the workflow were highlighted: no-code via AutoML UI and code-based via Vertex AI Pipelines with pre-built SDKs. MLOps via Vertex AI Pipelines enables the code-based path to achieve continuous integration, training, and delivery — automating the iterative ML lifecycle in production.

---

## Key Concepts

### The Three Stages (Recap with Restaurant Analogy)

- **Data preparation** = gather and prep ingredients (upload data + feature engineering with Feature Store).
- **Model development** = experiment with recipes (train + evaluate using confusion matrix, precision/recall, feature importance).
- **Model serving** = serve to customers (deploy to endpoint or batch + monitor with Vertex AI Pipelines).

### Two Build Paths (Recap)

- **AutoML UI**: practiced in the lab, no-code, good for exploring the workflow manually.
- **Vertex AI Pipelines with SDKs**: code-based, enables CI/CT/CD for production automation.

---

## Exam Tips

- The three-stage ML workflow sequence is always: **data preparation → model development → model serving**.
- The workflow is **iterative** — monitoring results in model serving can send you back to data prep or retraining.
- **AutoML lab** = builds a loan risk model end-to-end — the practical validation of all three stages.
- Vertex AI Pipelines with SDKs is the path to **production automation** — not AutoML UI, which is manual.
