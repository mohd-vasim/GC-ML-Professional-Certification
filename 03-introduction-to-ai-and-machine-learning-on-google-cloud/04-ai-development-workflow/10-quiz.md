# AI Development Workflow Module — Quiz Notes

> **Source:** `transcriptions/10-quiz.md`
> **Module:** 04-ai-development-workflow

---

## Questions and Answers

**1. A farm detects defective apples — goal is to identify only the apples that are actually bad so no good apples are wasted. Which metric?**

- Confusion matrix
- ✓ **Precision**
- Recall
- Feature importance

*Why correct:* The goal is "only flag apples that are actually bad" — minimize false positives (mislabeling good apples as bad). Precision = TP/(TP+FP) — focuses on ensuring all flagged cases are truly positive.

---

**2. A hospital wants to pre-diagnose cancer — goal is to identify as many potential cases as possible. Which metric?**

- Confusion matrix
- Feature importance
- Precision
- ✓ **Recall**

*Why correct:* The goal is to catch every potential cancer case, even at the cost of false alarms. Recall = TP/(TP+FN) — maximizes true positive detection. Missing a case (false negative) is more costly than a false alarm.

---

**3. Which provides a toolkit to automate, monitor, and govern ML systems by orchestrating the workflow in a serverless manner?**

- Explainable AI
- Responsible AI
- ✓ **Vertex AI Pipelines**
- Vertex AI Feature Store

*Why correct:* Vertex AI Pipelines is explicitly described as the backbone of MLOps on Vertex AI — it automates, monitors, and governs ML systems serverlessly. Feature Store manages features; Explainable AI handles interpretability; neither orchestrates the full ML pipeline.

---

**4. Select the correct machine learning workflow order.**

- Model training, data preparation, model serving
- Data preparation, model evaluation, model training
- ✓ **Data preparation, model development, model serving**
- Model serving, data preparation, model development

*Why correct:* The three canonical stages in order are data preparation → model development (which includes training and evaluation) → model serving (deployment and monitoring).

---

**5. Which stage of the ML workflow includes model training and evaluation?**

- Model serving
- Data preparation
- ✓ **Model development**

*Why correct:* Model development is the stage where the model is trained and evaluated iteratively. Data preparation handles feature engineering; model serving handles deployment and monitoring.
