SPEAKER: Let's focus on the third stage of the ML workflow, model serving.
00:05
The recipes are ready, and now it's time to serve the meal.
00:09
This represents the final stage of the machine learning workflow, model serving.
00:14
Model serving consists of two steps-- first, model deployment, which you can compare to serving a meal to a hungry customer; and second, model monitoring, which is like
00:25
checking with the waitstaff to ensure that the restaurant is operating efficiently. It's important to note that model management exists throughout this whole workflow to manage the underlying machine
00:36
learning infrastructure. This lets data scientists focus on what to do and not on how to do it. Let's start with model deployment, which is the exciting time when
00:46
the model is implemented and ready to serve. You have two primary options. Option one-- deploy the model to an endpoint for real-time predictions, or often called online predictions.
01:00
This option is best when immediate results with low latency are needed, such as making instant recommendations based on a user's browsing habits whenever they're online.
01:10
A model must be deployed to an endpoint before it can be used to serve real-time predictions.
01:16
Option two-- request the prediction job directly from the model resource for batch prediction.
01:22
This option is best when no immediate response is required, for example, sending out marketing campaigns
01:28
every other week based on the user's recent purchasing behavior, and what's currently popular on the market.
01:34
Batch prediction does not require deploying the model to an endpoint.
01:38
You can deploy a model either using the UI on Vertex AI or using code by calling APIs.
01:45
You'll practice building an endpoint later in the lab.
01:48
Beyond making predictions in the Cloud, deploying the model off cloud with edge computing is also possible.
01:55
This approach is generally adopted when the model needs to be deployed in a specific environment to mitigate latency, ensure privacy, or enable offline functionality.
02:05
For instance, consider an IoT application like object detection that utilizes a camera feed in a manufacturing plant.
02:13
In such a use case, the added latency of relying on the cloud can be impractical.
02:18
Once the model is deployed and begins making predictions or generating contents, it's important to monitor its performance.
02:25
The backbone of automating ML workflow on Vertex AI is a toolkit called Vertex AI Pipelines.
02:31
It automates, monitors, and governs machine learning systems by orchestrating the workflow in a serverless manner.
02:39
Imagine you're in a production control room, and Vertex AI Pipelines is displaying the production data onscreen.
02:45
If something goes wrong, it automatically triggers and displays a warning based on a predefined threshold.
02:51
With Vertex AI Workbench and Colab Enterprise, which are notebook tools, you can define your own pipeline using SDKs.
02:59
You can do this with pre-built pipeline components, which means that you primarily need to specify how the pipeline is put together using components as building blocks.
03:08
You'll explore more details about Vertex AI pipelines in the next lesson.
03:13
And it's with these final two steps, model deployment and model monitoring, that you complete the exploration of the machine learning workflow.
03:21
The restaurant is open and operating smoothly.
03:24
Bon appetit.