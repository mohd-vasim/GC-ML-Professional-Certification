SPEAKER: In the previous lesson, Ann experimented with the Vertex AI Studio toolkit to design, evaluate, and manage prompts.
00:08
Now she's ready to deploy the prompt to an application.
00:11
She teams up with Ian, the ML engineer who is responsible for building a pipeline and monitoring performance.
00:17
This brings us to the second half of the prompt-to-production lifecycle, integration and deployment, covering stages from build and test to monitor and optimize.
00:28
Recall that, early in their journey, Bea and Ann quickly tested their ideas by simply clicking Build with Code and then Deploy as App to build their own application.
00:38
However, what if they wanted to customize the application or integrate its features into other applications?
00:44
Vertex AI Studio provides this flexibility by automatically generating the code for you.
00:51
Besides the User Interface, UI, which requires no code to explore and test prompts, Vertex AI Studio offers other low-code approaches to access AI models.
01:02
These are Software Development Kits, or SDKs, in Python, and APIs with cURL.
01:09
Simply click Build with Code to find the code describing the prompt and its parameters.
01:14
Automated code generation simplifies application development.
01:18
Additionally, the integrated development environment with Cloud Run and Cloud Shell streamlines production and removes the need to worry about the underlying cloud architecture that supports application deployment.
01:31
After building your application, continuous monitoring and optimization are key to maintaining high performance.
01:38
But how do you ensure your Gen AI models deliver accurate, up-to-date results?
01:43
One way is through grounding and Retrieval Augmented Generation, or RAG.
01:48
Gen AI models are often pretrained, meaning their responses rely on potentially outdated or inaccurate training data.
01:57
Grounding connects these models to trusted external data sources, ensuring their answers are verified against the latest information.
02:05
RAG is a method for implementing this idea.
02:08
Think of grounding as the what and RAG as the how.
02:13
When constructing your prompt with Vertex AI Studio, you can choose to ground the results either through Google
02:19
real-time search for the most current information or your own data to instruct the AI with field-specific knowledge.
02:26
To further your knowledge of these advanced technologies, we recommend our courses Create Embeddings-- vector search and RAG with BigQuery and Vector Search and Embeddings with Vertex AI.
02:40
These courses introduce how to implement RAG pipelines with Google's two widely used platforms, BigQuery and Vertex AI, respectively.
02:50
You can scan the QR code on the screen or find the link in your reading list.
02:55
Other than fact-checking using grounding and RAG, what if you want to improve the quality of content generation itself?
03:03
That's where model tuning comes in.
03:04
It's another way to enhance Gen AI accuracy, providing the model with a training data set of specific downstream task examples.
03:12
While fine tuning refines the model's internal knowledge and abilities, grounding augments its knowledge with external, real-time and reliable information.
03:22
Remember the earlier analogy about foundation models versus fine-tuned models?
03:26
If K-12 education represents the foundation model, then fine-tuning is specialized professional training like medical school that embeds domain-specific expertise.
03:37
Grounding, then, is the ongoing practice of checking the latest research, drug treatments, and medical policies to stay current.
03:45
Now let's look at how to tune and customize a Gen AI model with Vertex AI Studio.
03:51
You have different options, ranging from less technical methods like prompt design, which require fewer computational resources, to more technical methods that require more computational resources, like full fine-tuning.
04:04
You are already familiar with prompt design, which lets you tune a generative AI model with examples and instructions in natural language.
04:12
Remember that prompt design does not alter the parameters of the AI model.
04:16
Instead, it improves the model's ability to respond appropriately by guiding it on how to react.
04:23
One benefit of prompt design is that it enables rapid experimentation and customization of generative AI results.
04:29
Another benefit is that it doesn't require specialized machine learning knowledge or coding skills, making it accessible to a wider range of users.
04:38
However, for more complex tasks that require tailored results, consider customizing an AI model with either parameter-efficient tuning or full fine-tuning.
04:47
Parameter-efficient tuning, also called adapter tuning, enables efficient adaptation of large models to your specific task or domain.
04:56
This method also updates a relatively small subset of the model's parameters during the tuning process.
05:02
Full fine-tuning is ideal for highly complex tasks, as it can achieve higher quality results.
05:08
However, this method requires more computational resources for both tuning and serving, as it updates all the model's parameters.
05:17
Given these techniques and even some variations between them, Vertex AI currently supports supervised fine-tuning to customize foundational models.
05:27
Supervised fine-tuning improves model performance by teaching it a new skill.
05:31
It uses data containing hundreds of labeled examples to teach the model to mimic a desired behavior or task.
05:38
Each labeled example demonstrates the desired model output.
05:42
The output of the tuning job is a new model that combines newly learned parameters with the original model.
05:49
Supervised fine-tuning is a good option for well-defined tasks with available labeled data.
05:54
For example, it can improve model performance for classification, summarization, extraction, and chat tasks.
06:01
Supervised fine tuning trains a model with labeled data.
06:05
It can be implemented with different techniques like parameter-efficient tuning or full fine-tuning, depending on task complexity and available computational resources.
06:14
Now let's move to Vertex AI Studio and see how to start a tuning job.
06:18
From the Vertex AI Studio menu, select Tuning, then Create a Tuned Model.
06:24
Specify the model details and the tuning data set.
06:27
Note that the UI may change as the product progresses.
06:31
The tuning data set should be structured as supervised training data in a JSONL file.
06:37
Each record or row contains a pair of text data, the input text, which is the prompt, and the output text, which is the expected response from the model.
06:47
For example, if the prompts are "This commercial building is architecturally interesting and has a great interior layout."
06:53
and "The room was terrible. It needs major rework." the expected sentiment labels would be positive and negative, respectively.
07:01
This structure allows the model to learn and adapt to your desired behavior.
07:05
You can then start the tuning job and monitor the status in the Google Cloud console.
07:11
When the tuning job completes, you'll see the tuned model in the Vertex AI Model registry.
07:15
And you can deploy it to an endpoint for serving or further test it in Vertex AI Studio.
07:21
That was a lot of information.
07:23
Ann and Ian can't wait to explore and start experimenting with Vertex AI Studio themselves.
07:29
It's time for you to have some hands-on practice.
07:32
This lab will give you the opportunity to create an application directly from a prompt, design effective prompts by
07:38
applying best practices, engineer and manage prompts by using features like prompt evaluation, and use multimodal prompts and generate media.
07:49
By the end of the lab, you'll be well equipped to use Gemini Multimodal with Vertex AI Studio.