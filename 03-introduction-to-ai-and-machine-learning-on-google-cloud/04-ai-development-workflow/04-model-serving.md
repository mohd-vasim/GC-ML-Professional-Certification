# Model Serving — Notes

> **Source:** `transcriptions/04-model-serving.md`
> **Module:** 04-ai-development-workflow

---

## Summary

The third and final stage of the ML workflow — model serving — involves deploying the model to make predictions and then monitoring its ongoing performance. This lesson covers two deployment modes (online endpoint for real-time predictions, batch prediction from the model resource), edge deployment for offline/latency-sensitive scenarios, and introduces Vertex AI Pipelines as the backbone for automated monitoring and workflow orchestration.

---

## Key Concepts

### Model Deployment: Two Options

**Option 1 — Online (real-time) predictions via endpoint**:
- Deploys the model to an endpoint for immediate, low-latency predictions.
- Use when instant results are needed (e.g., real-time product recommendations based on current browsing behavior).
- A model **must be deployed to an endpoint** before serving real-time predictions.

**Option 2 — Batch prediction from model resource**:
- Requests predictions directly from the model without deploying to an endpoint.
- Use when results don't need to be immediate (e.g., weekly marketing campaign targeting based on purchasing behavior).
- **No endpoint deployment required** for batch prediction.

### Edge Deployment

Beyond cloud deployment, models can be deployed to edge devices (off-cloud). Used when: (1) added cloud latency is impractical (e.g., IoT object detection on a manufacturing line); (2) privacy requirements prevent data leaving a local environment; (3) offline functionality is needed.

### Model Monitoring with Vertex AI Pipelines

After deployment, Vertex AI Pipelines automates, monitors, and governs the ML system in a **serverless** manner. It orchestrates the entire workflow and can automatically trigger alerts when metrics fall below predefined thresholds. It is the backbone of MLOps on Vertex AI. Pipelines can be defined with pre-built SDK components in Vertex AI Workbench or Colab Enterprise.

### Model Management

Model management exists throughout the entire ML workflow — it manages the underlying infrastructure so data scientists can focus on **what to do**, not **how to manage the infrastructure**.

---

## Google Cloud Products & Tools Mentioned

| Product / Tool | What it does in this context |
|---|---|
| Vertex AI (endpoint) | Target for deploying models for online/real-time prediction serving |
| Vertex AI Pipelines | Serverless toolkit for automating, monitoring, and governing ML workflows |
| Vertex AI Workbench | Notebook for defining pipeline code with pre-built SDK components |
| Colab Enterprise | Alternative notebook environment for defining Vertex AI pipelines |

---

## Exam Tips

- **Online prediction** = deploy to endpoint = real-time, low latency — use when immediacy matters.
- **Batch prediction** = no endpoint needed = scheduled/periodic — use when immediacy is not required.
- **Edge deployment** = off-cloud = for latency-sensitive, offline, or privacy-constrained scenarios (IoT manufacturing is the canonical example).
- Vertex AI Pipelines is **serverless** — no infrastructure management needed to run monitoring.
- A model deployed to an endpoint can also be further tested in Vertex AI Studio.
- Model management is **infrastructure-level**, distinct from model monitoring (performance-level).

---

## Questions to Follow Up

- What triggers Vertex AI Pipelines to alert on model degradation — is it configured manually via thresholds, or does it use automatic drift detection?
- How does Vertex AI's online prediction endpoint handle traffic spikes — is autoscaling automatic?
