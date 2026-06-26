# MLOps and Workflow Automation — Notes

> **Source:** `transcriptions/05-mlops-workflow-automation.md`
> **Module:** 04-ai-development-workflow

---

## Summary

MLOps (Machine Learning Operations) applies DevOps principles to ML — automating and monitoring every step of ML system construction to enable continuous integration, training, and delivery (CI/CT/CD). This lesson explains the role of Vertex AI Pipelines as the MLOps backbone, introduces Kubeflow Pipelines (KFP) and TensorFlow Extended (TFX) as supported pipeline frameworks, describes the three phases of MLOps maturity (0 → 1 → 2), and walks through a concrete example of building and running an AutoML classification pipeline.

---

## Key Concepts

### What MLOps Is

MLOps combines ML development with operations, solving production challenges around constantly evolving data and code. Practicing MLOps means automating and monitoring each step of the ML system: CI (continuous integration), CT (continuous training), and CD (continuous delivery). Both data and model logic change over time, so automation is essential for sustainability in production.

### Vertex AI Pipelines

The core MLOps toolkit on Vertex AI. It supports two pipeline SDKs:
- **Kubeflow Pipelines (KFP)**: general-purpose ML pipeline framework; good default for most ML workflows.
- **TensorFlow Extended (TFX)**: for TensorFlow-based models processing large structured datasets — use when you're already using TF.

A pipeline runs in two environments: (1) experimentation/development/test, and (2) staging/pre-production/production.

### Pipeline Components

A **pipeline component** is a self-contained unit of code that performs one task in the workflow — analogous to a function. Components are assembled into a pipeline to automate the full workflow. Two types:
- **Pre-built components** (provided by Google Cloud): e.g., `TabularDatasetCreateOp`, `AutoMLTabularTrainingJobRunOp`, `EndpointCreateOp`, `ModelDeployOp`.
- **Custom components**: built for task-specific logic not covered by pre-built options (e.g., a custom evaluation threshold component).

### Three MLOps Maturity Phases

- **Phase 0**: no automation; manual GUI-based workflow (AutoML UI). Critical as a first step to understand the end-to-end workflow before automating it.
- **Phase 1**: begin automating ML workflow by building pipeline components using Vertex AI Pipelines SDKs.
- **Phase 2**: integrate all components into a full automated pipeline achieving CI/CT/CD.

### Building and Running a Pipeline (Example)

To automate a bean classification AutoML model:
1. Plan the pipeline as a series of components (pre-built + custom).
2. Build any custom components needed (e.g., `classification_model_eval_metrics` to compare performance against a threshold and decide deploy vs. retrain).
3. Assemble with pre-built components: `TabularDatasetCreateOp` → `AutoMLTabularTrainingJobRunOp` → `classification_model_eval_metrics` → `EndpointCreateOp` + `ModelDeployOp`.
4. Compile with `compiler.Compiler().compile()` and run as a pipeline job.

Google Cloud visualizes the pipeline graph from the code, making it easy to audit components and artifacts.

---

## Google Cloud Products & Tools Mentioned

| Product / Tool | What it does in this context |
|---|---|
| Vertex AI Pipelines | Serverless MLOps toolkit supporting KFP and TFX for automated ML workflows |
| Kubeflow Pipelines (KFP) | General-purpose ML pipeline SDK supported by Vertex AI Pipelines |
| TensorFlow Extended (TFX) | TF-native pipeline SDK for large structured data; alternative to KFP |
| Vertex AI Workbench | Notebook for coding and running pipeline definitions |
| Colab Enterprise | Alternative notebook for pipeline development |
| Vertex AI Model Registry | Repository where trained/tuned models land after a pipeline training job |

---

## Exam Tips

- MLOps achieves **CI/CT/CD**: continuous integration, training, delivery — not just CI/CD.
- **KFP** = general-purpose pipeline SDK; **TFX** = TensorFlow-specific for large structured data — choose TFX only when already using TensorFlow on large tabular datasets.
- Pipeline components = functions in code — each does **one task**, enabling reuse (single responsibility principle).
- **Phase 0 = no automation** (manual GUI); **Phase 1 = component development**; **Phase 2 = full pipeline CI/CT/CD**.
- Vertex AI provides **pipeline templates** (e.g., classification/regression of tabular data with AutoML) — don't start from scratch.
- Google Cloud **visualizes the pipeline graph** from code — useful for auditing and debugging.

---

## Questions to Follow Up

- How does model registry versioning work in Vertex AI Pipelines — does each pipeline run create a new model version automatically?
- What is the difference between a Vertex AI Pipeline and a Vertex AI Workflow — are these the same product?
