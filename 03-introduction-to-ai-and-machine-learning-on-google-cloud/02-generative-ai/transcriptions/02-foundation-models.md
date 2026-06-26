SPEAKER: Previously, you explored the fascinating world of Gen AI architecture on Google Cloud.
00:05
Now let's dive into the foundational layer, foundation models, the true backbone of all Gen AI applications.
00:14
Interested in how AI creates content?
00:17
Want to learn about Google's foundation models, their differences, the significance of multimodal AI, and how to customize these models for your specific needs?
00:26
Let's explore these topics in this lesson.
00:30
How does AI generate new content?
00:33
It learns from a massive amount of existing content such as text, image, and video.
00:39
The process of learning from existing content is called training, which results in the creation of a foundation model.
00:46
A foundation model is usually a large model in the sense of a significant number of parameters, vast training data, and high computational power requirements.
00:56
The number of parameters generally indicates a model's capacity to learn complex patterns and store information.
01:02
To give you a perspective, the number of parameters has dramatically increased from millions to trillions in recent years.
01:10
This substantial increase signifies that foundation models are becoming progressively more capable and smarter.
01:18
As a pioneering AI company, Google trains foundation models for both general purposes, such as Gemini, and specialized tasks, such as Imagen.
01:27
These models empower Google's own products like Google Search and Workspace and provide services for external users.
01:35
Gemini family, ideal for general purposes and multi-modal data use cases-- popular options include Gemini Pro, the most capable model ideal for
01:45
complex tasks requiring advanced reasoning; Gemini Flash, optimized for high speed and low latency-- perfect for high volume, real-time applications like chatbots; Gemini
01:56
Flash-Lite, the most cost-effective model suited for high volume tasks where time isn't critical, such as batch translation and content summarization; specialty
02:04
models designed for specific tasks, for instance Imagen for image generation, Veo for video processing, embeddings models for semantic search, and data representation.
02:17
This list is subject to change due to the rapid evolution of foundation models.
02:22
Always refer to Google documentation for the latest updates.
02:25
You can find this via the QR code or reading list.
02:29
Powered by the foundation models, Gen AI is driving new opportunities to enhance productivity, save operational costs, and create new value.
02:39
You might have seen these opportunities from the use case about Coffee on Wheels in the previous module
02:43
where you used Gen AI capabilities to automate the marketing campaign, generate customer feedback, and optimize truck routes.
02:52
Take a moment to pause and reflect.
02:54
What could be the use cases for using AI to solve your business problems?
03:03
Each model is fine-tuned for optimal performance within its specific domain.
03:07
However, Gemini has the potential to replace some of these models due to its general purpose and the ability to process data across multiple modalities, a feature known as multimodal.
03:18
A multimodal model, such as Gemini, can process information from various sources, including text, images, and video.
03:26
It can also generate content in multiple modalities.
03:30
For example, you can prompt Gemini to generate a video walkthrough of a recipe based on a cookie photo.
03:38
Multimodal capability marks a significant leap in generative AI's evolution, fundamentally changing how AI perceives and engages with its environment.
03:48
Unlike earlier models limited to a singular modality, multimodal AI now processes an array of senses, enabling it to understand and interact using modalities like text, images, audio, and video.
04:00
These models seamlessly process and synthesize information from multiple sources simultaneously.
04:08
This holistic comprehension enables generative AI to grasp complex contexts, leading to more human-like reasoning and the ability to drive sophisticated, real-world actions.
04:21
How can Gemini enhance your business operations?
04:24
Here are some notable examples.
04:27
Information extraction-- Gemini can read text from images and videos, extracting crucial information for further
04:33
processing. Information analysis-- it can analyze information extracted from images and videos based on specific prompts.
04:42
For instance, it can categorize expenses from a receipt.
04:45
Information seeking-- Gemini can answer questions or generate Q&A based on information extracted from text, images,
04:53
and videos. Content creation-- it can create stories or advertisements drawing inspiration from images and videos.
05:01
The possibilities are extensive, limited only by your imagination regarding how Gen AI can address your business challenges.
05:10
Let's apply this to a challenge.
05:13
Assume you need AI to assess home insurance risk effectively by using real estate images, weather histories, property inspection reports and disaster videos.
05:23
Which Google AI model is best to process these multimodal data?
05:27
A, Veo.
05:29
B, Embeddings.
05:31
C, Imagen.
05:31
D, Gemini.
05:37
Yes, Gemini is the winner due to its powerful multimodal capabilities.
05:43
Let's now consider some practical challenges.
05:45
While foundation models generally possess broad capabilities, they often lack sufficient training data when confronting problems in specialized fields like health care or finance.
05:57
To address specific challenges, such as generating financial models or providing healthcare consulting, a foundation model can be further trained with new field-specific data sets.
06:10
This process yields a new model precisely tailored to your requirements.
06:14
This leads to the concept of pre-trained and fine-tuned models.
06:18
A foundation model is pre-trained for general purposes using a large data set and then fine-tuned for specific objectives with a much smaller data set.
06:28
Consider K-12 education.
06:30
After 12 years of foundational learning in reading, writing, and arithmetic, individuals become literate and can solve basic problems.
06:38
However, to become a professional such as a medical doctor, automotive engineer, or financial advisor, additional specialized training and education are necessary.
06:48
A similar idea applies to pre-trained versus fine-tuned models.
06:53
Foundation models like Large Language Models, LLM, fall under the category of horizontal AI, given their broad capabilities.
07:01
They address common challenges across industries including content creation-- text, image, audio, video, and code; information synthesis; document abstraction and summarization; and conversation generation, questions and answers.
07:19
Conversely, models fine-tuned for specific industries, like retail, finance, and health care are considered vertical AI solutions.
07:26
These often target industry niches and solve specialized problems such as disease diagnosis.
07:34
In light of these advancements of foundation models like Gemini, how can developers engage with them on Google Cloud and create applications that leverage multimodal capabilities?
07:44
There are three main approaches, each accomplishing the same goal with varying degrees of flexibility.
07:50
Google Cloud Console UI, or User Interface, a no-code solution perfect for exploring and testing prompts;
07:56
Gen AI model Application Programming Interfaces, or APIs, a low-code solution like Gemini APIs, used in conjunction
08:05
with command line tools cURL; predefined Software Development Kits or SDKs, a code-based solution available in languages
08:14
like Python and Java, used with notebooks like Colab and Workbench, and seamlessly integrated into Vertex AI.
08:21
Let's explore how to use AI models with Google in the next few lessons.