SPEAKER: In this lesson, you explore an advanced topic, MLOps and workflow automation.
00:06
You learned from the previous lessons to build an ML model through three main stages-- data preparation, model development, and model serving.
00:15
You have two approaches to build an end-to-end workflow.
00:18
One is codeless through Google Cloud Console, like AutoML on Vertex AI.
00:24
But what if you want to automate this workflow to achieve continuous integration, training, and delivery?
00:30
Here comes the other option, to code a pipeline that automates the ML workflow.
00:35
Machine learning operations, or MLOps, play a big role.
00:38
MLOps combines machine learning development with operations and applies similar principles from DevOps, or Development Operations, to machine learning models.
00:48
MLOps aims to solve production challenges related to machine learning.
00:52
In this case, this refers to building an integrated machine learning system and operating it in production.
00:58
These are considered to be some of the biggest pain points by the ML practitioners community, because both data and code are constantly evolving in machine learning.
01:06
Practicing MLOps means automating and monitoring each step of the ML system construction to enable continuous integration, training, and delivery.
01:16
The backbone of MLOps on Vertex AI is a toolkit called Vertex AI Pipelines.
01:23
This toolkit supports both Kubeflow Pipelines, or KFP, and TensorFlow Extended, or TFX.
01:31
If you already use TensorFlow to build ML models that process terabytes of structured data, it makes sense to use TFX and turn that code into an ML pipeline.
01:40
Otherwise, KFP can be a good alternative.
01:44
Learn more about how to choose between the Kubeflow Pipelines SDK and TFX from the reading list.
01:51
An ML pipeline contains a series of processes and runs in two different environments.
01:57
First is the experimentation, development, and test environment.
02:00
And second is the staging, pre-production, and production environment.
02:05
In the development environment, you start from data preparation, which includes data extraction, analysis, and preparation, to model development like training, evaluation, and validation.
02:15
The result is a trained model that can be entered in the model registry.
02:19
Once the model is trained, the pipeline moves to the staging and production environment, where you serve the model, which includes prediction and monitoring.
02:28
Each of these processes can be a pipeline component, which is a self-contained set of code that performs one task of a workflow.
02:34
You can think of a component as a function, which is a building block of a pipeline.
02:39
You can either build a custom component on your own, or leverage the pre-built components provided by Google.
02:45
If you want to accomplish a specific task to tailor your ML workflow, such as determining a special threshold for model deployment, you may need to code a custom component.
02:54
Before doing so, check the pre-built components offered by Google Cloud.
02:58
You may find a pipeline component to reuse or customize to suit your needs.
03:02
Learn more about using Google Cloud pipeline components in your pipeline in the reading list.
03:07
All these components are like pieces on an ML pipeline.
03:10
You need to assemble them together to automate the entire ML workflow.
03:14
Organizations often implement ML automation in three phases.
03:18
Phase 0 is the starting point where you have not configured any MLOps.
03:22
You typically use the graphical user interface or GUI-based workflow, such as AutoML for training, deployment, and serving.
03:32
Phase 0 is critical because it helps you build an end-to-end workflow manually before you automate it.
03:38
In Phase 1, you start automating your ML workflow by building components using the Vertex AI pipelines' SDKs.
03:45
An example of a component would be the training pipeline.
03:47
It is in this phase that you develop the building blocks for future use.
03:51
In phase 2, you integrate the separate components to form an entire workflow and to achieve CI, CT and CD.
03:59
Let's look at an example.
04:01
Assume you want to build a pipeline to train, evaluate, and deploy an AutoML model that classifies beans into one of seven types based on their characteristics.
04:09
You have two main steps-- build a pipeline and then run it.
04:14
To build a pipeline, you first plan it as a series of components, which can be a combination of custom and pre-built.
04:19
To promote reusability, each component should have a single responsibility.
04:24
Second, you build any custom components that are needed.
04:27
For example, you create a component called classification model eval metrics.
04:32
You use this component to compare the evaluation metrics to a threshold after the model is trained and determine whether the model should be deployed.
04:40
If the model performs well, you deploy it.
04:42
Otherwise, you retrain the model.
04:45
Third, you assemble the pipeline by adding pre-built components.
04:48
For example, TabularDatasetCreateOp creates a tabular data set in Vertex AI, given a data set source, either in Cloud Storage or BigQuery.
04:57
AutoMLTabularTrainingJobRunOp kicks off an AutoML training job for a tabular data set.
05:03
EndpointCreateOp creates an endpoint in Vertex AI.
05:06
And ModelDeployOp deploys a given model to an endpoint in Vertex AI.
05:11
You also include a custom component from the previous step, classification model eval metrics, to compare the performance of the trained model to a threshold.
05:19
After the pipeline is built, you must compile and run it.
05:22
First you compile it using the compiler, compiler.Compiler.compile, or compile commands.
05:28
And then you define and run the pipeline job.
05:31
The good news is you don't have to create a pipeline from the beginning.
05:35
Vertex AI provides a few templates, like the one for classification or regression of tabular data with AutoML to help you start your journey.
05:43
Now you have an automated pipeline to train, evaluate, and deploy an ML model.
05:48
This pipeline will check the performance of the model constantly and decide whether it should be deployed or retained without your intervention.
05:55
The nice thing is that Google Cloud also visualizes the pipeline based on the coding, with which you can easily check the components and the corresponding artifacts.
06:04
This example demonstrated the overall process to build a pipeline.
06:08
To know more about pipeline details, please practice with the coding example in the demo, "Introduction to Vertex AI Pipelines," which is available in the reading list for this course.