# Custom Training — Notes

> **Source:** `transcriptions/05-custom-training.md`
> **Module:** 03-ai-development-options

---

## Summary

Custom training is the code-based, full-control approach to building ML models on Vertex AI, used when AutoML's automated capabilities are insufficient. This lesson covers the choice between pre-built and custom containers, the two primary development environments (Vertex AI Workbench and Colab Enterprise), popular ML libraries (TensorFlow, scikit-learn, PyTorch), and a walkthrough of the three-step TensorFlow/Keras model training workflow: create model → compile → fit.

---

## Key Concepts

### Pre-built vs. Custom Container

Before writing any code, you must choose your training environment:
- **Pre-built container**: like a furnished kitchen — includes a pre-configured runtime (Python, TensorFlow, PyTorch) without needing to specify infrastructure details. Best when standard frameworks and compute are sufficient.
- **Custom container**: like an empty room — you define every detail (environment, machine type, disks). Best when you need precise control over the runtime environment.

### Development Environments

- **Vertex AI Workbench**: Jupyter Notebook in a managed, single development environment that supports the full data science workflow (explore → train → deploy). Fully managed by Google Cloud.
- **Colab Enterprise**: Integrated into Vertex AI since 2023, allows data scientists to code in the familiar Colab interface within Vertex AI's managed environment.

### ML Libraries

You don't code ML from scratch — you use libraries:
- **TensorFlow**: Google-supported, end-to-end ML platform with hierarchical APIs from low-level C++ operations to high-level Keras. Fully hosted on Vertex AI.
- **Keras** (`tf.keras`): High-level TensorFlow API that hides implementation details and auto-deploys training. The most commonly used layer.
- **scikit-learn** / **PyTorch**: Popular open-source libraries also supported.
- **JAX**: Newer Google framework for high-performance numerical computation — flexible and applicable to both research and production.

### TensorFlow/Keras Three-Step Workflow

1. **Create**: `tf.keras.Sequential` — define layers of a neural network.
2. **Compile**: `model.compile(loss=..., optimizer=...)` — specify the loss function and optimizer.
3. **Train**: `model.fit(X_train, y_train, epochs=...)` — run training iterations.

After training, the model can be deployed to an endpoint for predictions.

---

## Google Cloud Products & Tools Mentioned

| Product / Tool | What it does in this context |
|---|---|
| Vertex AI Workbench | Managed Jupyter environment for full-lifecycle data science and custom training |
| Colab Enterprise | Familiar Colab notebook environment integrated into Vertex AI |
| TensorFlow | End-to-end ML platform supported by Google; runs on Vertex AI with managed service |
| Keras (`tf.keras`) | High-level TensorFlow API for model creation — the standard interface for custom training |
| JAX | High-performance computation library; Google's newer framework for research and production |

---

## How Concepts Relate

Custom training is the most flexible but most demanding option in the development spectrum. The choice between pre-built and custom containers mirrors the overall spectrum: pre-built is simpler (like AutoML environments), custom is for specialized needs. TensorFlow's layered architecture (hardware → low-level Python → model libraries → Keras) illustrates why Vertex AI can offer "managed service" at every abstraction level — it hosts the full stack. JAX represents the cutting edge for researchers who need more control than Keras.

---

## Exam Tips

- **Pre-built container** = standard framework (TensorFlow, PyTorch, Python) without infrastructure config — sufficient for most custom training needs.
- **Custom container** = define everything (environment, machine type, disks) — only needed for very specific infrastructure requirements.
- Keras three-step workflow: **Sequential (create) → compile → fit** — know the method names: `tf.keras.Sequential`, `model.compile`, `model.fit`.
- **Vertex AI Workbench** = Jupyter for full data science lifecycle; **Colab Enterprise** = familiar Colab interface within Vertex AI.
- TensorFlow is fully hosted on Vertex AI — all abstraction levels (low-level to Keras) get a managed service.
- **JAX** is distinct from TensorFlow — newer, high-performance, flexible for both research and production.

---

## Questions to Follow Up

- What is the PMLE exam's expected depth on TensorFlow vs. PyTorch vs. JAX — is framework choice testable or just framework concepts?
- How does Colab Enterprise differ from standard free Colab in terms of data access and security for enterprise use?
