SPEAKER: Let's advance to the second stage, model development, where you train the model and evaluate the result.
00:08
Now that our data is ready, which, if you return to the cooking analogy, is the ingredients, it's time to train the model.
00:15
This is like experimenting with recipes.
00:17
This stage involves two steps, model training, which is like cooking the recipe, and model evaluation, which is like testing how good the meal is.
00:27
This process might be iterative.
00:30
To set up an ML model, you need to specify a few things.
00:34
Please note that the user interface may not be exactly the same, as the product is evolving rapidly.
00:40
However, similar features will remain.
00:43
First of all is the training method, where you tell Vertex AI the data set you just uploaded from the preparation stage.
00:50
Depending on the data type, whether it is tabular, image, text, or video, you specify the training objective.
00:58
This is the goal of the model training and the task you want to solve.
01:03
Then you choose the training method, AutoML, without code, or custom training, using code.
01:10
The next step is to determine the training details.
01:13
For example, if you are training the model to solve a supervised learning problem, such as regression and classification, you must choose the target column from your data set.
01:24
In Training Options, you can choose certain features to participate in the training and transform the data type if needed.
01:31
Finally, you specify the budget and pricing and then click Start Training.
01:36
AutoML will train the model for you and choose the best performed models among thousands of others.
01:43
Do you recall the powerful technologies behind AutoML?
01:47
Right.
01:47
The credit there goes to neural architecture search and transfer learning.
01:52
While you were experimenting with a recipe, you need to keep tasting it to ensure that it meets expectations.
01:59
This is the evaluation portion of the model development stage.
02:03
Vertex AI provides extensive evaluation metrics to help determine a model's performance.
02:10
Let's focus on the metrics of recall and precision when evaluating the performance of classification models.
02:16
To do this, you'll use a confusion matrix.
02:19
A confusion matrix is a specific performance measurement for machine learning classification problems.
02:26
It's a table with combinations of predicted and actual values.
02:30
To keep things simple, we assume the output includes only two classes.
02:36
Let's explore an example.
02:38
The first is true positive, which can be interpreted as the model predicted positive, and that's true.
02:45
The model predicted that this is an image of a cat, and it actually is.
02:50
The opposite of that is true negative, which can be interpreted as the model predicted negative, and that's true.
02:58
The model predicted that the image is not a cat, and it actually isn't.
03:02
Then there is false positive, otherwise known as a type I error, which can be interpreted as the model predicted positive, and that's false.
03:12
The model predicted that the image is a cat, but it actually isn't.
03:17
Finally, there is false negative, otherwise known as a type II error, which can be interpreted as the model predicted negative, and that's false.
03:27
The model predicted that the image is not a cat, but it actually is.
03:32
A confusion matrix is the foundation for many other metrics used to evaluate the performance of a machine learning model.
03:39
Let's look at the two popular metrics, recall and precision, that you will encounter in the lab.
03:46
Recall refers to all the positive cases and looks at how many were predicted correctly.
03:51
This means that recall is equal to the true positives divided by the sum of true positives and false negatives.
03:59
Precision refers to all the cases predicted as positive and how many are actually positive.
04:05
This means that precision is equal to the true positives divided by the sum of the true positives and false positives.
04:12
Precision and recall are often a trade off.
04:15
Depending on your use case, you might need to optimize for one or the other.
04:20
Consider a classification model where Gmail separates emails into two categories, spam and not spam.
04:28
If the goal is to catch as many potential spam emails as possible, Gmail might want to prioritize recall.
04:35
In contrast, if the goal is to only catch the messages that are definitely spam without blocking other emails, Gmail might want to prioritize precision.
04:45
Vertex AI visualizes the precision recall curve, so it can be adjusted based on the problem that needs to be solved.
04:52
You'll get the opportunity to practice adjusting precision and recall in the AutoML lab.
04:59
In addition to the confusion matrix and the metrics generated to measure recall and precision, the other useful measurement is feature importance.
05:08
In Vertex AI, feature importance is displayed through a bar chart to illustrate how each feature contributes to a prediction.
05:15
The longer the bar or the larger the numerical value associated with the feature, the more important it is.
05:21
This information helps decide which features are included in a machine learning model to predict the goal.
05:27
You will observe the feature importance chart in the lab, as well.
05:31
Feature importance is just one example of Vertex AI's comprehensive machine learning functionality called explainable AI.
05:39
Explainable AI is a set of tools and frameworks to help understand and interpret predictions made by machine learning models.
05:47
Please check the reading list if you want to know about explainable AI on Google Cloud.