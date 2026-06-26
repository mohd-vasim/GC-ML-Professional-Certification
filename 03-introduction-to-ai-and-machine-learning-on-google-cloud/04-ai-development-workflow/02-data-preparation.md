# Data Preparation — Notes

> **Source:** `transcriptions/02-data-preparation.md`
> **Module:** 04-ai-development-workflow

---

## Summary

The first stage of the ML workflow — data preparation — consists of data upload and feature engineering. This lesson focuses on how data is uploaded to AutoML, what objectives AutoML can solve (regression, classification, forecasting for tabular data), and the role of Vertex AI Feature Store as a centralized, reusable feature repository for both training and serving. It also notes that Feature Store now supports Gen AI embeddings for real-time similarity retrieval.

---

## Key Concepts

### Data Upload and Supported Objectives

AutoML accepts data from Cloud Storage, BigQuery, or local machines. For tabular data, AutoML supports three prediction objectives: **regression** (continuous value prediction), **classification** (categorical output), and **forecasting** (time-series future value prediction). Forecasting is especially important for industries like retail.

### Feature Engineering

Raw data must be transformed before training — this is feature engineering. A **feature** is an independent variable (a column in a table) that contributes to the prediction. Feature engineering is tedious and error-prone when done manually, especially when features come from multiple sources.

### Vertex AI Feature Store

A centralized repository for managing, serving, and sharing ML features. Key capabilities:
- Aggregates features from multiple BigQuery sources.
- Supports both **online (real-time, low latency)** and **offline (batch)** serving.
- **Shareable**: features are reused across projects and teams — reduces duplicated effort.
- **Reusable**: saves time by preventing teams from recreating the same features.
- **Scalable**: automatically scales to handle low-latency serving.
- **Easy to use**: built on a navigable UI.
- **Gen AI ready**: manages and serves **embeddings** (vector representations used in Gen AI) and supports real-time similarity retrieval.

### Feature Store Workflow (Online Serving)

1. Prepare data source in BigQuery.
2. (Optional) Register data sources as feature groups and features.
3. Create a feature view to define which features to copy into the online store.
4. Serve feature values online from the feature view.

---

## Google Cloud Products & Tools Mentioned

| Product / Tool | What it does in this context |
|---|---|
| Vertex AI Feature Store | Centralized store for managing, sharing, and serving ML features (online and offline) |
| BigQuery | Primary data source for Feature Store; also direct source for AutoML data upload |
| AutoML | The no-code tool consuming the uploaded and feature-engineered data |
| Cloud Storage | Alternative data upload source for AutoML |

---

## Exam Tips

- Vertex AI Feature Store supports **both online (real-time) and offline (batch) serving** — know when each is needed.
- Feature Store benefits: shareable, reusable, scalable, easy to use — the "four benefits" are testable.
- Feature Store is now **Gen AI ready** — it serves embeddings and supports real-time similarity search.
- AutoML supports tabular objectives: **regression, classification, forecasting** — not image, text, or video objectives (those are Custom Training).
- A **feature** = independent variable = column in a table — the raw data element that the model learns from.
- Feature Store aggregates from BigQuery and serves features at low latency — no manual management of feature copies for training vs. serving.

---

## Questions to Follow Up

- How does Vertex AI Feature Store relate to the concept of a training-serving skew — does it prevent skew by design?
- For embeddings stored in Feature Store, what retrieval mechanism is used for real-time similarity search — is it Vertex AI Vector Search?
