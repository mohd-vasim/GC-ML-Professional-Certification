SPEAKER: In the previous lesson, you learned about Vertex AI, a unified platform that supports both AutoML, a no-code solution, and custom training, a code-based solution.
00:12
In this lesson, you'll explore AutoML in depth, including the technologies used to power automated ML development.
00:21
AutoML, which stands for Automated Machine Learning, aims to automate the process to develop and deploy an ML model.
00:30
If you've worked with AutoML models before, you know that building them can be extremely time consuming because you
00:36
need to repeatedly add new data and features, try different models, and tune parameters to achieve the best result.
00:45
When ML was first announced in January of 2018, the goal was to save the manual
00:50
work from data scientists and automate machine learning pipelines from pre-processing data to model training and deployment.
00:59
Since 2021, AutoML features are embedded in Vertex AI and have become part of the platform.
01:06
But how could this be done?
01:08
How can you trust AutoML to generate the best results without bias and fast?
01:14
Let's look deeper to explore how AutoML works and the main technologies behind it.
01:20
AutoML is powered by the latest research from Google.
01:24
It's an ongoing endeavor.
01:26
There are four distinct phases.
01:28
Phase 1 is data processing.
01:30
After you upload a data set, AutoML provides functions to automate part of the data preparation process.
01:38
For example, it can convert numbers, datetime, text, categories, arrays of categories, and nested fields
01:46
into a certain format of data so that it can be fed into an ML model.
01:51
Phase 2 includes searching the best models and tuning the parameters.
01:57
Two critical technologies support this auto search.
02:00
The first one is called neural architecture search, which helps search the best models and tune the parameters automatically.
02:08
And the second one is called transfer learning, which helps speed the search by using the pre-trained models.
02:14
Let's first look at neural architecture search.
02:17
The goal of neural architecture search is to find optimal models among many options.
02:22
Specifically, AutoML tries different architectures and models and compares the performance of the models to find the best ones.
02:31
For instance, AutoML can search through multiple advanced ML models and automatically tune the parameters to find the best fit for your data.
02:41
Secondly, let's examine transfer learning.
02:44
Machine learning is similar to human learning.
02:47
It learns new things based on existing knowledge.
02:51
AutoML has already trained many different models with large amounts of data.
02:56
These trained models can be used as a foundation model to solve new problems with new data.
03:03
A typical example are Large Language Models or LLMs, which are general purpose and can be pre-trained and fine-tuned for specific purposes.
03:13
LLMs are trained for general purposes to solve common language problems, such as text classification, question answering, document summarization, and text generation across industries.
03:26
The models can then be tailored to solve specific problems in different fields such as retail, finance, and entertainment using a relatively small size of field data sets.
03:38
Transfer learning is a powerful technique that lets people with smaller data sets or less computational power achieve great results by using pre-trained models trained on similar larger data sets.
03:50
Because the model learns through transfer learning, it doesn't have to learn from the beginning, so it can
03:54
generally reach higher accuracy with much less data and computation time than models that don't use transfer learning.
04:03
In phase 3, the best models are assembled from phase 2 and prepared for prediction in phase 4.
04:10
Note that AutoML does not rely on one single model, but on the top number of models.
04:16
The number of models depends on the training budget, but is typically around 10.
04:20
The assembly can be as simple as averaging the predictions of the top number of models.
04:25
Relying on multiple top models instead of one greatly improves the accuracy of prediction.
04:32
By applying these advanced ML technologies, AutoML automates the pipeline from feature engineering to architecture search, to hyperparameter tuning, and to model ensemble.
04:44
It might seem that AutoML can do a better job than a human to find the optimal models that fit your data.
04:51
Perhaps the best feature of AutoML is that it provides a no-code solution.
04:56
You can point and click through a UI to build an ML model with your own data.
05:01
You'll walk through the details from preparing training data to training your model and finally get prediction in the next module.