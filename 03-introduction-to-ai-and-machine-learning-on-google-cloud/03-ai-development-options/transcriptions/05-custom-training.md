SPEAKER: In previous lessons, you learned about no-code solutions like AutoML and low-code solutions like pre-trained APIs.
00:08
Now let's explore a code-based solution, custom training, a do-it-yourself approach to building an ML model.
00:15
While AutoML UI offers significant convenience and pre-trained APIs eliminate the need for training data, you might require custom training if your unique needs extend beyond AutoML's automated capabilities.
00:29
This is when complete control and flexibility over the model architecture, frameworks, and training logic become essential.
00:37
Before any coding begins, you must determine what environment you want your ML training code to use.
00:43
There are two options, a pre-built container or a custom container.
00:49
A pre-built container is like a furnished kitchen with cabinets, appliances, and cookware.
00:55
So if your ML training needs a platform like Python, TensorFlow, and PyTorch, and you're not particular about the underlying infrastructure to
01:02
run on or, to use our kitchen analogy, which oven or knife you use, a pre-built container is probably your best choice.
01:12
A custom container, alternatively, is like an empty room.
01:16
You define the exact appliances and tools that you prefer to cook with.
01:21
That means you must determine the details like the environment, machine type, and disks when creating the custom container.
01:28
In terms of the tools to code your ML model, you can use Vertex AI Workbench.
01:34
You can think of Vertex AI Workbench as Jupyter Notebook deployed in a single development environment that
01:39
supports the entire data science workflow, from exploring to training, and then deploying a machine learning model.
01:47
You can also use Colab Enterprise, which was integrated into Vertex AI platform in 2023 so data scientists could code in a familiar environment.
01:57
After you decide the working environment, the next step is to start writing code.
02:02
These days, you don't have to code from scratch.
02:05
Instead, you can leverage ML libraries.
02:08
An ML library is a collection of pre-written code that can be used to perform machine learning tasks.
02:14
These libraries can save developers time and effort by providing them with the tools they need to build machine learning models without having to write everything from the beginning.
02:24
As a data scientist, you might already be familiar with popular ML libraries, like TensorFlow, scikit-learn, and PyTorch.
02:32
They are open-source and widely used by a large community of users and developers.
02:37
Let's explore TensorFlow, an end-to-end open platform for machine learning supported by Google.
02:43
TensorFlow contains multiple abstraction layers.
02:46
You use TensorFlow APIs to develop and train ML models.
02:51
The TensorFlow APIs are arranged hierarchically, with the high-level APIs built on the low level APIs.
02:58
The lowest layer is hardware.
03:00
TensorFlow can run on different hardware platforms, including CPU, GPU, and TPU.
03:07
The next layer is the low-level TensorFlow APIs where you can write your own operations in C++ and call the core, basic, and numeric processing functions written in Python.
03:18
The third layer is the TensorFlow model libraries, which provide the building blocks, such as neural network layers and evaluation metrics to create a custom ML model.
03:28
The high-level TensorFlow APIs like Keras sit on top of this hierarchy.
03:33
They hide the ML building details and automatically deploy the training.
03:37
They can be your most used APIs.
03:40
Note that Vertex AI fully hosts TensorFlow from low-level to high-level APIs.
03:46
Regardless of which abstraction level you are writing your TensorFlow code at, Vertex AI gives you a managed service.
03:53
Now let's look at an example of using tf.keras, a commonly used, high-level TensorFlow library to build a simple regression model.
04:02
Typically, it takes three fundamental steps.
04:05
In step 1, you create a model where you piece together the layers of a neural network.
04:10
In step 2, you compile the model where you specify hyperparameters, such as performance evaluation and model optimization.
04:18
Finally, you train your model to find the best fit.
04:21
Assume you already imported necessary packages like TensorFlow and uploaded the data.
04:26
The first step is to create a model by using tf.keras.sequential.
04:31
To demonstrate, you can define your model as a three-layer neural network.
04:36
You'll explore more details about neural networks such as activation functions in the next module.
04:41
The next step is to compile the model by specifying how you want to train it by using the method compile.
04:48
For instance, you can decide how to measure the performance by specifying a loss function.
04:53
You can also optimize the training by pointing to an optimizer.
04:57
The last step is to train the model by using the method fit.
05:01
For instance, you can define the input, the training data and the output, the predicted results.
05:07
You can also decide how many iterations you want to train the model by specifying the numbers of epochs.
05:13
After you train the model and are satisfied with the performance, you can then deploy the model and make predictions.
05:19
Apart from TensorFlow, Google is consistently introducing new frameworks.
05:24
One of the most promising frameworks is JAX.
05:27
JAX is a high-performance numerical computation library that is highly flexible and easy to use.
05:33
It offers new possibilities for both research and production environments.