# LokeshPareek089-langgraph-MAT496
## Module 1
  ### Lesson 1: Simple Graph
  * Summary:
    * I learnt concept of building a simple state graph using LangGraph. It explains how nodes represent states or tasks, and edges define the flow between these nodes, forming a directed graph
      that controls the sequence and conditional branching of agent actions.
  * Source File: https://github.com/langchain-ai/langchain-academy/blob/c71b9b999932dcf5bb70abdbca2e1f9ac6c01da8/module-1/simple-graph.ipynb
  * Changes Made:
    * Cheanged the output messages in each node.
    * Changed decision logic from a 50/50 random split to a 90/10 random split.
    * Changed initial state in graph invocation.
  ### Lesson 2: Chains
  * Summary:
    * I learnt how to use LangGraph to build and manage chains of language model calls. The video demonstrates how to structure a sequence of tasks (or "chain") where each step can process
      messages, call tools, and pass state to the next step 
  * Source File:https://github.com/langchain-ai/langchain-academy/blob/c71b9b999932dcf5bb70abdbca2e1f9ac6c01da8/module-1/chain.ipynb
  * Changes Made:
    * Changed the Messages in the AI and Human interaction.
    * Changed parameters in arithmetic function.
  ### Lesson 3: Router
  * Summary:
    * I learnt how to use a router node in LangGraph to direct different types of user queries to the appropriate processing path. It explains
      how to set up conditional edges and routing logic so
      the graph can intelligently decide, based on the input, whether to call a tool, answer directly, or take another action.
  * Source File:https://github.com/langchain-ai/langchain-academy/blob/c71b9b999932dcf5bb70abdbca2e1f9ac6c01da8/module-1/router.ipynb
  * Changes Made:
    * Defined both multiply and exponent functions as tools in the notebook.
    * Bound both tools to the language model using llm.bind_tools([multiply, exponent]).
    * Updated the graph construction so the ToolNode includes both multiply and exponent tools, not just one.
    * Added another message to invoke exponent function.
  ## Lessom 4: Agent
  * Summary:
    * The lesson teaches how to build an agent in LangGraph by connecting multiple nodes and tools in a workflow. It shows how agents can solve
      more complex, multi-step tasks in an adaptive and extensible way.
  * Source File:https://github.com/langchain-ai/langchain-academy/blob/c71b9b999932dcf5bb70abdbca2e1f9ac6c01da8/module-1/agent.ipynb
  * Changes Made:
    * Added Exponent Function in tools.
    * Modified message to raise output to the power of output so as to call exponent function.
  ### Lesson 5: Agent with Memory
  * Summary:
    * The video explains how to build AI agents that can remember previous interactions using LangGraph's memory features. It demonstrates how to use memory modules (like MemorySaver and
      checkpointers) to persist conversation history and user-specific data, enabling agents to provide context-aware, personalized responses across multiple turns or sessions
  * Source File:https://github.com/langchain-ai/langchain-academy/blob/c71b9b999932dcf5bb70abdbca2e1f9ac6c01da8/module-1/agent-memory.ipynb
  * Changes Made:
    * Added Exponent Function to the tools.
    * Continued thread by further raising the output to the power of itself and then dividing that by 2.
