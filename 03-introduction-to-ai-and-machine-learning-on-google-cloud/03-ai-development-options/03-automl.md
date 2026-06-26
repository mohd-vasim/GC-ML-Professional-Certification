# AutoML — Notes

> **Source:** `transcriptions/03-automl.md`
> **Module:** 03-ai-development-options

---

## Summary

AutoML (Automated Machine Learning) automates the entire ML development pipeline — from data preprocessing through model training, tuning, and deployment — using a no-code UI. This lesson explains the four phases of AutoML's internal process and the two key technologies that power it: neural architecture search (to find optimal model architectures automatically) and transfer learning (to accelerate search using pre-trained models as starting points).

---

## Key Concepts

### What AutoML Does

AutoML removes the manual work of ML development: repeated data feature engineering, trying different models, tuning parameters. First announced in 2018 and embedded in Vertex AI since 2021, AutoML automates the pipeline from preprocessing to training and deployment, targeting data scientists and business users who want results without architecture expertise.

### The Four Phases of AutoML

1. **Data processing**: AutoML auto-converts diverse data types (numbers, datetime, text, categories, arrays, nested fields) into model-ready formats.
2. **Model search and parameter tuning**: Uses neural architecture search and transfer learning (see below) to find the best model automatically.
3. **Model assembly**: Takes the top-performing models from phase 2 (typically ~10, depending on training budget) and assembles them into an ensemble.
4. **Prediction**: Serves predictions using the assembled ensemble.

### Neural Architecture Search

AutoML tries different model architectures and compares their performance to find the best fit for a given dataset automatically. This replaces the manual process of a data scientist iterating through model choices.

### Transfer Learning

AutoML uses pre-trained models as starting points when searching for the best architecture. Because the model doesn't start from scratch, it reaches higher accuracy faster and with less data. LLMs are a canonical example: pre-trained on general-purpose language tasks, then fine-tuned on smaller domain datasets. Transfer learning is particularly powerful for smaller datasets.

### Model Ensemble

AutoML does not rely on one single model — it uses the top ~10 models (depending on training budget) and averages (or otherwise combines) their predictions. Ensembling multiple models significantly improves prediction accuracy compared to any single model.

---

## Google Cloud Products & Tools Mentioned

| Product / Tool | What it does in this context |
|---|---|
| AutoML (Vertex AI) | No-code UI for training custom ML models using neural architecture search and transfer learning |
| Vertex AI | The platform AutoML is embedded in since 2021 |

---

## How Concepts Relate

AutoML's four phases map directly to the manual ML workflow (data prep → model training → evaluation → serving) but automate each step. The two underlying technologies — neural architecture search and transfer learning — are what make automation trustworthy: search finds the best model objectively, while transfer learning makes the process fast and data-efficient. The ensemble output is why AutoML can match or exceed hand-tuned models for many tasks.

---

## Exam Tips

- AutoML was first announced **January 2018** and embedded in Vertex AI **since 2021**.
- Two key technologies: **neural architecture search** (finds best model) + **transfer learning** (speeds search using pre-trained models).
- AutoML uses an **ensemble of ~10 top models**, not a single model — this improves accuracy.
- AutoML provides a **no-code, point-and-click UI** — no coding or architecture knowledge required.
- Transfer learning is why AutoML can achieve high accuracy with **smaller datasets and less compute time**.
- AutoML automates the pipeline: data preprocessing → model search/tuning → ensemble → prediction.

---

## Questions to Follow Up

- How does AutoML's neural architecture search compare to hyperparameter tuning — are they the same operation or distinct?
- When would you choose AutoML over Custom Training if you have sufficient data and ML expertise — what are the hidden costs/benefits of each?
