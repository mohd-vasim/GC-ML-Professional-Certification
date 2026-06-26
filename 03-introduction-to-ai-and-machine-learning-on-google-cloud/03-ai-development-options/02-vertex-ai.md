# Vertex AI — Notes

> **Source:** `transcriptions/02-vertex-ai.md`
> **Module:** 03-ai-development-options

---

## Summary

Vertex AI is Google Cloud's unified AI development platform that brings all components of the ML ecosystem together into one end-to-end workflow — from data ingestion to model deployment and monitoring. This lesson explains why a unified platform was needed (production challenges, ease-of-use problems), what it provides (end-to-end ML pipeline + both Gen AI and predictive AI support), and its four key benefits summarized as the four Ss: seamless, scalable, sustainable, and speedy.

---

## Key Concepts

### Why Vertex AI Was Created

Two categories of challenges motivated Vertex AI: (1) **Production challenges** — scalability, monitoring, continuous integration/delivery/training (only ~50% of enterprise ML projects make it past pilot per Gartner); (2) **Ease-of-use challenges** — many tools require advanced coding, leaving data scientists focused on tool mechanics instead of model configuration; no unified workflow meant difficulty finding the right tools.

### What "Unified Platform" Means

Unified has two dimensions: (1) **End-to-end ML pipeline** — data readiness (upload from Cloud Storage, BigQuery, or local) → feature readiness (Feature Store) → training and hyperparameter tuning → deployment and model monitoring (MLOps); (2) **Both Gen AI and predictive AI** — the same platform supports Vertex AI Studio and Agent Builder (Gen AI) alongside AutoML and Custom Training (predictive AI).

### The Four Ss

- **Seamless**: smooth user experience across the full lifecycle from data upload to production.
- **Scalable**: MLOps handles automated storage and compute scaling in production.
- **Sustainable**: artifacts and features created in Vertex AI are reusable and shareable.
- **Speedy**: produces models with 80% fewer lines of code than competitors.

### Predictive AI on Vertex AI

For predictive ML specifically, Vertex AI offers two paths: AutoML (no-code, UI-driven, focuses on business problem) and Custom Training (code-based, full control via Vertex AI Workbench or Colab). A notable feature is that data scientists can now write SQL in Workbench to bridge BigQuery and Vertex AI seamlessly.

---

## Google Cloud Products & Tools Mentioned

| Product / Tool | What it does in this context |
|---|---|
| Vertex AI | Unified platform that covers the entire ML lifecycle for both Gen AI and predictive AI |
| Vertex AI Feature Store | Centralized store for creating, managing, and sharing ML features |
| Vertex AI Workbench | Jupyter-based notebook for custom training and data science work |
| Colab | Integrated into Vertex AI for coding in a familiar notebook environment |
| Cloud Storage | One of the data ingestion sources for Vertex AI |
| BigQuery | Data source and SQL interface; integrated with Vertex AI Workbench |

---

## How Concepts Relate

Vertex AI is the container that all subsequent lessons' tools live inside. AutoML, Custom Training, Pre-trained APIs, and BigQuery ML are all options within or connected to Vertex AI. Feature Store, Workbench, and Colab are components of the platform. The four Ss distinguish Vertex AI from managing separate, disconnected tools — the MLOps capability (scalable, sustainable) is what enables production-grade ML at scale.

---

## Exam Tips

- Vertex AI supports **both Gen AI and predictive AI** — it is the single unified platform for both.
- The Gartner statistic ("only half of enterprise ML projects get past pilot") motivates why MLOps (and thus Vertex AI) matters.
- **Vertex AI Workbench** = Jupyter Notebook in a managed environment for full lifecycle data science work.
- **Four Ss**: seamless, scalable, sustainable, speedy — know these as the benefits of Vertex AI.
- "80% fewer lines of code than competitors" — Vertex AI's speed advantage for rapid model development.
- Data scientists can write **SQL in Workbench** to connect BigQuery with Vertex AI — bridge between data and ML.

---

## Questions to Follow Up

- How does Vertex AI's Feature Store differ from BigQuery for feature storage — when would you choose one over the other?
- What exactly is the MLOps workflow in Vertex AI Pipelines, and how does it achieve CI/CT/CD?
