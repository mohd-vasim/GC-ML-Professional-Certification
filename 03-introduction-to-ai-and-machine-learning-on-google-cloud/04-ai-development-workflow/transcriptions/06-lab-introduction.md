SPEAKER: Apply your new skills in an optional hands-on lab designed for practical experience.
00:05
While encouraged, completing this lab won't affect your course completion status.
00:11
In this lab, you'll use AutoML, a no-code tool, to build a machine learning model to predict loan risk.
00:18
The data set used in the lab relates to loans from a financial institution and has 2,050 data points.
00:24
AutoML requires at least 1,000 data points in a data set.
00:29
The goal is to practice working through the three phases of the machine learning workflow-- data preparation, model development, and model serving.
00:39
Before you start the lab, let's explain the details about model evaluation so that you can interpret the training results.
00:46
Let's start with the confusion matrix.
00:48
You will get a similar result like this in the lab.
00:51
Pause for a second and try to interpret this matrix yourself.
00:55
What does it tell you?
00:59
100% true positive rate.
01:02
The positive class here is 'repay' (0), the desired business outcome.
01:07
This 100% means that the model is perfect at identifying everyone who will actually repay their loan.
01:15
It never misses a good, safe customer.
01:18
That’s a fantastic outcome for maximizing business opportunities.
01:22
Note that the True Positive Rate equals True Positives divided by the sum of True Positives and False Negatives.
01:31
If the terms sound unfamiliar, please refer to the previous example, where you learned about the confusion matrix.
01:39
87% true negative rate.
01:42
The negative class is 'not repay' (1), the high-risk outcome.
01:47
This 87% means that the model correctly identifies 87% of all the people who are actually defaulters.
01:55
This is a strong result for risk management, as the bank successfully catches and rejects most of the high-risk applications.
02:03
Note that the True Negative Rate equals True Negatives divided by the sum of False Positives and True Negatives.
02:11
13% false positive rate.
02:13
A 'False Positive' is the most expensive mistake.
02:17
The model predicts the customer is safe ('repay' or
02:20
0) when they would have actually defaulted ('not repay' or 1).
02:25
This means that 13% of people who will actually default on their loan are mistakenly approved.
02:32
This directly leads to financial loss for the bank.
02:36
Note that the False Positive Rate equals False Positives divided by the sum of False Positives and True Negatives.
02:44
Finally, 0% false negative rate.
02:48
A 'False Negative' is the error where the model predicts risk ('not repay' or
02:52
1) when the customer would have been safe ('repay' or 0).
02:57
Since this rate is 0%, the model never incorrectly rejects a customer who is actually a safe borrower.
03:05
The bank avoids all lost business opportunity from turning away good customers.
03:11
This perfect rate for customer acceptance is a core strength, despite the trade-off of approving some bad loans seen in the False Positive rate.
03:20
Let's look at the precision recall curve you will encounter in the upcoming AutoML lab.
03:25
The confidence threshold determines how a machine learning model counts the positive cases.
03:30
A higher threshold increases the precision but decreases recall.
03:35
A lower threshold decreases the precision but increases recall.
03:39
Moving the confidence threshold to 0 produces the highest recall of 100% and the lowest precision of 50%.
03:47
So what does that mean?
03:49
That means the model predicts that 100% of loan applicants will be able to repay a loan they take out.
03:55
However, actually, only 50% of people were able to repay the loan.
04:00
Using this threshold to identify the default cases in this example can be risky because it means you can only get half of the loan investment back.
04:09
Now, let's view the other extreme by moving the threshold to 1.
04:12
This will produce the highest precision of 100% with the lowest recall of 1%.
04:17
What does this mean?
04:19
It means that of all the people who were predicted to repay the loan, 100% of them actually did.
04:25
However, you rejected 99% of loan applicants by only offering loans to 1% of them.
04:31
That's a pretty big business loss for your company.
04:34
These are both extreme examples, but it's important that you always try to set an appropriate threshold for your model.
04:40
Now that we've made a review, let's start the lab.