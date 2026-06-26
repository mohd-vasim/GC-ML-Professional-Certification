SPEAKER: In the previous module, you learned about different options to develop an AI project on Google Cloud from a ready
00:06
to use approach like pre-trained APIs to low or no-code solutions like AutoML, and to DIY solutions such as custom training.
00:17
Then how do you build an ML model step by step?
00:21
You'll find out in this module.
00:23
You begin with an overview of the ML workflow.
00:27
Then dive into each of the three workflow stages from data preparation to model development, and finally, model serving.
00:35
Next, you investigate Machine Learning Operations, or MLOps, which takes ML models from development to production in the back end.
00:45
You'll be shown an example of how to build a pipeline to automate the production using Vertex AI pipelines.
00:52
A hands-on lab will then help you walk through the three stages to build an ML model with AutoML on Vertex AI.
01:00
Gaining a solid grasp of ML terminology requires a clear understanding of how a neural network learns.
01:07
This module offers an optional lesson that delves into the neural networks learning process, along with the key terminologies.
01:14
If you're already familiar with the ML theories, feel free to skip this lesson.
01:19
Let's get started with the ML workflow.
01:22
Building an ML model is actually not too different from serving food in a restaurant.
01:27
You start by preparing raw ingredients and finish by serving the dishes on the table.
01:33
There are three main stages to the ML workflow with Vertex AI.
01:37
The first stage is data preparation, which includes two steps, data uploading and feature engineering.
01:44
A model needs a large amount of data to learn from.
01:47
The quality and quantity of the data decide how much and how well the machine learns.
01:53
The data used in machine learning can be real-time streaming data or batch data.
01:58
The data can also be structured or unstructured.
02:01
Structured data is data that can be easily stored in tables such as numbers and text.
02:07
Unstructured data is data that cannot be easily stored in tables such as images and videos.
02:13
The second stage of the ML workflow is model development.
02:17
A model needs a tremendous amount of iterative training.
02:20
This is when training and evaluation form a cycle to train a model, then evaluate the model, and then train the model some more.
02:29
The third and final stage is model serving.
02:32
A model needs to actually be used in order to predict results.
02:36
This is when the machine learning model is deployed and monitored.
02:40
If you don't move an ML model into production, it has no use and remains only a theoretical model.
02:46
Compare this process to serving food in a restaurant.
02:49
Data preparation is when you prepare the raw ingredients.
02:53
Model development is when you experiment with different recipes, and model serving is when you finalize the menu to serve the meal to customers.
03:01
Now, it's important to note that an ML workflow isn't linear, it's iterative.
03:06
For example, during model training, you might need to return to the raw data and generate more useful features to feed the model.
03:13
When monitoring the model during model serving, you might find data drifting or the accuracy of your prediction might suddenly drop.
03:21
You might need to check the data sources and adjust the model parameters.
03:25
Fortunately, these steps can be automated with MLOps.
03:29
You'll learn more about this later in this module.
03:32
Although the main stages remain the same, you have two options to set up the workflow with Vertex AI.
03:39
The first choice is to use AutoML, a no-code solution that lets you build an ML model through UI.
03:46
It's user friendly and doesn't require a lot of ML expertise.
03:50
Also, no coding skills are needed.
03:52
Alternatively, you can code the workflow with Vertex AI Workbench or Colab using Vertex AI Pipelines.
04:00
Vertex AI Pipelines is essentially a toolkit that includes pre-built SDKs, or Software Development Kits, which are the building blocks of a pipeline.
04:10
Coding the pipeline is a good option if you're an experienced ML engineer or data scientist, and want to automate the workflow programmatically.
04:18
Let's focus on AutoML first and then explore the code-based approach later in this module.