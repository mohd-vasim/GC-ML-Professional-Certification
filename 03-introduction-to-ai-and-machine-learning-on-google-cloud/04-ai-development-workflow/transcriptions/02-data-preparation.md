SPEAKER: Let's start with the first stage of ML workflow, data preparation.
00:05
During this stage, you must upload data and then prepare it for model training with feature engineering.
00:12
The data can come from Cloud Storage, BigQuery, or even your local machine.
00:17
AutoML now mainly supports tabular data by solving different types of problems called objectives.
00:24
For tabular data, you can train the model to solve regression, classification, or forecasting problems.
00:31
Forecasting is vital to many industries like retail.
00:35
To learn more about how to build a forecasting model, please check the course titled Introduction to Vertex Forecasting and Time Series in Practice in the reading list.
00:46
After the data is uploaded to AutoML, the next step is preparing it for model training with feature engineering.
00:53
Imagine you're preparing a meal.
00:55
Your data is like your ingredients, such as carrots, onions, and tomatoes.
01:00
Before you start cooking, you'll need to peel the carrots, chop the onions, and rinse the tomatoes.
01:06
This is what feature engineering is like.
01:08
The data must be processed before the model starts training.
01:12
A feature refers to a factor that contributes to the prediction.
01:16
It's like an independent variable in statistics or a column in a table.
01:21
Preparing features can be both challenging and tedious.
01:26
To help, Vertex AI provides a service called Vertex AI Feature Store, which is a centralized repository to manage, serve, and share features.
01:36
It aggregates the features from different sources in BigQuery and makes them available for both real-time, often called online, and batch, often called offline serving.
01:46
Vertex AI automates the feature aggregation to scale the process with low latency.
01:52
Additionally, Vertex AI Feature Store is ready for generative AI.
01:56
It can manage and serve embeddings, which are the data sources in Gen AI.
02:01
It also supports retrieving similar items in real time, ensuring low latency.
02:07
The workflow of serving real-time, online features with Vertex AI Feature Store can be summarized as follows.
02:14
One-- prepare the data source in BigQuery. Two-- optional, register the data sources by creating feature groups and features.
02:23
Three-- configure the connection by creating a feature view to define which features to copy from your data source into the online store for real-time serving.
02:34
Four-- serve the latest feature values online from a feature view.
02:39
So what are the benefits of Vertex AI Feature Store?
02:43
First, features are shareable for training and serving.
02:46
They are managed and served from a central repository, maintaining consistency across your organization.
02:53
Second, features are reusable.
02:55
This helps to save time and reduces duplicated efforts.
02:59
Third, features are scalable.
03:01
They automatically scale to provide low-latency serving, so you can focus on developing the logic to create them without worrying about deployment.
03:10
And fourth, features are easy to use.
03:13
Vertex AI Feature Store is built on an easy-to-navigate user interface.