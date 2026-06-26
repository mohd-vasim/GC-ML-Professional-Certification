# Module 1 Quiz — Notes

> **Source:** `transcriptions/08-quiz.md`
> **Module:** 01-ai-foundation
> **Passing score:** 80% (4 out of 5 correct)

---

## Questions & Answers

### Q1. You want to use machine learning to discover the underlying pattern and group a collection of unlabeled photos into different sets. Which should you use?

- Supervised learning, logistic regression
- **✓ Unsupervised learning, cluster analysis**
- Supervised learning, linear regression
- Unsupervised learning, dimensionality reduction

**Why:** The photos are unlabeled (no predefined categories), so this is unsupervised learning. The goal is to group by similarity — that is clustering. K-means cluster analysis is the right tool.

---

### Q2. Which SQL command would you use to create an ML model in BigQuery ML?

- **✓ CREATE MODEL**
- ML.PREDICT
- ML.EVALUATE
- CREATE CLASSIFICATION

**Why:** `CREATE MODEL` trains the model. `ML.EVALUATE` assesses performance. `ML.PREDICT` runs inference. There is no `CREATE CLASSIFICATION` command in BigQuery ML.

---

### Q3. Which Google hardware innovation tailors architecture to meet the computation needs on a domain, such as the matrix multiplication in machine learning?

- CPUs (central processing units)
- DPUs (data processing units)
- **✓ TPUs (tensor processing units)**
- GPUs (graphic processing units)

**Why:** TPUs are Google's domain-specific chips designed specifically for ML workloads (matrix multiplication). CPUs and GPUs are general-purpose. DPUs are not a Google AI chip category in this context.

---

### Q4. What are the three layers of the AI/ML framework on Google Cloud?

- ML development, ML applications, and ML use cases
- **✓ AI infrastructure, AI development, and AI application and solutions**
- Data preparation, data processing, and data analysis
- AI, ML, and generative AI

**Why:** The three-layer Google Cloud AI architecture from this module: (1) AI Infrastructure, (2) AI Development (Vertex AI), (3) AI Applications and Solutions.

---

### Q5. If you have unstructured data, like images, text, and/or audio, which storage option on Google Cloud would you choose?

- Spanner
- **✓ Cloud Storage**
- Bigtable
- Cloud SQL

**Why:** Cloud Storage is Google Cloud's object store, designed for unstructured data (files, images, audio, video). Spanner and Cloud SQL are for structured relational data. Bigtable is for high-throughput NoSQL (semi-structured, time-series).

---

## Exam Takeaways from This Quiz

- Unsupervised + grouping unlabeled data = **clustering** (not dimensionality reduction, which compresses features).
- BigQuery ML uses **`CREATE MODEL`** to train — memorize the three core commands: `CREATE MODEL`, `ML.EVALUATE`, `ML.PREDICT`.
- **TPUs** are the domain-specific hardware answer. GPUs are general-purpose despite being used for ML.
- Google Cloud AI has **three layers**: Infrastructure → Development → Applications.
- **Unstructured data → Cloud Storage**. Never Bigtable (NoSQL wide-column) or Spanner/Cloud SQL (relational).
