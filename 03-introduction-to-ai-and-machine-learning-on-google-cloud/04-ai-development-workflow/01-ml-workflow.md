# ML Workflow Overview — Notes

> **Source:** `transcriptions/01-ml-workflow.md`
> **Module:** 04-ai-development-workflow

---

## Summary

This lesson introduces the three-stage ML workflow as a restaurant analogy: data preparation (prep ingredients), model development (experiment with recipes), and model serving (serve and monitor). It emphasizes that the workflow is **iterative, not linear** — you may return to earlier stages based on monitoring results or training feedback. Two paths are available for the workflow: no-code AutoML via the UI, or code-based using Vertex AI Workbench and Vertex AI Pipelines SDKs.

---

## Key Concepts

### The Three-Stage ML Workflow

1. **Data preparation**: upload data (Cloud Storage, BigQuery, or local) and apply feature engineering to prepare it for model training. Data can be real-time streaming or batch; structured (tables, numbers, text) or unstructured (images, videos).
2. **Model development**: iterative cycle of training and evaluation. Train a model, evaluate its performance, then retrain with adjustments — repeated until performance is satisfactory.
3. **Model serving**: deploy the trained model and monitor it in production. If accuracy drops or data drifts, return to earlier stages.

### The Workflow is Iterative

ML workflows don't run linearly once. During training, you may need to return to data to generate better features. During serving/monitoring, you may discover data drift or accuracy degradation requiring retraining. MLOps automates this iteration.

### Two Implementation Paths

- **AutoML via UI**: no-code, builds the workflow through point-and-click; best for users who want to focus on the business problem.
- **Vertex AI Workbench or Colab + Vertex AI Pipelines**: code-based, uses pre-built SDKs as building blocks of a pipeline; best for experienced ML engineers who want automation.

---

## Google Cloud Products & Tools Mentioned

| Product / Tool | What it does in this context |
|---|---|
| Vertex AI | Platform hosting both AutoML (no-code) and Pipeline (code-based) workflow paths |
| Vertex AI Pipelines | SDK toolkit for coding and automating ML workflows (introduced here, detailed later) |
| Vertex AI Workbench | Jupyter-based environment for writing pipeline code |
| Colab | Alternative notebook environment for pipeline coding |
| Cloud Storage | One source for uploading training data |
| BigQuery | Structured data source for training data |

---

## Exam Tips

- **Three stages**: data preparation → model development → model serving — in this order; know this sequence.
- The ML workflow is **iterative**, not one-directional — monitoring can trigger a return to data prep or retraining.
- **Structured data**: tables, numbers, text (easily stored in tables). **Unstructured data**: images, videos (cannot be stored in standard tables).
- The two workflow paths: **AutoML UI** (no-code) vs. **Vertex AI Pipelines with Workbench/Colab** (code-based).
- Data can be **batch** (periodic) or **real-time streaming** — both are supported as input to Vertex AI.

---

## Questions to Follow Up

- How does Vertex AI Pipelines specifically implement the iterative ML workflow — what triggers retraining automatically?
- For the PMLE exam, what is the most common scenario that tests knowledge of the ML workflow stages?
