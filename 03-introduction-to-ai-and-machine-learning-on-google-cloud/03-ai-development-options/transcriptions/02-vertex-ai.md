SPEAKER: Before exploring various options to build an ML model, you first need to familiarize yourself with the playground, Vertex AI, Google's unified AI development platform.
00:11
For years now, Google has invested time and resources into developing data and AI, and applied these technologies to
00:19
many of its products and services like Gmail, Google Maps, Google Photos, and Google Translate, just to name a few.
00:26
But developing these technologies doesn't come without challenges.
00:31
There are challenges around getting ML models into production, for example, scalability, monitoring and continuous integration, delivery and training.
00:41
In fact, according to Gartner, only half of enterprise ML projects get past the pilot phase.
00:48
There are also ease-of-use challenges.
00:50
Many tools on the market require advanced coding skills, which can take a data scientist's focus away from model configuration.
00:58
Without a unified workflow, data scientists often have difficulties finding tools.
01:04
Google's solution to many of the production and ease-of-use challenges is Vertex AI, a unified platform that brings all the components of the machine learning ecosystem and workflow together.
01:16
So what exactly does a unified platform mean?
01:19
There are two primary aspects.
01:21
Firstly, it means that Vertex AI provides an end-to-end ML pipeline to prepare data and create, deploy, and manage models over time and at scale.
01:33
For instance, during the data readiness stage, users can upload data from wherever it's stored, Cloud Storage, BigQuery, or a local machine.
01:42
Then, during the feature readiness stage, users can create features, which are the processed data that will be put into the model.
01:49
Then they can share them with others by using the feature store.
01:53
After that, it's time for training and hyperparameter tuning.
01:57
This means that when the data is ready, users can experiment with different models and adjust hyperparameters.
02:03
And finally, during deployment and model monitoring, users can set up the pipeline to transform the model into production by automatically monitoring and performing continuous improvements.
02:15
You'll learn how to do this later in the course when you explore MLOps.
02:20
Second, Vertex AI is a unified platform that encompasses both generative AI, enabling creation of multimodal content, and predictive AI, allowing for forecasting and classification.
02:33
You already explored Gen AI tools in the previous module like Vertex AI Studio and Agent Builder.
02:40
Let's focus on the tools for predictive AI.
02:43
Vertex AI allows users to build ML models with either AutoML, a no-code solution, or custom training, a code-based solution.
02:53
AutoML provides a UI that is easy to navigate.
02:56
It lets data scientists focus on what business problems to solve, instead of how to code and deploy an ML solution.
03:04
Custom training gives data scientists and ML engineers more control over the development environment and process.
03:11
They can use tools like Vertex AI Workbench and Colab to do their ML projects themselves.
03:17
One convenient feature is that data scientists can now write SQL with Workbench on Vertex AI to seamlessly connect BigQuery and Vertex AI.
03:27
Being able to perform such a wide range of tasks in one unified platform has many benefits.
03:34
This can be summarized with four Ss.
03:36
It's seamless.
03:38
Vertex AI provides a smooth user experience from uploading and preparing data all the way to model training and production.
03:45
It's scalable.
03:47
The Machine Learning Operations, MLOps, provided by Vertex AI help to monitor and manage the ML production, and therefore scale the storage and computing power automatically.
03:58
It's sustainable.
04:00
All of the artifacts and features created using Vertex AI can be reused and shared.
04:06
And it's speedy.
04:07
Vertex AI produces models that have 80% fewer lines of code than competitors.
04:13
Let's take a deep dive into ML model building options in the next lesson.