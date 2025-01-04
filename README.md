# exploring-langGraph - 

### What is LangGraph?
[Langgraph](https://langchain-ai.github.io/langgraph/) is a library on top of [langchain](https://www.langchain.com/langchain) for building agents & agent runtime.
What is an Agent?
	A system powered by LM that decides what action to take.

### What is an Agent runtime?
This runtime runs agent in a loop, calls the agent, decides the action to take, takes the action & records the observation & passes it back & starts to loop all over again & continues going through that loop until it decides that its finished.
With Langchain, it is now easier to customize agents with Langchain expression language.

LangGraph is another way to create this runtime.
With LangGraph, goal is to now also easily customize the agent runtime. Earlier, the runtime was agent executor class, which was basically something that run in loop, called tools in specific way, handled errors.

LangGraph is another way to create this runtime to provide more flexibility & dynamically & we can add cycles here to be able to run steps with agent in a loop.
It’s added 2 agent runtimes in LangGraph –
1.	Agent executor – Recreated agent executor like in Langchain. Very similar to it.
2.	Chat agent executor


#### Graph state – 
This state is tracked throughout the graph over time. Once established during initialization step, each node can push updates to that state. So, this doesn’t require the state to be passed around from node to node & instead the updates are passed to that state by nodes.
During updating, we need to specify the type of update that will be pushed in that state. By default, the updates will basically override the existing attribute for that state & in other cases, can add to existing state.

#### Nodes –
-	These are typically python functions, 1st positional argument
-	BTS, functions are converted to Runnable Lambdas which add batch & sync support to your function with native tracing & debugging.

#### Edges –
Define how logic is routed & graphs decide to stop.

Types of edges –
1.	Normal
2.	Conditional – A function decides whether the edge will exist & the associated node will be visited / processed / executed.
3.	Entry point
4.	Conditional entry point

### References -
* Video tutorial – Agent executor - https://www.youtube.com/watch?v=9dXp5q3OFdQ&t=256s
* Chat Agent executor - https://www.youtube.com/watch?v=Un-88uJKdiU&t=316s
* Notebook – How to build basic agent executor from scratch – Plan and execute - https://github.com/langchain-ai/langgraph/blob/main/docs/docs/tutorials/plan-and-execute/plan-and-execute.ipynb
* Notebook - Multi-agent supervisor - https://github.com/langchain-ai/langgraph/blob/main/docs/docs/tutorials/multi_agent/agent_supervisor.ipynb
* LangGraph concept glossary - https://langchain-ai.github.io/langgraph/concepts/low_level/
* LangGraph conceptual guide - https://langchain-ai.github.io/langgraph/concepts/#conceptual-guide
* Tutorials by Langchain academy -
  - Introduction to LangGraph - https://youtu.be/29XE10U6ooc?si=dOPeMg37jgn8YW2V
  - LangGraph Introduction - https://www.youtube.com/watch?v=5h-JBkySK34&t=103s
  - LangGraph tutorial playlist - https://www.youtube.com/watch?v=5h-JBkySK34&list=PLfaIDFEXuae16n2TWUkKq5PgJ0w6Pkwtg

