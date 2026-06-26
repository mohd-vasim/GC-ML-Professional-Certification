# Lab Introduction: AutoML Loan Risk Model — Notes

> **Source:** `transcriptions/06-lab-introduction.md`
> **Module:** 04-ai-development-workflow

---

## Summary

This lesson prepares students for the AutoML lab where they build a loan risk classification model using a 2,050-record financial dataset. It provides a deep walkthrough of how to interpret model evaluation results — specifically confusion matrix percentages, the precision-recall curve, and how the confidence threshold setting affects the balance between precision and recall.

---

## Key Concepts

### Lab Context

- Dataset: 2,050 loan records from a financial institution (minimum required for AutoML: 1,000).
- Goal: predict whether a loan applicant will repay (`repay = 0`, positive class) or not repay (`not repay = 1`, negative class).
- Task: walk through all three ML workflow stages (data preparation → model development → model serving) using AutoML.

### Interpreting the Confusion Matrix (Loan Risk Example)

| Metric | Value | Meaning |
|---|---|---|
| True Positive Rate (Recall for "repay") | 100% | Model catches every safe customer — no business opportunity lost. |
| True Negative Rate | 87% | Model correctly identifies 87% of actual defaulters — strong risk management. |
| False Positive Rate | 13% | 13% of actual defaulters are approved — this is the most expensive mistake (financial loss). |
| False Negative Rate | 0% | Zero safe customers are incorrectly rejected — no lost business from turning away good applicants. |

### Confidence Threshold and Precision-Recall Tradeoff

The confidence threshold determines how the model classifies positive cases:

- **Threshold → 0** (lowest): Recall = 100%, Precision = 50%. The model approves everyone — catches all safe customers but half of those approved will actually default.
- **Threshold → 1** (highest): Recall = 1%, Precision = 100%. The model only approves customers it's certain about — 100% of approved applicants actually repay, but 99% of applicants are rejected (massive business loss).
- **The right threshold** depends on the business objective — there is no universal answer.

---

## Google Cloud Products & Tools Mentioned

| Product / Tool | What it does in this context |
|---|---|
| AutoML (Vertex AI) | Tool used in the lab to train the loan risk classification model |
| Vertex AI (evaluation) | Provides the confusion matrix, precision-recall curve, and feature importance visualizations |

---

## Exam Tips

- A **False Positive** in loan risk = model approves a defaulter = **financial loss** — this is the most dangerous error in this context.
- A **False Negative** in loan risk = model rejects a safe borrower = **lost business opportunity**.
- **Higher threshold** → higher precision, lower recall (more conservative approvals).
- **Lower threshold** → higher recall, lower precision (more approvals, more risk).
- AutoML requires a **minimum of 1,000 data points** — this is a testable threshold.
- The precision-recall curve tradeoff is visualized in Vertex AI — adjusting the threshold is done post-training, not during training.

---

## Questions to Follow Up

- Is the 1,000 data point minimum specific to tabular AutoML, or does it apply to image and other data types too?
- How does the PMLE exam frame precision vs. recall tradeoff questions — does it always provide a business context clue?
