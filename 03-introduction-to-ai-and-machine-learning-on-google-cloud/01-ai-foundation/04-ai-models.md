# AI Model Categories — Notes

> **Source:** `transcriptions/04-ai-models.md`
> **Module:** 01-ai-foundation

---

## Summary

This lesson establishes the vocabulary needed to talk about ML models: AI as the umbrella term, machine learning as its main sub-discipline, deep learning as a subset of ML, and generative AI as the newest branch that sits on top of deep learning. It then goes deep on the supervised vs. unsupervised split, walking through classification and regression (supervised) and clustering, association, and dimensionality reduction (unsupervised), with worked examples and multiple-choice knowledge checks.

---

## Key Concepts

### The AI / ML / Deep Learning / GenAI Hierarchy

These four terms are often used interchangeably but describe a nesting relationship:
- **Artificial Intelligence (AI)** — any system where a computer mimics human intelligence (robots, self-driving cars).
- **Machine Learning (ML)** — a subset of AI where computers learn patterns from data instead of being explicitly programmed.
- **Deep Learning (Deep Neural Networks)** — a subset of ML that adds hidden layers between input and output, enabling the model to learn at much greater depth and handle unstructured data like images and audio.
- **Generative AI (GenAI)** — a subset of deep learning that creates content and performs tasks; powered by foundation models like LLMs, which are a type of deep learning model.

### Supervised vs. Unsupervised Learning

The core split in ML:

**Supervised learning** requires labeled training data — each example comes with the correct answer. The model learns to map inputs to that answer. It is task-driven and goal-oriented (you define what you want predicted). Two flavors:
- **Classification** — predict a category (dog or cat? buy or not buy?). Models: logistic regression, decision trees, neural networks.
- **Regression** — predict a continuous number (future sales amount, house price). Model: linear regression.

**Unsupervised learning** uses unlabeled data — no correct answers provided. The model discovers structure on its own. It is data-driven and pattern-oriented. Three flavors:
- **Clustering** — group data points by similarity (customer segments). Model: k-means clustering.
- **Association** — find co-occurrence relationships (product A often bought with product B). Algorithm: Apriori.
- **Dimensionality Reduction** — compress many features into fewer, more meaningful ones while preserving information (combining age, driving record, car type into a single insurance risk score). Technique: Principal Component Analysis (PCA).

### Worked Decision Framework

A quick test from the transcript to internalize the difference:
- "Predict customer spending based on purchase history" → **Supervised** (you have historical labeled spend data) → **Regression** (continuous number) → **Linear regression** model.
- "Identify customer segmentation without predefined categories" → **Unsupervised** (no labels, discover structure) → **Clustering** → **K-means** model.

---

## Google Cloud Products & Tools Mentioned

| Product / Tool | What it does in this context |
|---|---|
| BigQuery ML | Contains built-in implementations of logistic regression, linear regression, k-means clustering, and time-series models |
| AutoML | Trains ML models on your data with minimal code; supports classification and regression |
| Custom Training (Vertex AI) | Build and train models from scratch when pre-built options don't fit |

---

## How Concepts Relate

The supervised/unsupervised distinction flows directly into BigQuery ML, AutoML, and Custom Training later in the course — each of those tools supports specific model types, and choosing the right one starts here. Understanding that regression predicts numbers while classification predicts categories, for instance, is what lets you pick the correct model type in BigQuery ML's `CREATE MODEL` statement. Deep learning (and GenAI on top of it) is introduced here conceptually but covered in detail in Module 2; this lesson just establishes that it sits within the ML hierarchy.

---

## Exam Tips

- **AI ⊃ ML ⊃ Deep Learning ⊃ GenAI** — know this nesting. GenAI is not separate from ML; it builds on deep learning.
- **Supervised = labeled data, task-driven. Unsupervised = unlabeled data, data-driven.**
- **Classification = categorical output** (logistic regression). **Regression = numeric output** (linear regression). Don't confuse these — a common exam trap.
- **Clustering = k-means. Association = Apriori. Dimensionality reduction = PCA.** These are the canonical model-to-problem pairings.
- **Logistic regression ≠ regression.** Despite the name, logistic regression solves classification problems (predicts a probability between 0 and 1, then thresholds to a class).

---

## Questions to Follow Up

- What are the BigQuery ML model types beyond logistic regression, linear regression, and k-means? Does it support deep neural networks natively?
- How does AutoML choose between model types internally — does it try multiple and pick the best?
- Where does reinforcement learning fit in this hierarchy? It isn't mentioned here but may appear on the PMLE exam.
