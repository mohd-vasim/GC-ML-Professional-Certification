# Deployment and Model Tuning — Notes

> **Source:** `transcriptions/05-deployment-and-model-tuning.md`
> **Module:** 02-generative-ai

---

## Summary

This lesson covers the second half of the prompt-to-production lifecycle: integration, deployment, and model tuning in Vertex AI Studio. It explains how auto-generated code (Python SDK or cURL API) is used to move from prototype to production, integrated with Cloud Run and Cloud Shell. The lesson then distinguishes two techniques for improving Gen AI output quality: grounding/RAG (connecting the model to current external data) and model tuning (training the model on domain-specific labeled examples via supervised fine-tuning).

---

## Key Concepts

### From Prototype to Production with Auto-Generated Code

Vertex AI Studio's "Build with Code" feature generates Python SDK or cURL API code from a designed prompt, removing the manual effort of writing integration code. Cloud Run and Cloud Shell are integrated for deployment, removing the need to configure the underlying cloud infrastructure. This path serves developers and ML engineers who want to embed Gen AI into custom applications.

### Grounding and RAG

Foundation models are pre-trained on static data that can be outdated or lack domain specificity. **Grounding** connects the model to external trusted data sources at inference time so its answers are verified against current information. **RAG (Retrieval Augmented Generation)** is the mechanism that implements grounding: it retrieves relevant documents from an external store and augments the prompt with that context. The analogy: grounding is the **what** (connect to fresh data), RAG is the **how** (retrieve-augment-generate). In Vertex AI Studio, grounding can use Google real-time search or a user's own data.

### Model Tuning Options

When prompt design alone isn't sufficient, there are three tuning options along a spectrum of computational cost:
- **Prompt design** — guides behavior through instructions and examples; no parameter changes; accessible to non-engineers.
- **Parameter-efficient tuning (adapter tuning)** — updates a small subset of model parameters; balances quality and compute cost.
- **Full fine-tuning** — updates all parameters; highest quality for complex tasks; highest compute cost.

### Supervised Fine-Tuning

Vertex AI supports supervised fine-tuning as the primary tuning method. A JSONL file with input-output pairs (prompt → expected response) is used as the training dataset. The tuned model combines newly learned parameters with the original foundation model and appears in the Vertex AI Model Registry for deployment. It's suited for well-defined tasks with labeled data: classification, summarization, extraction, chat.

---

## Google Cloud Products & Tools Mentioned

| Product / Tool | What it does in this context |
|---|---|
| Vertex AI Studio | Provides "Build with Code" for SDK/API generation and the Tuning menu for fine-tuning jobs |
| Cloud Run | Serverless deployment environment for Gen AI applications |
| Cloud Shell | Command-line environment for deploying and managing applications |
| Vertex AI Model Registry | Stores tuned models after a fine-tuning job completes |
| BigQuery | Mentioned as a platform for RAG pipeline implementation |
| Vector Search (Vertex AI) | One of two platforms cited for building RAG pipelines |

---

## How Concepts Relate

Grounding/RAG and model tuning are complementary but address different problems: grounding solves the **currency** problem (outdated or missing knowledge at inference time), while tuning solves the **competence** problem (the model doesn't know how to behave for a specific task). Using the K-12 analogy: tuning is like medical school (embeds domain expertise), grounding is like reading the latest medical journals (stays current). In practice, many production systems use both: a tuned model for task behavior plus RAG for factual freshness.

---

## Exam Tips

- **Grounding = what** (anchor to external data); **RAG = how** (mechanism to retrieve and inject that data into the prompt).
- Prompt design does **not** change model parameters — it only shapes behavior through instruction.
- Parameter-efficient tuning updates a **subset** of parameters; full fine-tuning updates **all** — full fine-tuning has the highest compute cost.
- Supervised fine-tuning requires a **JSONL file** with labeled input-output pairs.
- Tuning data needs hundreds of labeled examples; the output is a **new model** in the Model Registry.
- Cloud Run + Cloud Shell integration in Vertex AI Studio means developers don't need to manage cloud infrastructure for deployment.

---

## Questions to Follow Up

- How does BigQuery-based RAG differ from Vertex AI Vector Search-based RAG — when to choose each for PMLE scenarios?
- What is the difference between supervised fine-tuning and RLHF (Reinforcement Learning from Human Feedback) — is RLHF covered in the PMLE scope?
