# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Repository Purpose

This is a personal study notes repository for the **Google Cloud Professional Machine Learning Engineer (PMLE)** certification, tracking the [19-activity learning path](https://www.skills.google/paths/17). There is no build system, test suite, or runnable code — the content is entirely markdown notes.

## Structure

Each top-level numbered folder corresponds to one activity in the learning path:

```
NN-course-name/
├── README.md          # Course overview and metadata
├── NN-summary.md      # High-level course summary
├── NN-<module>/       # Per-module subfolder
│   ├── NN-<topic>.md  # Notes per video/lesson (content is transcript text or summaries)
│   └── NN-quiz.md     # Quiz questions and answers
└── NN-course-resources.md
```

Notes in `01-ai-foundation/` and similar subfolders currently contain raw video transcripts. The intended format (see [01-build-a-certification-study-guide-pmle/NOTES.md](01-build-a-certification-study-guide-pmle/NOTES.md)) is:
- **Summary** (2–3 sentences)
- **Key Concepts** (bullet list)
- **Tools / Products Mentioned**
- **Exam Tips**
- **Questions / Things to Follow Up**
- **Overall Takeaways** and **Exam-Relevant Points** at the course level

## Content Domain

The path covers: BigQuery ML, Vertex AI (Feature Store, Model Evaluation, MLOps), Keras/TensorFlow on Google Cloud, Generative AI (LLMs, RAG, Agent Studio), MLOps lifecycle, and Responsible AI (fairness, interpretability, privacy). Activity 08 is deprecated but retained.

## Working With Notes

- When summarizing transcripts into structured notes, follow the NOTES.md template above.
- Exam-relevant points should focus on tradeoffs, definitions, and service distinctions likely to appear on the PMLE exam.
- Raw transcript files use a `MM:SS` timestamp prefix per paragraph — strip these when converting to clean notes.
