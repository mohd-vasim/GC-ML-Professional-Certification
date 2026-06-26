SPEAKER: Given that foundation models are the backbone of generative AI development and applications, you may wonder how to interact with them and bring your ideas to applications.
00:10
Are there tools available to assist with this process?
00:14
Let's look at a use case that may resonate with your real-world problems.
00:18
Bea, Ann, and Ian, all work for Cymbal Insurance, a national insurance company with a strong presence in the Western states.
00:27
They are looking for Gen AI tools to help them in their everyday work, including conducting research and automating their workflow.
00:35
Bea, business analyst-- seeks to quickly prototype a Gen AI app idea that automates risk analysis and report generation, despite lacking
00:44
a technical background. Ann, AI developer-- needs a user-friendly development platform for prompt engineering, including drafting, evaluating, refining, and managing prompts.
00:58
Ian, ML engineer-- requires a robust, secure, and scalable tool to build pipelines for deploying prompts to production and fine-tuning Gen AI models.
01:10
Powered by advanced foundation models like Gemini and an enterprise-ready AI infrastructure, Google offers a variety
01:16
of products and services that can help Bea, Ann, and Ian accomplish their Gen AI use cases.
01:23
For example, Vertex AI Studio-- easily build, deploy, and scale generative AI applications. Agent Builder and Gemini Enterprise-- design, deploy, and manage AI agents.
01:38
NotebookLM-- an AI-powered research and note-taking tool for document interaction and insights.
01:46
Let's check out Vertex AI Studio first and then move to AI Agents and NotebookLM later in this course.
01:52
What is Vertex AI Studio?
01:55
Simply put, Vertex AI Studio is your gateway to generative AI.
02:00
Vertex AI Studio provides an intuitive interface between developers and the foundation models.
02:06
It enables you to build Gen AI applications in a low-code, or even no-code environment where you can rapidly test and prototype applications,
02:14
tune and customize models using your own data, augment them with real-world, up-to-date information, and deploy models efficiently in production environments with auto-generated code.
02:26
Envision Vertex AI Studio as a cutting-edge workshop where Gen AI models are your raw materials.
02:33
You are the craftsperson, and the Vertex AI Studio toolkit is your arsenal for shaping and refining these models into powerful AI solutions.
02:42
Intrigued?
02:44
Join Bea, Ann, and Ian to learn how to use this magical tool from prompt to production.
02:50
They all understand that the prompt-to-production may involve a comprehensive lifecycle.
02:55
Designing, evaluating, and refining prompts, building and testing applications, and monitoring and optimizing generative AI models.
03:04
However, Bea, with no technical background, wonders if there's a quicker way to directly turn idea to app.
03:11
The journey begins with a prompt, a natural language request to an AI model.
03:16
This can be a question, task, or instruction leading the AI to generate text, code, images, videos, music, or more.
03:25
The process of creating prompts to get the desired response is called prompt design.
03:29
The iterative process of designing, refining, and optimizing prompts to effectively guide an AI model in generating desired and high quality outputs is called prompt engineering.
03:41
Think of a prompt as the way to communicate with Gen AI models.
03:45
Just as human communication requires clarity, so does prompting AI.
03:49
You need to be good at asking questions to get the results you want.
03:53
So what makes a good prompt?
03:56
Let's begin by examining the anatomy of a prompt.
03:59
Generally, a prompt includes one or more of the following key components-- task, context, examples.
04:07
Task is required.
04:09
This is the core instruction for the model.
04:11
For example, "Conduct a risk analysis for an insurance company."
04:15
Simple tasks may only require zero-shot prompting, which means providing only the task without any examples.
04:23
Context is optional.
04:24
This is the background information or system instructions that sets the stage for the AI, such as, "You are a business analyst overseeing risk assessment for an insurance company."
04:35
Examples are optional.
04:37
These are demonstrations of desired responses, step-by-step instructions or output formats that are useful for complex tasks, such as guiding the AI with a report template.
04:47
This is also known as few-shot prompting.
04:51
When crafting effective prompts, focus on two key aspects, content and structure.
04:57
For content, ensure your prompt includes all relevant information for the task, such as clear instructions, context, and examples.
05:06
For structure, organize the information in a way that the model can understand.
05:10
Consider the order, labels, and delimiters.
05:14
Here's an example of a well-structured prompt.
05:17
You first describe the context.
05:19
"You are an IT help desk technician at a university. Your daily job is to help faculty and students solve their technology issues."
05:27
You then specify the task by providing a step-by-step instruction, such as, "To complete the task, you will need to follow these steps."
05:35
Additionally, you also provide some common Q&A examples.
05:39
Tips for effective prompts-- now that you understand the ingredients of a good prompt, here are some tips for crafting effective ones.
05:47
Be direct and specific.
05:48
State requests clearly, and use keywords.
05:52
Use structure.
05:53
Break down complex tasks into smaller steps, and use delimiters to organize sections.
05:59
Iterate and refine.
06:01
Start simple, and improve based on AI output.
06:05
Explore advanced techniques.
06:07
Consider few-shot prompting, chain-of-thought prompting, or Retrieval Augmented Generation, or RAG, for more complex scenarios.
06:16
Some of these advanced techniques will be discussed later in this course.
06:20
And remember basics-- avoid jargon, set clear goals, create scenarios, and encourage analysis. As Bea and Ann reflect on their
06:29
discovery journey with Vertex AI Studio, they want to create a prompt that utilizes key components and best practices. Which of
06:37
the following prompts is the best option? A, provide a risk assessment report. B, conduct a market risk analysis for
06:46
a health insurance company in the United States. C, you are an analyst at a regional health insurance provider in the
06:53
southeastern United States. Your task is to generate a market risk analysis by following the steps A, B, and C.
07:00
Please find the report template that includes 1, 2, and 3. Yes, C is the correct answer. Take a moment to
07:09
think about why. What makes C an effective prompt? Compared to A and B, C clearly outlines all three components-- task,
07:18
generate a market risk analysis; context, you are an analyst at an insurance company; and examples, such as steps and template.
07:27
This detailed instruction will effectively guide the AI.
07:32
Excited, Bea and Ann then used Vertex AI Studio to prototype a web-based application.
07:39
Bea is a little anxious about her first prompt.
07:41
But Vertex AI studios Help me write feature provides AI-assisted prompting, clarifying content, formatting responses, and breaking down complex tasks.
07:51
The platform's prompt gallery also offers numerous examples, filtered by modality such as audio, doc, text, image, and video, tasks, such as answer questions, classify, and code, and features.
08:05
Ann is particularly impressed by Vertex AI studio's support for multimodal prompts and outputs, allowing embedding
08:12
documents, PDFs, images, videos, and YouTube content in prompts and generating responses in similar multimodal formats.
08:22
With the AI assistant and prompt gallery's help, Bea drafted her first confident prompt.
08:27
"Conduct a risk assessment on housing in southern Los Angeles. You are a business analyst for
08:32
Cymbal Insurance. Analyze the articles from the internet, and extract the following information. Risk assessment-- identify potential
08:39
risks and rate severity 1 to 5, low to high. Categorization-- classify risks by geography, type, and
08:47
sentiment. Impact analysis-- evaluate potential consequences of each risk. And additional insights. Provide relevant observations and recommendations."
08:58
Take a moment to reflect on Bea's prompt. Are you able to identify the major components that make up an effective prompt-- task, context and examples?
09:07
Do you have any suggestions to improve it?
09:11
With a few rounds of experimenting with prompts, Bea and Ann are ready to see their first prototype.
09:16
They click on the Build with Code button and Deploy as App.
09:20
And voila!
09:21
Vertex AI Studio automatically generates a web-based application.
09:25
Bea and Ann are amazed at how quickly they were able to prototype an idea and discover the capabilities of Gen AI.
09:32
They can't wait to see more options provided by Vertex AI Studio and dive deeper to design, evaluate, and refine prompts.
09:39
You'll learn more about this soon.