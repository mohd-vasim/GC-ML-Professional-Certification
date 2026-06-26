# BigQuery ML — Notes

> **Source:** `transcriptions/05-bigquery-ml.md`
> **Module:** 01-ai-foundation

---

## Summary

This lesson makes the transition from theory to practice by introducing BigQuery ML — the capability within BigQuery that lets you build, train, evaluate, and predict with ML models using only SQL commands. It walks through all five phases of a BigQuery ML project (ETL → feature selection → model creation → evaluation → prediction) with the specific SQL commands for each phase. The motivating example is predicting whether an e-commerce visitor will make a future purchase.

---

## Key Concepts

### BigQuery: Two Services in One

BigQuery is not just a storage tool — it is simultaneously a **fully managed data warehouse** (storing large structured and semi-structured datasets) and a **fast SQL analytical engine**. These two services are connected by Google's internal high-speed network, which is what enables BigQuery to independently scale compute and storage. Originally a data warehouse, it has evolved to support the full data-to-AI lifecycle, including ML model training and prediction.

### Why BigQuery ML Exists

Traditional ML workflows require exporting data from your warehouse, importing it into a separate ML environment, then managing model training, evaluation, and deployment as separate steps. BigQuery ML collapses this into a single SQL interface: your data never leaves BigQuery, and you use `CREATE MODEL` and a handful of other SQL commands to do everything. This eliminates data movement overhead and makes ML accessible to data analysts who know SQL but not Python or TensorFlow.

### The Five Phases of a BigQuery ML Project

1. **ETL** — Load your raw data into BigQuery. If you're already using Google products (e.g., Google Analytics, YouTube), use built-in connectors. Enrich with joins.
2. **Feature Selection & Preprocessing** — Use SQL to construct your training dataset. BigQuery ML handles some preprocessing automatically, e.g., **one-hot encoding** of categorical variables (converting text categories like "red", "blue" into numeric binary columns that models can consume).
3. **Create Model** — Use `CREATE MODEL` and specify the model type and label column. The label column is what you're predicting.
4. **Evaluate** — Use `ML.EVALUATE` to measure model performance on a held-out evaluation set. Metrics include accuracy, precision, and recall.
5. **Predict** — Use `ML.PREDICT` to run the model on new data. The output includes the predicted label (prefixed with "predicted_") and a confidence score.

### Choosing the Right Model Type

The same supervised/unsupervised logic from the previous lesson applies here. For the e-commerce example (will this visitor buy?), the answer is **logistic regression** because:
- It's supervised (you have historical data with known purchase outcomes as labels).
- It's a classification problem (buy = yes or no, not a continuous number).

BigQuery ML also supports linear regression, k-means, and time-series forecasting models. The lesson advises starting with simpler models (logistic/linear regression) as a baseline benchmark before trying complex models like DNNs, which are slower and more resource-intensive to train.

### MLOps Support in BigQuery ML

BigQuery ML isn't just for prototyping — it supports MLOps, the practice of operationalizing ML models. This means you can deploy, monitor, and manage models through BigQuery ML as part of a production workflow.

---

## Google Cloud Products & Tools Mentioned

| Product / Tool | What it does in this context |
|---|---|
| BigQuery ML | Runs ML model lifecycle (train, evaluate, predict) entirely in SQL within BigQuery |
| Gemini Code Assist | AI coding assistant used in the lab to explain, generate, and debug SQL for BigQuery ML |

---

## How Concepts Relate

BigQuery ML is the practical application of the model taxonomy from the previous lesson. The choice of `logistic_reg` vs `linear_reg` in the `CREATE MODEL` statement directly maps to "classification vs regression." The five-phase workflow mirrors the high-level ML lifecycle introduced in the course overview. BigQuery ML also connects to the MLOps theme that runs through the later courses in the PMLE path — you'll see these same concepts (evaluate, monitor, retrain) again at scale in Vertex AI.

---

## Exam Tips

- **`CREATE MODEL`** — creates and trains a BigQuery ML model.
- **`ML.EVALUATE`** — evaluates model performance on an evaluation dataset.
- **`ML.PREDICT`** — runs inference; output field is prefixed with `predicted_`.
- BigQuery ML's automatic preprocessing includes **one-hot encoding** of categorical variables — you don't need to do this manually.
- BigQuery provides **two services**: managed data warehouse storage + SQL analytical engine, connected by a high-speed internal network.
- **Start simple** — logistic/linear regression as baselines before moving to DNNs.
- BigQuery ML supports **MLOps**: deploy, monitor, and manage models in production.

---

## Questions to Follow Up

- What evaluation metrics does `ML.EVALUATE` return for logistic regression? (Accuracy, precision, recall — what else? AUC-ROC?)
- Does BigQuery ML support hyperparameter tuning automatically, or do you need to iterate manually?
- What is the practical limit on dataset size for BigQuery ML training, and when should you graduate to Vertex AI Custom Training?
