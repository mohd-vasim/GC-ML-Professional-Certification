SPEAKER: In the previous module, you explored cutting-edge technologies about generative AI.
00:04
But what if you want to create predictive AI for traditional AI tasks like forecasting and classification?
00:12
How do you build an ML model, and what options do you have?
00:15
Find the answers in this module.
00:17
You begin by comparing AI development options on Google Cloud, from no-code to low-code, and finally a do-it-yourself approach.
00:26
These options apply to both Gen AI and predictive AI.
00:30
You are then introduced to Vertex AI, Google Cloud's unified AI development platform, and your playground to build an ML model from end to end.
00:39
After that, we take a deep dive into how each of three options works-- AutoML, pre-trained APIs, and custom training.
00:48
Never miss a practice.
00:49
You conclude with hands-on experience using the natural language API to identify subjects and analyze sentiment in text.
00:57
Let's start with Google Cloud's AI development options.
01:00
What choices do you have for both generative AI and predictive AI projects?
01:04
And how do you make the right decision?
01:06
Let's find out.
01:08
Imagine transforming your organization's business model and operations with AI.
01:14
Perhaps you're a business user without a technical background, but you're eager to prototype business ideas using AI.
01:20
What are your options?
01:21
Or maybe you're a data scientist with training data looking to build a custom ML model without spending hours tuning parameters from scratch.
01:29
What choices do you have?
01:30
Even if you are an ML engineer who enjoys a do-it-yourself approach to building ML pipelines, what tools can you utilize?
01:39
Google Cloud can help you achieve your goals by meeting you where you are, offering no-code, out-of-box solutions like Gemini Enterprise and Conversational
01:49
Agents introduced in the previous Gen AI module-- no- to low-code solutions like AutoML, which helps you build your own ML models through
01:57
point and click; low-code solutions like pre-configured APIs, which use pre-trained ML models, eliminating the need to build your own if you lack
02:06
training data or in-house ML expertise, code-based approaches, ranging from BigQuery, ML, and Agent Development Kit, ADK, both introduced earlier, to completely custom training.
02:23
Beyond technical expertise, how do you choose the right tool to build an ML model?
02:29
This brief guide comparing four options-- pre-trained APIs, BigQuery ML, AutoML, and custom training may offer some insight.
02:38
BigQuery ML only supports tabular data and semi-structured data like JSON files.
02:44
AutoML supports tabular and image data.
02:48
Whereas the other two support tabular data, images, text, and video.
02:55
Pre-trained APIs also process audio.
02:59
In terms of training data size, pre-trained APIs do not require any training data, whereas BigQuery ML and custom training require a large amount of data.
03:08
Pre-trained APIs and AutoML are user-friendly, with low requirements for machine learning and coding expertise.
03:15
Whereas custom training has the highest requirement, and BigQuery ML requires you to understand SQL.
03:21
At the moment, you can't tune the hyperparameters with pre-trained APIs or AutoML.
03:26
However, you can experiment with hyperparameters by using BigQuery ML and custom training.
03:31
Pre-trained APIs require no time to train a model, because they directly use pre-trained models from Google.
03:37
The time to train the model for the other three options depends on the specific project.
03:41
Normally, custom training takes the longest time because it builds the ML model from the beginning, unlike AutoML and BigQuery ML.
03:50
The best option depends on your business needs and ML expertise.
03:54
Budget is also an important consideration.
03:56
Visit Google Cloud's website for detailed pricing information.
04:00
If you have little ML experience and no intention to train your own ML models, using pre-trained APIs might be the best choice.
04:07
Pre-trained APIs address common perceptual tasks such as vision, video, and natural language.
04:14
They are ready to use without any model development effort.
04:17
If your data engineers, scientists, or analysts are familiar with SQL and already have data in BigQuery, BigQuery ML lets you use SQL queries to build pre-defined ML models.
04:28
If you wish to build custom models with your own training data while you spend minimal time coding, then AutoML on Vertex AI is your choice.
04:36
AutoML allows you to focus on business problems instead of the underlying model architecture and provisioning.
04:43
If your ML engineers and data scientists want full control of the ML workflow, Vertex AI custom
04:48
training lets you train and serve custom models with code on Vertex AI Workbench or Colab Enterprise.
04:57
Before delving into these options, the next lesson will introduce Vertex AI, Google Cloud's AI development platform.