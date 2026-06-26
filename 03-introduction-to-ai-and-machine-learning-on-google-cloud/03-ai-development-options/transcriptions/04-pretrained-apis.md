'SPEAKER: In the previous lesson, you learned about no to low-code solution of AutoML.
00:06
Let's proceed to a low-code solution by using pre-trained APIs.
00:11
Good machine learning models require lots of high-quality training data.
00:16
You should aim for hundreds of thousands of records to train a custom model.
00:20
But what if you don't have that kind of data?
00:22
How can you use AI to serve your purposes?
00:25
Pre-trained APIs are a great place to start.
00:29
API stands for Application Programming Interface.
00:33
APIs define how software components communicate with each other.
00:38
Imagine APIs as electrical outlets.
00:41
Different regions have different standards.
00:43
For example, the US uses type A and B, whereas Europe uses type F. As a traveler, you only need
00:49
to know which adapter to use without worrying about what's behind the wall or how the electrical network is built.
00:57
The same principle applies to APIs.
00:59
As a user, you only need to know which API to use and what parameters to pass and in what
01:04
format without worrying about the implementation, specifically the intricacies of model training and deployment, much like calling a predefined function.
01:15
Look at a simple example.
01:16
The code uses the Google AI for Python SDK, or Software Development Kit, to communicate with the Gemini API following these steps.
01:27
Authenticate your session by passing the unique API key as a parameter to the genai.configure function, granting you permission to use the API using the statement genai.configure(api key="YOUR API KEY").
01:45
2, specify the Gemini models you want to process your request, like Gemini 2.5 Flash, using the statement model is equal to genai.
01:59
GenerativeModel of Gemini 2.5.
02:03
Flash.
02:03
3, make an API call to Google's servers sending the prompt data.
02:08
This string of text passed to the model.generate_content function serves as the main input, the question or instruction that you want the AI to respond to.
02:17
Follow the statement response = model.generate content("What are the three largest countries by area?") 4, receive the model's generated text back as a response by using the statement print(response.text).
02:34
It's remarkable, isn't it?
02:36
You don't need to train your own large language models.
02:38
Instead, you can access and utilize the pre-trained AI models directly through API calls in the same way as a function call.
02:47
So what are the API services provided by Google Cloud?
02:50
Let's explore a short list.
02:52
Generative AI APIs include foundation model APIs, such as the multimodal Gemini APIs, which can be leveraged to directly create content.
03:02
Additionally, Vertex AI Agent Builder provides a comprehensive suite of features for discovering, building, and deploying AI agents.
03:10
Machine learning APIs, like the Vertex AI API, can be used to train, monitor, and tune an ML model with minimal ML expertise and effort.
03:21
Other APIs include speech, image, document, and conversation APIs.
03:25
This list is constantly evolving with technological advancements.
03:29
Many of these can be replaced by the Gemini APIs, which are considered multi-task and multimodal.
03:36
Ever wondered what magic lies behind understanding human language?
03:39
Discover the Natural Language API, a powerful tool that allows you to analyze text directly in your browser.
03:46
Uncover hidden insights by identifying entities, sentiment, syntax, and categories, transforming raw text into meaningful data.