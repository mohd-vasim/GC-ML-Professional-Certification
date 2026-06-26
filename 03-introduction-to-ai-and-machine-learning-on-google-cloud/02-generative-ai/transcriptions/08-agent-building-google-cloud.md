SPEAKER: Earlier, you learned about the evolution of GenAI applications, from chatbots to AI agents, and then to agentic AI.
00:09
You also delved into an AI agent, how it works, with three components-- model, tools, and orchestration
00:14
layer. Now it's time for a practical guide-- how to create an AI agent on Google Cloud.
00:22
Google's GenAI architecture, as discussed at the beginning of this module, provides a comprehensive suite of AI agent tools and products.
00:31
These offerings span foundation models, development tools, and application products.
00:36
From the bottom up, Vertex AI Model Garden provides access to a wide range of Google's foundation models and third-party generative AI models, serving as the brain for your agent.
00:47
Moving up to the development layer, a developer can build an AI agent using Vertex AI Agent Builder with either low-code or pro-code options.
00:57
This platform offers tools such as Agent Development Kit, or ADK, Agent Engine, and Agent Garden, along with a managed environment to simplify agent development.
01:08
It empowers developers, including software and ML engineers, to build AI agents end-to-end, from design to deployment.
01:17
The top layer is the application or solution layer, designed for business users or analysts who want to build an AI agent with no code or minimum code.
01:28
Gemini Enterprise is the hub for hosting and building AI agents to solve customized business problems.
01:36
You can also rely on the Customer Engagement Suite to build conversational agents like customer service chatbots.
01:42
How exciting.
01:43
You're probably thrilled by the capabilities of AI agents, yet perhaps a bit overwhelmed by the sheer number of tools available.
01:50
The big question is, how do you use them efficiently to build an AI agent?
01:56
This is the exact challenge Bea, Ann, and Ian faced when they set out to build an AI agent to automate insurance quotes for their customers.
02:04
Where to start?
02:06
Let's dive deeper into how to use these different tools from an AI agent builder's perspective.
02:11
Product choices and development journeys are influenced by two key factors, ease of use and flexibility.
02:18
Ease of use ranges from no-code, ready-to-go solutions like Gemini Enterprise, progressing to more comprehensive code-based solutions for building your own.
02:30
Flexibility varies from minimal configuration, like Gemini Enterprise, to full customization and high flexibility, like build your own.
02:40
Let's focus on Gemini Enterprise and Vertex AI Agent Builder, as these are the tools most people interact with.
02:48
Bea, Ann, and Ian want to prototype their ideas using an AI agent to automate insurance quotes.
02:56
They turn to Gemini Enterprise, a user-friendly, no-code application designed for business users and analysts.
03:05
Imagine a team of expert AI agents, each ready to tackle a specific business challenge, just like hiring a travel agent or general contractor.
03:14
That's Gemini Enterprise.
03:16
This powerful enterprise platform unites AI, Google-quality search, and your company's proprietary data in one secure space.
03:26
Breaking down data silos, Gemini Enterprise makes your enterprise knowledge readily accessible and actionable in a secure manner.
03:36
A core capability of Gemini Enterprise is its intelligent, multimodal search.
03:42
It allows employees to quickly find contextual, cited answers from all organizational data formats-- documents, images, videos-- within a single interface, streamlining research and boosting productivity.
03:55
Beyond search, Agentspace also provides a hub for AI agents that can automate workflows and complete tasks on behalf of users.
04:03
It offers pre-built Google agents and a no-code agent designer for creating custom agents tailored to specific business needs.
04:11
These agents can perform actions like updating project tickets, sending emails, or analyzing reports, reducing manual overhead and freeing up time for more strategic work.
04:24
Among the powerful AI agents in Google Agentspace, NotebookLM stands out.
04:29
It's your personal AI research assistant, a learning companion and study tutor designed to quickly help you understand and gain insights from vast amounts of information.
04:39
Let's look at a demo on how to get started with NotebookLM, use it as your personal research assistant, and leverage it to discover insights and generate content.
04:52
Welcome to NotebookLM, where you can tap into the power of generative AI.
04:57
To begin, simply select the Create button to start a new notebook.
05:01
The first step is to add your source documents.
05:03
NotebookLM is flexible and supports a wide range of formats, including PDFs, text, markdown, and audio files.
05:11
You can also pull documents directly from Google Drive, add links from websites or YouTube, or paste in text.
05:18
For example, you could upload a report from McKinsey and a white paper from Google Cloud to create a new intelligent workspace.
05:25
Once your documents are uploaded, you can start a conversation in the text box at the bottom.
05:30
Think of it like talking to a super smart research assistant that uses only the documents you've provided for context.
05:37
You can ask NotebookLM to perform a variety of tasks, such as creating a concise summary of your source materials with easy-to-reference citations.
05:45
You can also ask specific questions, give it creative assignments, or have it summarize highly complex information.
05:52
The right-hand Studio panel offers even more ways to work with your documents.
05:57
In the Audio Overview section, NotebookLM can generate a podcast from two hosts based on your source documentation.
06:05
In the Notes section, it can automatically create a study guide, a briefing document, an FAQ, or even a timeline.
06:14
With these powerful features, it's your turn to explore and unlock the potential of your own data with NotebookLM.
06:22
While Gemini Enterprise and NotebookLM are impressive for building AI agents, they fall short when it comes to tailoring agents for unique business needs.
06:33
Bea, Ann, and Ian require an agent that can seamlessly integrate with their company's legacy applications and internal databases.
06:40
They also need specific response behaviors, such as adhering to industry policies for claim reports while maintaining a warm and empathetic tone for customer communications.
06:50
Gemini Enterprise couldn't accommodate these custom requirements, highlighting the need for tools like Vertex AI Agent Builder.
06:59
Let's explore the Vertex AI components that facilitate end-to-end AI agent development from design to deployment.
07:07
Vertex AI Agent Garden, a resource offering agent samples, customizable blueprints, and source code for various use
07:13
cases, like data analysis and customer service, accelerating agent development so you don't have to start from scratch.
07:20
Vertex AI Agent Development Kit, or ADK, an open source framework for developers seeking more control over
07:26
agent logic, enabling the creation of production-ready agents using Python and seamless integration with Google Cloud Services.
07:35
It's the agent version of an SDK, Software Development Kit.
07:39
Feel free to check out ADK Quickstart in the Reading List.
07:42
Vertex AI Agent Engine, a fully managed runtime for simplified deployment, scaling, and monitoring of agents in production, handling infrastructure so you can focus on capabilities.
07:54
To summarize, a simplified decision tree can help navigate Google's AI agent ecosystem, including tools and products.
08:01
Please note this is only a brief guide and may change as products evolve.
08:06
Out-of-the-box solutions-- Gemini Enterprise and conversational agents are ideal for no-code deployment.
08:13
This path is best for business users who need ready-to-use solutions with minimal setup.
08:18
Customizable templates-- Agent Garden with Agent Builder offers pre-built sample agents that can be modified.
08:25
This low-code approach is best for data scientists and analysts who need a starting point for creating more tailored solutions.
08:32
Custom development-- the ADK or building your own solution from scratch is the pro-code path.
08:38
This approach offers maximum flexibility and is best for developers like software and ML engineers who need to build highly tailored agents with complex logic and deep integrations.
08:49
Armed with these amazing tools, you can now create your very own AI agent.
08:54
Explore NotebookLM-- notebookLM.google.com.
08:58
Now completely free for the general public, and find your AI research assistant, learning companion, or even tutor.
09:06
Have fun.