# agent_harnesses_over_time
A repo to analyze the evolution of agentic harnesses over time

# Introduction
We have seen AI Agents around for the last couple of years mostly; they said 2025 were the year of agents, and even though it felt like it was not going places... at the end of the year, with the release of certain Agent Harnesses (more on this soon) like OpenCode, or the improved Claude Code; it felt like really 2025 was the year of agents after all.

I can confidently say, that after being into the field with a close analysis of what was going on for the last 3 years... I have seen different Agentic Harnesses to be the "goto" method to solve problems that agents needed to solve.

So, what is an Agent Harness after all? Well, you can call them "agents" or "scaffolds" too; but somehow, calling a harness, an "agent"; makes the concept a bit more magical of what it truly is.

My definition for agent would be the combination of:
- Model: which LLM is used; it turns out that certain models are trained with certain tool formats, and others with other tool formats, being the OpenAI format the one becoming de facto. The model is not the only relevant thing, also the quantization used.
- Prompt: which prompt is given to the Model to get responses back.
- Agent Harness: the code that prepares the final prompts for the model, and executes the code of the tools that have been used by the Model.
- Inference engine: it makes a lot of sense to mention the inference engine used, as different engines use different mechanisms to extract the tool calls (llama.cpp is different to ollama and is different to vllm, to name a few).
- Hyperparameters: it is also relevant to remark which hyperparameters are used to run the Agent, as changing the temperature, repetition penalty... will cause different behaviors.
- Tools*: even though I have mentioned that I was not going to put them separate to the Agent Harness, a second read of the written material here, suggests that when you use "general harnesses" like OpenCode or Claude Code, you actually get to choose which tools (as MCP servers) you want to load, thus, they are relevant to be considered separately to the Agent Harness itself.

As you can see, I do not (need to) mention anything related to "Tools" or "Context Engineering"; as they both go inside the Agent Harness. Putting them inside the Agent Harness makes a lot of sense; when you realize that a set of tools in a different script, system prompt and/or code that calls the model; causes different behaviors.

So here we are, we are achieving AGI under our fingertips, by looping LLM calls, and adding guardrails and some tricks on top; to make models work on themselves, on what I like to call: "AFK Coding". We are likely moving away from the vibe coding philosophy in which you get to "Accept" which changes are applied by the model and in which manner, to actually let them make such choices, and let us go AFK (Away from keyboard) for a while. How long that "while" is, depends on how good your agent is; and thus, how good each of the pieces that the agent contains are.

# Evolution
We have been coding agents for a while; and they have gone under different kinds of harnesses, or if you wanna call it this way: different kinds of interfaces that make them behave differently and provide different kinds of user experiences; at each new kind of interface, a believe appeared that "yeah, that's the way we are going to do things in the long term", just to be replaced by a "oh shit, how wrong I was, kind of feeling afterwards".

From the PoV of DaertML, there are archived agents that were build on custom scaffolds and called models as old as Nous Hermes 2 (those days...); the behavior of the agent was sooo tightened that felt like the model needed to be better, so that it could behave more on their own. It felt like we were writing a convoluted and complex version of a data pipeline that could be written without the use of AI at all, and just a bunch of conditionals and loops here and there... the OGs will remember the era of chatbots, that happened way before this AI paradigm, and they were cool on their own and did great things on their own.

Somehow, it was a needed step to bootstrap the amount of intelligence that we have around nowadays. I would like to give some "nostalgic materials", so that, you can see how we got here:
- Langchain: the early days, do you recall? It felt magical to write pipelines, and connect different prompts together... it felt like the bolts to build AGI in our hands.
- CrewAI: the harness starts to be less "DIY" and more: write your prompts, your tools, and how you wanna connect them, and it will do so.
- Flowise: what a second... these things dont work, and we need to come back to DIY... code becomes spaguetti, and we need a better way to see the flow of things and agent communication: here is your web UI to connect things together.
- Cursor: let's build the agents and all your code by just clicking Tab, and letting autonomous agents take control of the IDE.
- Claude Code: here is your better model that you always needed to say goodbye to the tight harnesses, and let the model decide what to do on itself. And, hey! You do not need an IDE or a web UI, or to write python code or to define the prompts in different complex hierarchy filesystems... just skills, plugins, and subagents! Running in your terminal.

I do not know if I am missing something, but I can tell that I have spent a shit ton of time on langchain like systems, crewAI harnesses and the like and Flowise-like platforms; and at each step over the last 3 years, they all felt like the right thing, and at the same time like it was behaving so wrong.

