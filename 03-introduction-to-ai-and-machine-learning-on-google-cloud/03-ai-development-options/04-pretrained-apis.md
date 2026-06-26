# Pre-trained APIs — Notes

> **Source:** `transcriptions/04-pretrained-apis.md`
> **Module:** 03-ai-development-options

---

## Summary

Pre-trained APIs allow developers to use Google's ML models without training their own, by making simple API calls. This lesson explains what APIs are (using an electrical outlet analogy), shows a code example using the Gemini API via the Google AI Python SDK, and catalogs the categories of Google Cloud APIs available — from Gemini generative APIs to specialized speech, image, and document APIs.

---

## Key Concepts

### What an API Is (in Context)

An API (Application Programming Interface) defines how software components communicate. Like an electrical outlet adapter, you only need to know the interface (which API to call and what parameters to pass) — not what's behind the wall (model training, deployment infrastructure). APIs abstract all model complexity into a simple function call.

### Using the Gemini API: The Four Steps

A typical API call with the Google AI Python SDK follows four steps:
1. **Authenticate**: `genai.configure(api_key="YOUR_API_KEY")` — grants permission to use the API.
2. **Select model**: `model = genai.GenerativeModel("gemini-2.5-flash")` — specifies which foundation model to use.
3. **Make API call**: `response = model.generate_content("What are the three largest countries by area?")` — sends the prompt.
4. **Receive response**: `print(response.text)` — retrieves and uses the generated output.

### Google Cloud API Categories

- **Generative AI APIs**: Foundation model APIs (multimodal Gemini APIs for content creation); Vertex AI Agent Builder APIs for building and deploying agents.
- **ML APIs**: Vertex AI API for training, monitoring, and tuning ML models with minimal ML expertise.
- **Other specialized APIs**: Speech, image, document, and conversation APIs — many of which are being subsumed by the more capable multimodal Gemini APIs.

### Natural Language API

A specific example of a pre-trained API for text analysis. Capabilities: entity identification (subjects in text), sentiment analysis (document-level and entity-level), syntax analysis (linguistic structure, word relationships), and content classification (topic/keyword-based tagging). Used in the upcoming lab.

---

## Google Cloud Products & Tools Mentioned

| Product / Tool | What it does in this context |
|---|---|
| Gemini API | Primary generative AI API for content creation via model.generate_content() |
| Google AI Python SDK | SDK that provides genai.configure and GenerativeModel classes for Gemini access |
| Vertex AI API | ML training/monitoring API usable with minimal ML expertise |
| Vertex AI Agent Builder APIs | Suite for building and deploying AI agents via API |
| Natural Language API | Pre-trained API for entity, sentiment, syntax, and content classification from text |

---

## How Concepts Relate

Pre-trained APIs sit at the low-code end of the AI development spectrum — below AutoML (no-code UI) but above custom training. They are the right choice when you have no training data but need to add AI capability quickly. The Gemini APIs are increasingly generalizing the specialized APIs (speech, image, document) due to their multimodal capability. The Natural Language API exemplifies the "use without training" principle: four analysis capabilities, zero model training required.

---

## Exam Tips

- Pre-trained APIs require **no training data** — this is the primary differentiator from AutoML and Custom Training.
- Using an API is like calling a predefined function: you pass inputs and receive outputs without knowing the implementation.
- The Gemini API replaces many specialized APIs due to its **multimodal** (multi-task) capability.
- Natural Language API methods: `analyzeEntities`, `analyzeSentiment`, `analyzeEntitySentiment`, `analyzeSyntax`, `classifyText`.
- API calls use REST (JSON requests/responses) and can be made with **cURL** or language-specific SDKs (Python, Java).
- **Authentication**: every API call requires an API key passed via `genai.configure()` or equivalent.

---

## Questions to Follow Up

- What is the distinction between the Gemini API (via Google AI SDK) and the Vertex AI Gemini API — are these the same or different endpoints?
- For the PMLE exam, when would you recommend Natural Language API over a fine-tuned Gemini model for NLP tasks?
