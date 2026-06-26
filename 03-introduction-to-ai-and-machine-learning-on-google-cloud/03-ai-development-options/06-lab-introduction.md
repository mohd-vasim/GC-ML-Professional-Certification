# Lab Introduction: Natural Language API — Notes

> **Source:** `transcriptions/06-lab-introduction.md`
> **Module:** 03-ai-development-options

---

## Summary

This lesson prepares students for a hands-on lab using the Natural Language API to analyze text programmatically. It reviews the four core capabilities of the API (entity identification, sentiment analysis, syntax analysis, content classification), explains the request-response structure of the REST API (JSON with cURL), and provides the conceptual framework for how to construct and call API requests in code.

---

## Key Concepts

### Natural Language API Capabilities (Review)

Four analysis types:
- **Entity analysis** (`analyzeEntities`): identifies subjects in text — e.g., "Google" as a company, "Mountain View" as a location.
- **Sentiment analysis** (`analyzeSentiment`, `analyzeEntitySentiment`): detects emotion at document level and per-entity level.
- **Syntax analysis** (`analyzeSyntax`): extracts linguistic structure — relationships between words.
- **Content classification** (`classifyText`): assigns text to categories based on topics or keywords, like a tag.

### API in Code vs. UI

The UI enables quick demonstration and testing of API features. But for **production use**, the API must be embedded in code — the JSON request must be constructed and called programmatically. The UI is for exploration; the code integration is for deployment.

### API Request Structure

A Natural Language API JSON request (for entity analysis) includes:
- `type`: document type (e.g., `PLAIN_TEXT`)
- `language`: e.g., `EN`
- `content`: the text itself, or a Cloud Storage file path
- `encodingType`: e.g., `UTF8`

### Calling the API with cURL

```bash
curl -s -H "Content-Type: application/json" \
  -H "Authorization: Bearer $(gcloud auth print-access-token)" \
  -X POST \
  -d @request.json \
  https://language.googleapis.com/v1/documents:analyzeEntities \
  > result.json
```

The response is a JSON file that can be reviewed with `cat result.json` or parsed for further use. Python and Java SDKs are also available.

---

## Google Cloud Products & Tools Mentioned

| Product / Tool | What it does in this context |
|---|---|
| Natural Language API | Pre-trained API for entity, sentiment, syntax, and category analysis on text |
| Cloud Storage | Alternative source for document content in API requests |
| cURL | Command-line tool for making REST API calls in the lab |

---

## Exam Tips

- Natural Language API methods: `analyzeEntities`, `analyzeSentiment`, `analyzeEntitySentiment`, `analyzeSyntax`, `classifyText`.
- API requests use **REST with JSON** — the request body specifies document type, language, content, and encoding.
- cURL can be used to call any Google Cloud REST API — it's not specific to the Natural Language API.
- Three things you need to use any API: **features** (what it can do), **input** (how to format the request), **output** (how to handle the response).

---

## Questions to Follow Up

- How does entity-level sentiment (`analyzeEntitySentiment`) differ from document-level sentiment (`analyzeSentiment`) — which is more useful for product review analysis?
