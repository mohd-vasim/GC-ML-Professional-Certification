# Generative AI Module — Quiz Notes

> **Source:** `transcriptions/10-quiz.md`
> **Module:** 02-generative-ai

---

## Questions and Answers

**1. Which type of prompt allows a generative AI model to perform a task with a few examples?**

- Zero-shot prompt
- Supervised prompt
- Unsupervised prompt
- ✓ **Few-shot prompt**

*Why correct:* Few-shot prompting provides examples (demonstrations of desired input-output) alongside the task. Zero-shot provides the task only, with no examples.

---

**2. What is the best way to generate more creative or unexpected content by adjusting model parameters in Generative AI Studio?**

- ✓ **Set the temperature to a high value.**
- Set the temperature to a low value.
- Set the top P to 25%.
- Set the top K to 1.

*Why correct:* High temperature expands the range of token candidates to include lower-probability, more unusual words, producing more creative output. Low temperature is for predictable, factual responses.

---

**3. What are the three major components of an AI agent?**

- ✓ **The model, the tools, the orchestration layer**
- Prompt, prompt design, and prompt engineering
- AI infrastructure, AI development, and AI solutions
- Storage, computing, and network

*Why correct:* An AI agent is defined by its model (reasoning/brain), tools (external action), and orchestration layer (coordination/nervous system). These are the three canonical components.

---

**4. How does generative AI generate new content?**

- The training leads to a foundation model that cannot be further tuned with a new dataset.
- ✓ **It learns from a massive amount of existing content and can then be used to solve general problems or be further tuned to solve specific problems.**
- It's programmed based on predetermined algorithms that cannot be altered.
- It's a random process.

*Why correct:* Training on large datasets produces a foundation model (horizontal AI) that can then be fine-tuned on smaller domain-specific datasets (vertical AI). The process is learned, not random or fixed.

---

**5. To build an agent with deep legacy system integration and custom industry-policy response behavior — which tool?**

- NotebookLM
- Gemini Enterprise
- ✓ **Vertex AI Agent Builder with the Agent Development Kit (ADK)**
- Vertex AI Model Garden

*Why correct:* ADK is the pro-code path for agents requiring custom logic, deep integrations, and specific behavioral constraints. Gemini Enterprise and NotebookLM are no-code tools with limited customization. Model Garden provides models, not an agent development framework.
