# prepare-notes

Convert raw video transcriptions in a course module folder into structured study notes.

## What this skill does

When invoked, look at the conversation context to figure out which folder to work on:
- If the user mentioned a folder, module, or course name — use that.
- If files or a directory were recently discussed — use that.
- If truly ambiguous, ask: "Which module folder should I prepare notes for?"

For the identified folder, do the following for each `.md` subfolder within it (e.g. `01-ai-foundation/`, `02-generative-ai/`):

1. **Identify transcription files** — `.md` files whose content contains raw video transcript text. Signals: lines starting with `SPEAKER:`, or bare timestamp lines like `00:05`. Skip empty files (placeholders) and files that are already structured notes (contain `## Summary` or `## Key Concepts`).
2. **Create a `transcriptions/` subfolder** inside the module subfolder and **move all transcription files** into it, preserving filenames.
3. **Create one detailed notes file per transcription** in the module subfolder itself (adjacent to `transcriptions/`), using the same filename as the source transcription.

---

## Notes format

Each generated notes file must follow this structure:

```markdown
# <Lesson Title> — Notes

> **Source:** `transcriptions/<original-filename>.md`
> **Module:** <module subfolder name>

---

## Summary

<2–4 sentence plain-English explanation of what the lesson covers. Write as if explaining to someone who hasn't seen the video. Focus on the core argument or teaching, not just a list of topics.>

---

## Key Concepts

### <Concept Name>

<2–5 sentences explaining the concept, its purpose, and how it fits into ML/AI on Google Cloud. Use analogies from the transcript where helpful. Synthesize — do not copy sentences verbatim.>

<!-- Repeat ### section for each major concept -->

---

## Google Cloud Products & Tools Mentioned

| Product / Tool | What it does in this context |
|---|---|
| <name> | <one-line explanation specific to how this lesson frames it> |

---

## How Concepts Relate

<3–6 sentences drawing connections between the concepts in this lesson — the "big picture" paragraph that explains why these ideas belong together.>

---

## Exam Tips

- <Specific, testable fact or tradeoff — e.g. "TPUs are domain-specific; CPUs/GPUs are general-purpose" not "Know about TPUs".>
- <Aim for 3–6 bullets.>

---

## Questions to Follow Up

- <Something mentioned briefly that deserves deeper investigation for exam prep, framed as a question.>
```

**Special cases:**
- **Quiz files** (filename contains `quiz`): move to `transcriptions/`, but notes should list each question with the correct answer clearly marked (`✓`) and a one-line explanation of why it's correct.
- **Summary files** (filename contains `summary`): move to `transcriptions/`, notes use only Summary + Key Concepts + Exam Tips sections.
- **Empty files**: move to `transcriptions/` silently, skip note generation.

---

## Tracker file

After processing, create or update `NOTES_TRACKER.md` in the **root of the repository** (not inside the course folder). This file is the single source of truth across all courses for what has been done and what remains.

**Format:**

```markdown
# Notes Tracker

> Course: <course folder name>
> Last updated: <YYYY-MM-DD>

---

## Progress

| Module | Lesson | Status | Notes file |
|---|---|---|---|
| 01-ai-foundation | 01-use-case | ✅ Done | [01-use-case.md](01-ai-foundation/01-use-case.md) |
| 01-ai-foundation | 02-ai-on-google-cloud | ✅ Done | [02-ai-on-google-cloud.md](01-ai-foundation/02-ai-on-google-cloud.md) |
| 01-ai-foundation | 06-predict-visitor-purchases-bigquery-ml | ⬜ Empty | — |
| 02-generative-ai | 01-generative-ai-google-cloud | 🔲 Pending | — |
| 02-generative-ai | 02-foundation-models | 🔲 Pending | — |

---

## Summary

- ✅ Done: X lessons
- 🔲 Pending: X lessons (transcription exists but notes not yet written)
- ⬜ Empty: X lessons (placeholder file, no transcription content yet)
```

**Status values:**
- `✅ Done` — notes file exists and is structured (has `## Summary`).
- `🔲 Pending` — transcription exists in `transcriptions/` but no notes file yet, or notes file is still raw transcript.
- `⬜ Empty` — file is 0 bytes; transcription content hasn't been added yet.

**Update rules:**
- If `NOTES_TRACKER.md` already exists, update only the rows affected by this run. Preserve all other rows.
- Scan every module subfolder in the course folder (not just the one being processed) so the tracker always reflects the full course state.
- The tracker is written last, after all notes files are created.

---

## After finishing

Print a summary for each module subfolder processed:

```
Module: 01-ai-foundation
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
Transcriptions moved:  5 → transcriptions/
Notes created:         5
Skipped (empty):       2
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
  ✓ 01-use-case.md
  ✓ 02-ai-on-google-cloud.md
  ...

NOTES_TRACKER.md updated.
```

---

## Rules

- Never delete transcription files — only move them.
- Never overwrite an existing notes file that is already structured (has `## Summary`).
- Process all module subfolders in the target folder unless the user asked for a specific one.
- Always update `NOTES_TRACKER.md` at the end of every run, even if no new notes were created.
