SPEAKER: To understand machine learning, you must first understand how neural networks learn.
00:05
This includes exploring this learning process and the terms associated with it.
00:10
If you are already familiar with the ML theories and terminologies, feel free to skip this lesson.
00:16
How do machines learn?
00:18
And how do they assess their learning?
00:21
Before you dive into building an ML model, let's take a look at how a neural network learns.
00:27
You may already know about various neural networks, such as Deep Neural Networks, or DNN, Convolutional
00:32
Neural Networks, or CNN, Recurrent Neural Networks, or RNN, and more recently, Large Language Models, or LLMs.
00:43
These networks are used to solve different problems.
00:46
All of these models stem from the most basic, Artificial Neural Network, or ANN.
00:53
ANNs are also referred to as neural networks or shallow neural networks.
00:58
Let's focus on ANN to see how a neural network learns.
01:03
An ANN has three layers-- an input layer, a hidden layer, and an output layer. Each node represents a neuron. The lines between neurons stimulate
01:14
synopsys, which is how information is transmitted in a human brain. For instance, if you input article titles from multiple resources, the neural network can tell
01:23
you which media outlet or platform the article belongs to, such as GadgeHub, Daily Insight, and DevStream. How does an ANN learn from examples and
01:34
then make predictions? Let's examine how it works in depth. Let's assume you have two input neurons or nodes-- one hidden neuron and one output neuron.
01:46
Above the link between neurons are weights.
01:49
The weights retain information that a neural network learned through the training process.
01:54
They are the mysteries that a neural network aims to discover.
01:58
The first step is to calculate the weighted sum.
02:01
This is done by multiplying each input value by its corresponding weight and then summing the products.
02:07
It normally includes a bias component, bi.
02:10
However, to focus on the core idea, ignore it for now.
02:14
The second step is to apply an activation function to the weighted sum.
02:18
What is an activation function?
02:21
And why do you need it?
02:23
Let's pause your curiosity for just a moment and get back to that soon.
02:27
In the third step, the weighted sum is calculated for the output layer, assuming multiple neurons in the hidden layers.
02:34
The fourth step is to apply an activation function to the weighted sum.
02:38
This activation function can be different from the one applied to the hidden layers.
02:43
The result is the predicted y, which consists of the output layer.
02:47
You use y-hat to represent the predicted result and y as the actual result.
02:53
Now let's get back to activation functions.
02:55
What does an activation function do?
02:58
Well, an activation function is used to prevent linearity or add non-linearity.
03:04
What does that mean?
03:05
Think about a neural network.
03:07
Without activation functions, the predicted result, y-hat, will always be a linear function of the input, x, regardless of the number of layers between input and output.
03:18
Let's walk through this for clarity.
03:20
Without the activation function, the value of the hidden layer, h, equals a total of w1 times x1 and w2 times x2.
03:29
Please note that, to make this illustration easy, we ignored the bias component, b, which you often see in other ML materials.
03:36
The output, y-hat, therefore equals to w3 times h and eventually equals to a total of constant number, a, times x1 and a constant number, b, times x2.
03:47
In other words, the output, y, is a linear combination of the input,
03:51
x. If y is a linear function of x, you don't need all the hidden layers, but only one input and one output.
04:00
You might already know that linear models do not perform well when handling comprehensive problems.
04:05
That's why you must use activation functions to convert a linear network to a nonlinear one.
04:11
What are the widely used activation functions?
04:14
You can use the Rectified Linear Unit, or ReLU function, which turns an input value to 0 if it's negative or keeps the original value if it's positive.
04:24
You can use the sigmoid function, which turns the input to a value between 0 and 1-- and hyperbolic
04:31
tangent, or tanh function, which shifts the sigmoid curve and generates a value between minus 1 and plus 1.
04:41
Another interesting and important activation function is called softmax.
04:46
Think about sigmoid.
04:48
It generates a value from 0 to 1 and is used for binary classification and logistic regression models.
04:54
An example for this would be deciding whether an email is spam.
04:58
What if you have multiple categories, such as GadgeHub, Daily Insight, and DevStream?
05:04
Here you must use softmax, which is the activation function for multi-class classification.
05:10
It maps each output to a 0, 1 range in a way that the total adds up to 1.
05:15
Therefore, the output of softmax is a probability distribution.
05:20
Skipping the math, you can conclude that softmax is used for multi-class classification.
05:25
Whereas, sigmoid is used for binary class classification and logistic regression models.
05:31
Also note that you don't need to have the same activation function across different layers.
05:36
For instance, you can have ReLU for hidden layers and softmax for the output layer.
05:41
Now that you understand the activation function and get a predicted y, how do you know if the result is correct?
05:48
You use an assessment called loss function or cost function to measure the difference between the predicted y and the actual
05:54
y. Loss function is used to calculate errors for a single training instance.
06:00
Whereas, cost function is used to calculate errors from the entire training set.
06:05
Therefore, in step 5, you calculate the cost function to minimize the difference.
06:09
If the difference is significant, the neural network knows that it did a bad job in predicting and must go back to learn more and adjust parameters.
06:19
Many different cost functions are used in practice.
06:22
For regression problems, Mean Squared Error, or MSE, is a common one used in linear regression models.
06:29
MSE equals the average of the sum of squared differences between y-hat and
06:32
y. For classification problems, cross-entropy is typically used to measure the difference between the predicted and actual probability distributions in logistic regression models.
06:45
If the difference between the predicted and actual results is significant, you must go back to adjust weights and biases to minimize the cost.
06:53
This potential sixth step is called backpropagation.
06:57
The challenge now is how to adjust the weights.
07:00
The solution is slightly complex but, indeed, the most interesting part of a neural network.
07:06
The idea is to take cost functions and turn them into a search strategy.
07:11
That's where gradient descent comes in.
07:13
Gradient descent refers to the process of walking down the surface formed by the cost function and finding the bottom.
07:21
It turns out that the problem of finding the bottom can be divided into two different and important questions.
07:27
The first one is, which direction should you take?
07:32
The answer involves the derivative.
07:34
Let's say you start from the top left.
07:36
You calculate the derivative of the cost function and find its negative.
07:40
This means the angle of the slope is negative, and you are on the left side of the curve.
07:44
To get to the bottom, you must go down and right.
07:48
Then, at one point, you're on the right side of the curve.
07:51
And you calculate the derivative again.
07:53
This time, the value is positive.
07:55
And you must slide again to the left.
07:57
You calculate the derivative of the cost function every time to decide which direction to take.
08:02
Repeat this process, according to gradient descent, and you will eventually reach the regional bottom.
08:09
The second question in finding the bottom is, what size should the steps be?
08:14
The step size depends on the learning rate, which determines the learning speed of how fast you bounce around to reach the bottom.
08:21
Step size or learning rate is a hyperparameter that is set before training.
08:26
If the step size is too small, your training might take too long.
08:30
If the step size is too large, you might bounce from wall to wall or even bounce out of the curve entirely without converging.
08:38
When step size is just right, you're set.
08:41
The seventh and last step is iteration.
08:44
One complete pass of the training process from step 1 to step 6 is called an epoch.
08:49
You can set the number of epochs as a hyperparameter in training.
08:53
Weights or parameters are adjusted until the cost function reaches its optimum.
08:58
You can tell that the cost function has reached its optimum when the value stops decreasing, even after many iterations.
09:06
This is how a neural network learns.
09:08
It iterates the learning by continuously adjusting weights to improve behavior until it reaches the best result.
09:15
This is similar to a human learning lessons from the past.
09:19
We have illustrated a simple example with two input neurons, or nodes-- one hidden neuron, and one output neuron.
09:27
In practice, you might have many neurons in each layer.
09:30
Regardless of the number of neurons in the input, hidden, and output layer, the fundamental process of how a neural network learns remains the same.
09:40
Learning about neural networks can be exciting, but also overwhelming with the large number of new terms.
09:46
Let's take a moment to review them.
09:48
In a neural network, weights and biases are parameters learned by the machine during training.
09:53
You have no control of the parameters except to set the initial values.
09:58
The number of layers, and neurons, activation functions, learning rate, and epochs are hyperparameters, which are decided by a human before training.
10:07
The hyperparameters determine how a machine learns.
10:10
For example, the learning rate decides how fast a machine learns.
10:14
And the number of epochs defines how many times the learning iterates.
10:18
Normally, data scientists choose the hyperparameters and experiment with them to find the optimum combination.
10:24
However, if you use a tool like AutoML, it automatically selects the hyperparameters for you and saves you plenty of experiment time.
10:33
You also learned about cost or loss functions, which are used to measure the difference between the predicted and actual value.
10:39
They are used to minimize error and improve performance.
10:43
You use backpropagation to modify the weights and bias if the difference is significant and gradient descent to decide how to tune the weights and bias and when to stop.
10:52
Mastering these foundational concepts is your first step toward building powerful ML models.
10:59
You'll constantly apply them when moving from theory to practice.