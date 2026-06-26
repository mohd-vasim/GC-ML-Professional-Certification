SPEAKER: This lesson covers the first half of the prompt-to-production lifecycle, prompt engineering from design to evaluation and refinement.
00:10
A good prompt, as we learned previously, considers both content-- instructions, context, and examples-- and structure-- order, labels, delimiters.
00:21
So how do you engineer a good prompt?
00:24
It begins with prompt design, supported by a rich toolkit provided by Vertex AI Studio.
00:31
This is your primary playground for crafting prompts.
00:34
On the left, specify the context in system instructions, then pose your tasks or questions in the Prompt section.
00:43
Need help?
00:44
Gemini, the built-in AI assistant, can help you create your prompt.
00:49
Powered by multimodal foundation models like Gemini, you can incorporate multimedia data such as documents, images,
00:56
and videos from diverse sources, including Google Cloud Storage, Google Drive, your local computer, or a URL.
01:04
You can even embed YouTube video links into a prompt.
01:08
Guide the AI's output by adding examples using the default input and output features.
01:13
Or customize them to question and answer.
01:17
Enterprise users can also import example files of their company's data.
01:22
Ann is a developer looking for a way to code prompts, perhaps using a function or method with variables to streamline repetitive actions.
01:31
Vertex AI Studio's new prompt template feature is the perfect solution.
01:35
It uses replaceable variables, allowing you to reuse a prompt by simply changing values.
01:41
Imagine a function in coding but using natural language.
01:45
The beauty is, you only need to tell GenAI what to do without worrying about how to do it with specific programming languages.
01:53
Consider this example.
01:55
By clicking Add Variables, you can assign values, just like passing arguments to a function.
02:02
For instance, you could ask AI to research Los Angeles tenant vacancy rate and generate a report on real-estate market analysis.
02:11
You can also instruct AI to add variables to study annual crime rate and conduct an insurance risk assessment by using the same prompt template with different values.
02:22
When your draft is complete, navigate to the right side of the user interface to experiment with various model parameters.
02:29
Begin with model selection.
02:30
Vertex AI Studio offers a wide selection of Google and third-party models, including Anthropic Claude, Meta Llama, and OpenAI GPT.
02:40
A key advantage of Vertex AI Studio, though, is its access to Google's cutting-edge GenAI models, like Gemini.
02:47
Choosing the right Google model depends on your task.
02:50
In the previous lesson, you were introduced to Google's different foundation models.
02:54
To refresh your memory, Gemini family-- example, Gemini Flash and Gemini Pro-- ideal for general purposes and multimodal data use cases, specialty models designed for specific tasks.
03:07
For instance, here are a few options when you are in media studio, where you create multimedia with Vertex AI Studio-- Imagen for
03:14
image creation, Chirp for voice generation, Veo for video processing, Lyria for music composition. After model selection, the next step is parameter specification, like
03:28
temperature, Top P, and Top K. You might find some of these options in the advanced settings. These parameters control the randomness of
03:37
the model's responses by adjusting how output tokens are selected. But how do they actually work? Let's look at an example. The garden was
03:46
full of beautiful dot, dot, dot. When prompted with this incomplete sentence, language models predict the probability of potential words, like flowers, trees,
03:56
herbs, and bugs. The selection strategy impacts the outcome. Always choosing the most probable word can lead to repetitive and potentially biased text, while
04:07
random sampling might yield unlikely responses, such as bugs. Adjusting model parameters to control randomness allows you to balance predictability and variety, finding the
04:18
ideal strategy for a specific task. Let's explore these parameters in depth. First, temperature-- this number controls the degree of randomness in generated output.
04:29
A low temperature setting narrows the range of possible output to high-probability, more typical words.
04:36
This is ideal for tasks like question answering and summarization, where a more typical answer with less variability is expected.
04:44
A high-temperature setting expands the range to include lower-probability, more unusual words, useful for generating creative or unexpected content.
04:54
Another parameter is Top K. Top K allows the model to randomly select a word from the Top K most probable words, where K equals a number.
05:04
For example, top two means the model will randomly select either of the two most probable words, such as flowers or trees.
05:12
This approach gives high-scoring words an equal chance.
05:15
However, if the probability distribution is highly skewed-- example, flowers at 80% and books at 10%-- it can result in strange responses, like the garden was full of beautiful books.
05:29
The challenge of selecting the optimal top K value led to Top P, where P stands for probability.
05:36
Top P allows the model to return a word from the smallest subset with a sum of likelihoods that exceeds or equals P. For example, a P of 75% means
05:46
sampling from a set of words with a cumulative probability greater than 75%-- in this
05:52
case, flowers, trees, and herbs. This dynamically adjusts the size of the word set based on
05:58
the probability distribution of the next word. And that is an overview of the model parameters-- model type, temperature, Top K, and Top P. Note that you are not required
06:10
to adjust them constantly, especially Top K and Top P. After crafting the prompt and
06:15
specifying parameters, how can you ensure you've selected the optimal model and parameters for the task?
06:22
This is where evaluation and refinement come in.
06:25
Vertex AI Studio allows you to compare prompts side by side to see which produces the best results.
06:31
This helps you understand how different prompts, models, and/or parameter settings influence the output.
06:37
You can even generate your own evaluation metrics by adding ground truth from your field knowledge, your preferred answer to the prompt against which all other model responses are evaluated.
06:48
Ready to take your prompt to the next level?
06:50
Optimize it in a Colab Enterprise notebook by adding labeled examples to refine the results.
06:56
You can perform these tasks' comparison, optimization, and evaluation under the Prompt management menu.
07:03
Imagine Prompt management as storage to save and share prompts for future use and collaboration, complete with tools like version control and security.
07:12
Beyond general purpose prompts, you can apply these prompt engineering techniques and tools on Vertex AI Studio
07:18
to specific tasks, such as generating real-time streaming, creating multimedia content, translating content, and converting speech and text.
07:28
Ann has learned so much about what she can do with prompts and is eager
07:32
to leverage these tools to create custom prompts using her own data to solve business problems.
07:38
She's excited to learn how to deploy the prompt to code, which will be revealed in the next lesson.