# Prompt Engineering — Notes

> **Source:** `transcriptions/04-prompt-engineering.md`
> **Module:** 02-generative-ai

---

## Summary

This lesson covers the first half of the prompt-to-production lifecycle in depth: prompt design, evaluation, and refinement within Vertex AI Studio. It explains prompt templates with reusable variables, model selection (Google and third-party), and the key parameters that control model output randomness — temperature, Top K, and Top P. The lesson concludes with how to evaluate prompts side-by-side and manage them via version control, setting the stage for deployment in the next lesson.

---

## Key Concepts

### Prompt Templates

Vertex AI Studio supports prompt templates with replaceable variables, analogous to a function in programming where you define the structure once and pass different arguments each time. This enables reuse of prompt logic across different datasets or queries without rewriting the prompt from scratch.

### Model Selection in Vertex AI Studio

Vertex AI Studio provides access to both Google's models (Gemini family, Imagen, Chirp, Veo, Lyria) and third-party models (Anthropic Claude, Meta Llama, OpenAI GPT). The key advantage is access to Google's cutting-edge Gemini models. Model choice depends on task type: Gemini variants for general/multimodal; specialty models for specific media creation tasks.

### Temperature

Temperature controls the randomness of token selection. A **low temperature** narrows output to high-probability tokens — predictable and suitable for factual Q&A and summarization. A **high temperature** expands to lower-probability tokens — more creative and varied, good for brainstorming or open-ended generation.

### Top K

Top K randomly selects a token from among the K most probable next tokens, giving each equal probability. A Top K of 2 means the model picks randomly between the two most likely words. Problem: if the probability distribution is skewed, Top K can yield unlikely results (e.g., choosing "books" over "flowers" at equal probability).

### Top P (Nucleus Sampling)

Top P selects from the smallest set of tokens whose cumulative probability exceeds P. For example, Top P = 75% means sampling from tokens that together account for 75% of probability mass. This dynamically adapts to the distribution, avoiding the fixed-size limitation of Top K. You rarely need to tune Top K and Top P constantly — defaults work for most tasks.

### Prompt Evaluation and Management

Vertex AI Studio allows side-by-side prompt comparison with custom evaluation metrics (including user-supplied ground truth). The Prompt management menu provides storage, versioning, and sharing of prompts for collaboration. Optimization can be done in a Colab Enterprise notebook.

---

## Google Cloud Products & Tools Mentioned

| Product / Tool | What it does in this context |
|---|---|
| Vertex AI Studio | Primary environment for designing, parameterizing, and evaluating prompts |
| Gemini (Flash, Pro) | Default models for general-purpose and multimodal prompting |
| Imagen | Image creation model accessible in Vertex AI Studio's media studio |
| Chirp | Voice/audio generation model |
| Veo | Video generation model |
| Lyria | Music composition model |
| Colab Enterprise | Notebook for prompt optimization with labeled examples |

---

## How Concepts Relate

Temperature, Top K, and Top P all control the same thing — how the model selects the next output token — but at different levels of granularity. Temperature is the coarsest lever (more/less randomness overall); Top K sets a hard count; Top P adapts dynamically to the probability distribution. In practice, temperature is the most commonly adjusted parameter, while Top K and Top P are advanced controls. Prompt templates extend the value of prompt engineering by enabling reuse, which bridges toward production-grade applications discussed in the next lesson.

---

## Exam Tips

- **Low temperature** → deterministic, factual (Q&A, summarization); **High temperature** → creative, diverse.
- **Top K** = fixed number of candidates; **Top P** = dynamic set by cumulative probability — Top P is generally preferred.
- Vertex AI Studio supports third-party models (Claude, Llama, GPT) in addition to Google's Gemini models.
- Prompt templates use **replaceable variables** — like function parameters in natural language.
- Side-by-side prompt comparison in Vertex AI Studio lets you evaluate different models or parameters on the same input.
- Prompt management provides version control — this is relevant for MLOps-style questions about reproducibility.

---

## Questions to Follow Up

- In the PMLE exam, when would Top P vs Top K matter as a design choice — are there scenario-type questions on this?
- How does Colab Enterprise integration with Vertex AI Studio differ from using standalone Colab notebooks?
