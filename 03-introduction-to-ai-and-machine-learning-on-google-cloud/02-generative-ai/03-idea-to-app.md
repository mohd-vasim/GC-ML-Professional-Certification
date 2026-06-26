# Idea to App with Vertex AI Studio — Notes

> **Source:** `transcriptions/03-idea-to-app.md`
> **Module:** 02-generative-ai

---

## Summary

This lesson introduces Vertex AI Studio as the central tool for turning a Gen AI idea into a working application, following three personas: Bea (business analyst, no technical background), Ann (AI developer), and Ian (ML engineer). It covers the prompt-to-production lifecycle at a high level, the anatomy of a good prompt (task, context, examples), and how Vertex AI Studio enables rapid prototyping — including auto-generating a web app directly from a prompt. The goal is to show that Gen AI development is accessible at multiple skill levels.

---

## Key Concepts

### Vertex AI Studio

Vertex AI Studio is the interface between developers and foundation models. It supports a low-code to no-code environment where users can test prompts, tune models with their own data, ground responses with real-world data, and deploy models to production with auto-generated code. It is the primary workspace for the prompt-to-production lifecycle.

### The Prompt-to-Production Lifecycle

The full lifecycle has three phases: (1) designing, evaluating, and refining prompts; (2) building and testing applications; (3) monitoring and optimizing Gen AI models. Bea and Ann demonstrated the fastest path — directly from prompt to deployed web app by clicking "Build with Code" and "Deploy as App."

### Anatomy of a Prompt

A prompt has up to three components: **Task** (required) — the core instruction; **Context** (optional) — background or system-level instruction; **Examples** (optional) — demonstrations of desired output format or behavior. Simple tasks only need a task (zero-shot). Complex tasks benefit from context and examples (few-shot).

### Zero-shot vs. Few-shot Prompting

Zero-shot prompting provides only the task, no examples. Few-shot prompting includes examples of desired input-output pairs to guide the model on complex tasks. Few-shot prompting is more effective when the desired output format is specific or non-obvious.

### Effective Prompt Crafting

Effective prompts are direct and specific, use structure (labels, delimiters, step-by-step instructions), and iterate based on AI output. Advanced techniques include few-shot prompting, chain-of-thought prompting, and RAG. The best prompt includes all three components — task, context, and examples — organized clearly.

---

## Google Cloud Products & Tools Mentioned

| Product / Tool | What it does in this context |
|---|---|
| Vertex AI Studio | Main platform for designing, testing, and deploying prompts and Gen AI apps |
| Gemini Enterprise | No-code option for business users; mentioned as the starting point for Bea |
| NotebookLM | AI research assistant shown as an application-layer option |
| Agent Builder | Tool for deploying and managing AI agents (mentioned briefly as an option) |

---

## How Concepts Relate

Vertex AI Studio is the practical implementation of the "Gen AI development" layer in Google's three-layer stack. Understanding prompt anatomy is fundamental to using any Gen AI tool effectively. The three personas — Bea, Ann, Ian — map to no-code, low-code, and pro-code usage respectively, illustrating how Vertex AI Studio serves all technical levels. Moving from idea-to-app quickly is the entry point; deeper lifecycle stages (prompt engineering, deployment, tuning) are covered in subsequent lessons.

---

## Exam Tips

- A **task** is the only required component of a prompt; context and examples are optional but improve quality for complex tasks.
- **Zero-shot** = task only; **Few-shot** = task + examples; know the terminology.
- Vertex AI Studio can auto-generate a web application directly from a prompt — this is its "Deploy as App" feature.
- The prompt-to-production lifecycle has three distinct phases: design/evaluate/refine → build/test → monitor/optimize.
- RAG (Retrieval Augmented Generation) is listed as an advanced prompting technique — distinct from basic few-shot prompting.

---

## Questions to Follow Up

- How does chain-of-thought prompting differ from few-shot prompting for complex reasoning tasks on the PMLE exam?
- What is the relationship between Vertex AI Studio's "Build with Code" feature and actual SDK/API usage in production?
