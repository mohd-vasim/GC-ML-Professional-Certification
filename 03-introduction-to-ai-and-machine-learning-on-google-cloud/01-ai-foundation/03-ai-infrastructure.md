# AI Infrastructure on Google Cloud — Notes

> **Source:** `transcriptions/03-ai-infrastructure.md`
> **Module:** 01-ai-foundation

---

## Summary

This lesson zooms into the foundational layer of Google Cloud's AI stack — the infrastructure that everything else runs on. It covers three tiers: networking/security at the base, compute and storage in the middle, and data/AI products at the top. The central theme is that compute and storage are deliberately decoupled on Google Cloud so each can scale independently. The lesson also introduces TPUs as Google's purpose-built chip for AI workloads and closes by showing the end-to-end data-to-AI product workflow.

---

## Key Concepts

### Three-Tier Infrastructure Architecture

Google Cloud's infrastructure is structured in three tiers. The **base tier** handles networking and security — the plumbing that everything else depends on. The **middle tier** contains compute and storage, which are decoupled from each other (unlike a local machine where they're tightly coupled). The **top tier** houses the data and AI products — BigQuery, Vertex AI, Looker, etc. — which abstract away the underlying hardware complexity so you can focus on the ML problem rather than infrastructure management.

### Compute Spectrum: From High Control to Serverless

Google offers a spectrum of compute options depending on how much control vs. convenience you want:
- **Compute Engine** — full VM control, like managing a physical server.
- **Google Kubernetes Engine (GKE)** — containerized workloads with orchestration.
- **Cloud Run** — fully serverless; Google manages all infrastructure.

For ML workloads specifically, you also choose from CPU, GPU, and TPU hardware.

### TPUs: Purpose-Built for AI

Central Processing Units (CPUs) are general-purpose. Graphics Processing Units (GPUs) were originally built for rendering but handle matrix math well, making them useful for ML. Tensor Processing Units (TPUs) are Google's custom chips, introduced in 2016, designed specifically for the kind of math that dominates ML: matrix multiplication. Because they're domain-specific, TPUs are significantly faster and more energy-efficient than GPUs and CPUs for AI/ML workloads. They're integrated across Google's own products and available to Google Cloud customers as Cloud TPUs.

### Decoupled Compute and Storage

On a laptop, compute and storage are tightly bound — more processing doesn't give you more disk space. Cloud separates these entirely, so you can scale up compute for a training job without paying for extra storage, and vice versa. This is one of the fundamental architecture differences between cloud and local computing.

### Storage Options by Data Type

The right storage product depends on what kind of data you have:
- **Unstructured data** (images, audio, documents, video): use **Cloud Storage**.
- **Structured data** (tables, rows, columns): use **BigQuery**, **AlloyDB**, **Cloud SQL**, or **Spanner**.
- **Semi-structured data** (JSON): BigQuery handles this natively and is highly optimized for it.
- **NoSQL**: **Bigtable** (wide-column, high-throughput) or **Firestore** (document store).

BigQuery is particularly versatile — it can even query unstructured data in Cloud Storage by defining an external table that provides a structured reference to it.

### Data-to-AI Workflow

The top layer products follow a three-phase workflow:
1. **Ingest & Process** — Pub/Sub (streaming events), Dataflow (stream and batch processing), Dataproc (Spark/Hadoop), Cloud Data Fusion (ETL pipelines).
2. **Store & Analyze** — Cloud Storage, BigQuery, Looker.
3. **Activate with AI** — Vertex AI (Studio, Agent Builder, AutoML, Notebooks) for both predictive and generative AI.

---

## Google Cloud Products & Tools Mentioned

| Product / Tool | What it does in this context |
|---|---|
| Compute Engine | High-control IaaS VMs |
| GKE | Container orchestration (Kubernetes) |
| Cloud Run | Serverless container execution |
| TPU (Cloud TPU) | Domain-specific chip accelerating matrix math for AI/ML |
| Cloud Storage | Object storage for unstructured data |
| BigQuery | Data warehouse for structured + semi-structured data; also queries external unstructured data |
| AlloyDB | PostgreSQL-compatible, high-performance relational DB |
| Pub/Sub | Asynchronous messaging / event streaming |
| Dataflow | Managed Apache Beam for stream and batch pipelines |
| Dataproc | Managed Spark/Hadoop for large-scale data processing |
| Cloud Data Fusion | Code-free ETL pipeline builder |
| Looker | BI and data visualization |
| Vertex AI | AI development platform: Studio, Agent Builder, AutoML, Notebooks |

---

## How Concepts Relate

The decoupling of compute and storage is what makes scalable AI possible on Google Cloud: a BigQuery training query can spin up massive compute without touching the storage layer. TPUs sit within that compute tier and are the reason Google can train foundation models like Gemini at scale. The data-to-AI workflow ties all of this together — data flows from ingestion tools through storage into BigQuery and Vertex AI, where models are trained and deployed. The infrastructure layer exists precisely so that practitioners can use BigQuery ML or Vertex AI without ever configuring a single server.

---

## Exam Tips

- **TPUs are domain-specific** (built for matrix multiplication / ML). CPUs and GPUs are general-purpose. Cloud TPUs are faster and more energy-efficient than GPUs/CPUs for AI workloads.
- **TPUs were introduced by Google in 2016.**
- Cloud separates compute and storage so they scale **independently** — this is a key architectural difference from on-premises.
- **Unstructured data → Cloud Storage. Structured data → BigQuery / Cloud SQL / Spanner. NoSQL → Bigtable / Firestore.**
- BigQuery can query unstructured data in Cloud Storage via **external tables**.
- The data-to-AI product flow: **Ingest/Process → Store/Analyze → Activate with AI**.

---

## Questions to Follow Up

- What is the current generation of Cloud TPU (TPU v5?) and how do its specs compare to NVIDIA H100 GPUs?
- When would you choose Dataproc (Spark) over Dataflow (Beam)? What are the use-case tradeoffs?
- Can you use a Cloud TPU directly from a Vertex AI training job, or does it require separate configuration?
