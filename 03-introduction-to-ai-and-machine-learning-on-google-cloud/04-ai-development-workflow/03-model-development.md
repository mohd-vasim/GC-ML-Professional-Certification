# Model Development — Notes

> **Source:** `transcriptions/03-model-development.md`
> **Module:** 04-ai-development-workflow

---

## Summary

The second stage of the ML workflow — model development — involves training the model and evaluating its performance in a cycle until results are satisfactory. This lesson covers how to configure an AutoML training job, introduces the confusion matrix as the foundation of classification evaluation, explains recall and precision as complementary metrics with a precision-recall tradeoff, and introduces feature importance and Explainable AI as Vertex AI evaluation capabilities.

---

## Key Concepts

### Setting Up a Training Job in AutoML

Key configuration steps: (1) specify the **training method** — AutoML or custom training; (2) select the **training objective** — what problem to solve (e.g., regression, classification) based on data type; (3) choose the **target column** for supervised learning problems; (4) optionally exclude features or transform data types in Training Options; (5) specify budget and pricing, then start training. AutoML uses neural architecture search and transfer learning to find the best model.

### Confusion Matrix

A confusion matrix is a 2×2 table (for binary classification) showing combinations of predicted vs. actual labels:
- **True Positive (TP)**: predicted positive, actually positive (e.g., model says "cat", it is a cat).
- **True Negative (TN)**: predicted negative, actually negative (model says "not cat", it isn't).
- **False Positive (FP)** = Type I error: predicted positive, actually negative (model says "cat", it isn't).
- **False Negative (FN)** = Type II error: predicted negative, actually positive (model says "not cat", it is).

### Recall

**Recall** = TP / (TP + FN)

Looks at all actual positive cases and asks: how many did we correctly predict? Use when **missing a positive is costly** — e.g., a hospital trying to catch as many cancer cases as possible.

### Precision

**Precision** = TP / (TP + FP)

Looks at all cases predicted as positive and asks: how many are actually positive? Use when **false alarms are costly** — e.g., spam filter where you don't want to block legitimate emails.

### Precision-Recall Tradeoff

Precision and recall are in tension: optimizing for one typically degrades the other. Vertex AI visualizes the precision-recall curve, allowing you to adjust the confidence threshold based on your use case.

### Feature Importance and Explainable AI

Feature importance is displayed as a bar chart in Vertex AI, showing how much each feature contributes to predictions. Longer bar = more important feature. This is one component of Vertex AI's **Explainable AI** — a set of tools and frameworks for understanding and interpreting ML model predictions.

---

## Google Cloud Products & Tools Mentioned

| Product / Tool | What it does in this context |
|---|---|
| Vertex AI (AutoML) | Trains classification, regression, and forecasting models with automated architecture search |
| Vertex AI Explainable AI | Framework for interpreting model predictions; includes feature importance visualization |

---

## Exam Tips

- **Recall** = catch everything (minimize false negatives) — use in high-stakes detection (cancer, fraud detection where missing a case is worse than a false alarm).
- **Precision** = only flag what you're sure of (minimize false positives) — use in spam filtering, content moderation where false alarms have costs.
- **False Positive = Type I error**; **False Negative = Type II error** — know both names.
- Confusion matrix formulas: Recall = TP/(TP+FN); Precision = TP/(TP+FP).
- **Feature importance** indicates which inputs most influence predictions — used for model explainability and feature selection.
- Explainable AI is a Vertex AI built-in capability — not a separate product.

---

## Questions to Follow Up

- How does the PMLE exam test precision vs. recall tradeoff — are there scenario-based questions about which metric to prioritize?
- What other Explainable AI techniques does Vertex AI provide beyond feature importance (e.g., SHAP values, integrated gradients)?
