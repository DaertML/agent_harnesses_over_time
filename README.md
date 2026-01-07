# agent_harnesses_over_time
A repo to analyze the evolution of agentic harnesses over time

# History
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

So here we are, 
