SPEAKER: Let's proceed to the most recent AI application, AI agents.
00:07
In previous lessons, you learned about foundation models like Gemini and development tools like Vertex AI Studio for building Gen AI applications.
00:18
You might now be wondering how to further leverage these technologies to enable AI to not only chat and research but also take action.
00:29
For instance, can AI be used to automate your workflows and make decisions on your behalf?
00:36
This is where AI agents and Agentic AI takes center stage.
00:42
Join us in this lesson to explore the evolution of Gen AI and then dive into AI agents, discovering how they take action for you.
00:54
Think about the applications you've explored so far.
00:57
Many are conversational in nature.
00:59
You pose a question with a prompt, and the AI delivers an answer.
01:04
Think back to the example with Bea and Ann.
01:07
They asked Vertex AI Studio to generate an insurance analysis report from a set of instructions.
01:14
And voila!
01:15
The AI did a fantastic job in mere seconds, saving Ann tremendous time.
01:21
Naturally, Bea and Ann wished the AI could automate the subsequent steps, like verification, decision-making, and policy structuring.
01:32
However, these tasks require accessing internal documentation and interacting with various existing applications.
01:40
This falls outside the scope of foundation models, which base their knowledge on pre-trained data that's often not field-specific and cannot connect to different applications.
01:54
An AI agent solves this problem and adds real value to foundation models.
02:00
AI agents connect to information and applications outside of foundation models, take action, and observe feedback from the environment to improve over time.
02:12
Bea and Ann are amazed by the potential of AI agents.
02:16
What if they desire a unified agent system that coordinates multiple agents for insurance, underwriting, and claims?
02:25
This is termed agentic AI, which can be imagined as a more autonomous, complex reasoning and
02:31
coordinating system for multi-step tasks involving multiple agents, surpassing the capabilities of a single AI agent.
02:41
Gen AI is embarking on a fascinating journey, evolving from simple chatbots to sophisticated AI agents and, ultimately, to proactive Agentic AI.
02:52
This progression promises to make AI increasingly practical, empowering us to tackle more complex real-world challenges.
03:01
Given the evolution of Gen AI, let's zoom in on an AI agent and discover how it works.
03:07
First and foremost, what exactly is an AI agent?
03:11
In generative AI, an AI agent is an application that combines AI models for reasoning, tools for external interaction, and sophisticated coordination to achieve a desired goal.
03:26
The agent's operation is driven by its logical architecture, which has a few key features.
03:32
It is goal-oriented, uses an AI model as its brain, employs tools for action, and has a potential reasoning and decision-making capability that allows it to operate autonomously.
03:45
To achieve these attributes, an AI agent coordinates three essential components-- model, tools, and orchestration. First, the model-- the brain.
03:56
The model, which can be one or multiple AI foundation models, is the agent's reasoning center.
04:03
Like a brain, it acts as the central decision-maker, thinking, planning, and figuring out the steps needed to achieve a goal.
04:11
Models are typically general purpose, but can be refined with specific examples to showcase capabilities.
04:18
Next the tools-- hands, feet, and senses. Tools are the connectors that allow the agent to
04:25
interact with the outside world, often taking the form of APIs, using comments such as GET, POST,
04:33
PATCH, DELETE. Like hands and feet, they perform actions such as sending an email. Like senses, they
04:41
gather new, external information, such as fetching weather data. And lastly, the orchestration layer-- the nervous system.
04:51
The orchestration layer is the central, cyclical process that governs the agent's operation.
04:57
Like a nervous system, it acts as the communication network.
05:01
It takes the brain's decisions, uses tools to take action, and then carries feedback from that action back to the brain to inform the next step.
05:12
To learn more about AI agents, please refer to Google's whitepaper, Agents, accessible via the QR code on the screen and URL in the reading list.
05:23
Quiz time-- Bea and Ann learned a lot about an AI agent and how it works with three components. They want to design an AI agent to handle insurance
05:33
claims. This agent needs to first access the customer's claim history from an external database. Then the agent needs to validate the claim by checking it against the internal
05:44
policy documentation. And finally, send a confirmation email to the customer. Let's match the components from the following list to the questions. Which AI Agent component is responsible for
05:57
managing the sequence of actions and decisions which connects to internal and external resources and services? And which comprehends communication and logic-- the model, the tools, or the orchestration layer?
06:17
Yes, A, the model, acting as the brain, comprehends communication and logic.
06:23
B, the tools, connect to resources and services.
06:27
While C, the orchestration layer, manages the sequence of actions and decisions.
06:33
Did you get all of them right?
06:35
In summary, AI agents advance the AI function from conversational, chatbots, to actionable.
06:43
But how can you create an AI agent on Google Cloud?
06:46
You'll find out soon.