# AI Development Options — Introduction Notes

> **Source:** `transcriptions/01-introduction.md`
> **Module:** 03-ai-development-options

---

## Summary

This lesson introduces the spectrum of AI development options on Google Cloud — from no-code out-of-the-box solutions to custom-coded pipelines — applicable to both Gen AI and predictive AI projects. It presents a comparison framework for four key options (Pre-trained APIs, BigQuery ML, AutoML, and Custom Training) across five dimensions: data type support, training data requirements, ML expertise needed, hyperparameter control, and training time. The module then maps each option to a user profile and concludes by previewing Vertex AI as the unified platform for all approaches.

---

## Key Concepts

### The AI Development Spectrum

Google Cloud's options form a spectrum from least to most technical: (1) no-code out-of-the-box (Gemini Enterprise, Conversational Agents); (2) no- to low-code (AutoML — point-and-click ML model building); (3) low-code (Pre-trained APIs — use pre-built models without training data); (4) code-based (BigQuery ML with SQL, ADK, or Custom Training for full control).

### Comparison Framework: Four Options

| Dimension | Pre-trained APIs | BigQuery ML | AutoML | Custom Training |
|---|---|---|---|---|
| Data types | Tabular, image, text, video, **audio** | Tabular, semi-structured (JSON) | Tabular, image | Tabular, image, text, video |
| Training data required | **None** | Large | Moderate | Large |
| ML/coding expertise | Low | SQL only | Low | High |
| Hyperparameter tuning | No | Yes | No | Yes |
| Training time | None (uses pre-trained) | Varies | Varies | Longest (builds from scratch) |

### Choosing the Right Option

- **Pre-trained APIs**: best if you have no training data and no in-house ML expertise; handles common perceptual tasks (vision, NLP, video).
- **BigQuery ML**: best if your team knows SQL and data is already in BigQuery; write SQL to build pre-defined ML models.
- **AutoML**: best if you have your own training data but want minimal coding; focuses on the business problem, not model architecture.
- **Custom Training**: best if ML engineers need full control over architecture, frameworks, and training logic.

---

## Google Cloud Products & Tools Mentioned

| Product / Tool | What it does in this context |
|---|---|
| Pre-trained APIs | Ready-to-use ML models from Google for common tasks (vision, NLP, video) |
| BigQuery ML | SQL-based ML model building on data already in BigQuery |
| AutoML (Vertex AI) | No-code ML model training via UI using your own labeled data |
| Custom Training (Vertex AI) | Full-code ML pipeline with complete architecture control |
| Gemini Enterprise | No-code Gen AI application; the top of the spectrum |
| ADK | Code-based Gen AI agent development; mentioned as one code-based approach |

---

## How Concepts Relate

All four options ultimately live within or connect to Vertex AI as Google's unified platform. The right choice depends on three variables: available training data, ML expertise, and required flexibility. Pre-trained APIs and AutoML sit at the accessible end; Custom Training sits at the flexible end. BigQuery ML is the outlier — it's code-based (SQL) but designed for analysts, not ML engineers, and only supports tabular/semi-structured data.

---

## Exam Tips

- **Pre-trained APIs** = no training data needed, no hyperparameter tuning — use when you have no labeled data.
- **BigQuery ML** = tabular/JSON only, requires SQL — use when the team knows SQL and data is in BigQuery.
- **AutoML** = no hyperparameter tuning, tabular and image only — use when you have labeled data but want minimal code.
- **Custom Training** = takes the longest (builds from scratch), requires most expertise, but offers full control.
- Only **Pre-trained APIs** can process audio — all others do not support audio as an input type.
- The question "which option requires no training data?" always points to Pre-trained APIs.

---

## Questions to Follow Up

- What specific pre-trained API products correspond to each data type (vision API, Video Intelligence API, Natural Language API, Speech-to-Text)?
- Does AutoML support video data in any configuration, or is it strictly tabular and image only?
