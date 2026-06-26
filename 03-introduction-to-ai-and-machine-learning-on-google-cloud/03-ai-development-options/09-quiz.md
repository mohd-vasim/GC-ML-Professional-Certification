# AI Development Options Module — Quiz Notes

> **Source:** `transcriptions/09-quiz.md`
> **Module:** 03-ai-development-options

---

## Questions and Answers

**1. A video production company wants to categorize event footage without training its own ML model. Which option helps?**

- BigQuery ML
- AutoML
- ✓ **Pre-trained APIs**
- Custom training

*Why correct:* Pre-trained APIs require no training data. Video categorization maps to Google's Video Intelligence API (or Gemini multimodal API). No model training needed.

---

**2. A global hotel chain has guest data in BigQuery, uses SQL, and wants to predict guest trends. Which option is best?**

- ✓ **BigQuery ML**
- Custom training
- Pre-trained APIs
- AutoML

*Why correct:* Data is already in BigQuery, team knows SQL. BigQuery ML allows SQL-based model training directly on BigQuery data — no data movement or code-based ML needed.

---

**3. Which code-based solution on Vertex AI gives data scientists full control over the development environment?**

- AutoML
- ✓ **Custom training**
- AI Platform
- AI Solutions

*Why correct:* Custom training gives complete control over architecture, frameworks, and training logic. AutoML is no-code. AI Platform is the old name for Vertex AI, not a current option name.

---

**4. Your company has massive data and wants to build its own ML model — but requires a codeless solution. Which option?**

- BigQuery ML
- Custom training
- Pre-trained APIs
- ✓ **AutoML**

*Why correct:* AutoML is the no-code UI solution for training custom ML models using your own data. Custom training requires code; BigQuery ML requires SQL; Pre-trained APIs don't train on your data.

---

**5. Which of the following can you do with the Natural Language API?**

- Classify pictures.
- Complete new areas of an existing image.
- ✓ **Analyze sentiment and identify subjects of text.**
- Generate a caption for a YouTube video.

*Why correct:* The Natural Language API's core capabilities are entity identification (subjects), sentiment analysis, syntax analysis, and content classification — all text-based operations.

---

**6. Which `tf.keras` construct lets you create a neural network with multiple layers?**

- tf.keras.Run
- model.fit
- ✓ **tf.keras.Sequential**
- model.compile

*Why correct:* `tf.keras.Sequential` defines the neural network architecture by stacking layers. `model.compile` sets the optimizer and loss; `model.fit` runs training. There is no `tf.keras.Run`.
