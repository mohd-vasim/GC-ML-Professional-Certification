# AI Use Case: Coffee on Wheels — Notes

> **Source:** `transcriptions/01-use-case.md`
> **Module:** 01-ai-foundation

---

## Summary

This lesson opens the course with a concrete business story — Coffee on Wheels, a multinational food truck company — to show how AI moves beyond simple efficiency and becomes a driver of innovation. The three core problems the company faces (where to park trucks, how to forecast sales, and how to automate marketing) map directly to the two AI paradigms you'll study throughout the course: predictive AI and generative AI. The demo walkthrough shows a real-time dashboard that ties together BigQuery, Vertex AI, Gemini, and Looker.

---

## Key Concepts

### Predictive AI vs. Generative AI in a Business Context

Predictive AI solves problems where you want to forecast or optimize based on historical patterns — like choosing the best truck location given weather and traffic. Generative AI solves problems where you want to create something new — like writing a personalized marketing campaign email or generating a new menu suggestion. The lesson's key insight is that these two are not mutually exclusive: the output of a prediction can become the input to a generation (e.g., predict which customers are at risk of churning, then generate personalized outreach for them).

### Multimodal Input

The Coffee on Wheels app ingests multiple data types simultaneously: text (customer reviews), images (coffee and food photos), and video (real-time street view). This is called multimodal input and is what makes modern AI systems powerful — they aren't limited to a single data type the way classical ML models are.

### Data-to-AI Workflow

The lesson introduces a layered view of how Google products collaborate: Gemini handles multimodal data acquisition, BigQuery provides analytics, Vertex AI runs ML model development, and AI agents connect outputs to downstream systems like Looker for visualization. This pipeline pattern — data → analytics → prediction/generation → action — recurs throughout the course.

---

## Google Cloud Products & Tools Mentioned

| Product / Tool | What it does in this context |
|---|---|
| BigQuery | Stores and queries the business data that feeds the dashboard |
| Vertex AI | Hosts and runs the ML models powering sales forecasts and route optimization |
| Gemini | Provides multimodal capabilities (text, image, video understanding) |
| Looker | Visualizes the resulting insights and operational reports |
| AI Agents | Connect model outputs to business actions (e.g., publishing a new route, sending an email) |

---

## How Concepts Relate

The Coffee on Wheels use case is designed to make the abstract concrete. Predictive AI (sales forecasting, route optimization) provides structured numerical outputs, while generative AI (campaign creation, menu suggestions) takes those outputs and turns them into human-readable actions. Both rely on the same underlying infrastructure: BigQuery for data, Vertex AI for ML, and Gemini for multimodal understanding. The lesson is essentially a preview of the entire course architecture seen through one business story.

---

## Exam Tips

- **Predictive AI = analyze/forecast** using historical data. **Generative AI = create** new content or take action. Know which category a given business problem falls into.
- Combining both is valid and often ideal: use predictive AI output as a prompt input to generative AI.
- The three Google Cloud AI layers are: **AI infrastructure → AI development (Vertex AI) → AI applications and solutions**. Coffee on Wheels spans all three.
- AI agents connect model outputs to external systems — they are not models themselves.

---

## Questions to Follow Up

- How does Gemini Multimodal specifically handle real-time video input like street view? Is this streaming inference?
- What is the difference between Vertex AI agents and standalone AI agents built with frameworks like LangGraph?
- How does Looker connect to Vertex AI model outputs — is it a direct API or through BigQuery?
