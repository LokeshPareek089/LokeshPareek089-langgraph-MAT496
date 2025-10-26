# LokeshPareek089-langgraph-MAT496
## Module 1
  ### Lesson 1: Simple Graph
  * Summary:
    * I learnt concept of building a simple state graph using LangGraph. It explains how nodes represent states or tasks, and edges define the
      flow between these nodes, forming a directed graph
      that controls the sequence and conditional branching of agent actions.
  * Source File: https://github.com/langchain-ai/langchain-academy/blob/c71b9b999932dcf5bb70abdbca2e1f9ac6c01da8/module-1/simple-graph.ipynb
  * Changes Made:
    * Cheanged the output messages in each node.
    * Changed decision logic from a 50/50 random split to a 90/10 random split.
    * Changed initial state in graph invocation.
  ### Lesson 2: Chains
  * Summary:
    * I learnt how to use LangGraph to build and manage chains of language model calls. The video demonstrates how to structure a sequence of
      tasks (or "chain") where each step can process
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
  ### Lessom 4: Agent
  * Summary:
    * The lesson teaches how to build an agent in LangGraph by connecting multiple nodes and tools in a workflow. It shows how agents can solve
      more complex, multi-step tasks in an adaptive and extensible way.
  * Source File:https://github.com/langchain-ai/langchain-academy/blob/c71b9b999932dcf5bb70abdbca2e1f9ac6c01da8/module-1/agent.ipynb
  * Changes Made:
    * Added Exponent Function in tools.
    * Modified message to raise output to the power of output so as to call exponent function.
  ### Lesson 5: Agent with Memory
  * Summary:
    * The video explains how to build AI agents that can remember previous interactions using LangGraph's memory features. It demonstrates how to
      use memory modules (like MemorySaver and
      checkpointers) to persist conversation history and user-specific data, enabling agents to provide context-aware, personalized responses
      across multiple turns or sessions
  * Source File:https://github.com/langchain-ai/langchain-academy/blob/c71b9b999932dcf5bb70abdbca2e1f9ac6c01da8/module-1/agent-memory.ipynb
  * Changes Made:

## Module 2
  ### Lesson 1: State Schema
  * Summary:
    * I learnt ow to define a structured state schema in LangGraph using Python's TypedDict, which serves as the central data that
      flows through nodes in a graph workflow. It shows how nodes update and use this state, demonstrating the importance of a clear state
      structure for better code clarity and type safety.
  * Source File: https://github.com/langchain-ai/langchain-academy/blob/c71b9b999932dcf5bb70abdbca2e1f9ac6c01da8/module-2/state-schema.ipynb
  * Changes Made:
    * The field name was changed from mood with values "happy" and "sad" to job_role with values "cowboy," "merchant," and "soldier."
    * The number of conditional paths expanded from two options to three options, requiring an additional node (node_4) to handle the third path.
    * The decision function logic was modified from a simple 50/50 split between two options to a more complex 40/40/20 split distributing
      probability across three options.
    * The validator implementation was updated to check the job_role field instead of the mood field, with the validator method renamed from
      validate_mood to validate_job_role.
  ### Lesson 2: State Reducers
  * Summary:
    * The video explains that state reducers in LangGraph control how node outputs update the shared state, allowing customization of whether new values overwrite or combine with existing
      ones. This enables flexible and robust state handling, especially in parallel or aggregated workflows.
  * Source File:https://github.com/langchain-ai/langchain-academy/blob/c71b9b999932dcf5bb70abdbca2e1f9ac6c01da8/module-2/state-reducers.ipynb
  * Changes Made:
    * Message content updated - Marine biology examples replaced with Machine Learning and LangGraph topics.
    * Conversation context modified - Ocean mammals discussion changed to Machine Learning and LangChain learning topics.
    * User name changed - "Lance" updated to "Brijesh" in message examples.
  ### Lesson 3: Multiple Schemas
  * Summary:
    * I Learnt how to use multiple state schemas within a single graph. It covers defining separate input, output, and internal state schemas to control what data is visible or private at
      different stages.
  * Source File:https://github.com/langchain-ai/langchain-academy/blob/c71b9b999932dcf5bb70abdbca2e1f9ac6c01da8/module-2/multiple-schemas.ipynb
  * Changes Made:
    * node_1 changed from +2 to +1, and node_2 from +3 to +1, resulting in output of 3 instead of 5.
    * Person's name changed from "Nagesh" to "Lance" throughout the greeting logic.
  ### Lesson 4: Trim-Filter-Messages
  * Summary:
    * The video covers how to manage message histories efficiently using trim_messages and filter_messages. Trimming shortens message content to stay within token or message limits, while
      filtering removes irrelevant messages (like system or tool outputs) before sending data to the model. Together, they keep conversations concise, relevant, and optimized for performance.
  * Source File:https://github.com/langchain-ai/langchain-academy/blob/9dc3654883260f1fa217accbfc0a891c9e42e6c3/module-2/trim-filter-messages.ipynb
  * Changes Made:
    * Message content updated - Marine biology examples replaced with Machine Learning and LangGraph topics.
    * Conversation context modified - Ocean mammals discussion changed to Machine Learning and LangChain learning topics.
    * User name changed - "Lance" updated to "Nagesh" in message examples.
  ### Lesson 5: Chatbot with Summarizing Messages and Memory
  * Summary:
    * The video eplains how to make chatbots smarter and more memory-efficient by summarizing past conversations instead of keeping full histories. It introduces a summarization node that
      condenses older messages into a brief summary, preserving context while optimizing memory with tools like MemorySaver and conditional graph edges.
  * Source File:https://github.com/langchain-ai/langchain-academy/blob/9dc3654883260f1fa217accbfc0a891c9e42e6c3/module-2/trim-filter-messages.ipynb
  * Changes Made:
    * Message content updated - Introductory messages replaced weather related messages.
  ### Lesson 6: Chatbot with Summarizing Messages and External Memory
  * Summary:
    * I learnt how to enhance chatbot memory by summarizing past messages and saving these summaries to external memory stores. This approach enables efficient long-term context retention
      across sessions without overloading the model with full chat histories
  * Source File:https://github.com/langchain-ai/langchain-academy/blob/9dc3654883260f1fa217accbfc0a891c9e42e6c3/module-2/chatbot-external-memory.ipynb
  * Changes Made:
    * Message content updated - Introductory messages replaced weather related messages.
    * Conversation context modified.

## Module 3
  ### Lesson 1: Streaming-Interruption
  * Summary:
    * The video explains how to enable real-time streaming of outputs within LangGraph workflows, allowing developers to observe model responses as they are generated rather than after full
      completion. Streaming enhances user experience by providing incremental updates from LLMs, improving responsiveness and interactivity in AI agents.
  * Source File:https://github.com/langchain-ai/langchain-academy/blob/26377bf69b01132c91617878afb51d3eb340f3e1/module-3/streaming-interruption.ipynb
  * Changes Made:
    * Conversational Content changed.
    * Message content changed from command to a question on Vatican City.
  * <img width="3197" height="1810" alt="image" src="https://github.com/user-attachments/assets/52c59ed4-ea91-4eb0-abdb-3ad5f032c410" />
  ### Lesson 2: Breakpoints
  * Summary:
    Breakpoints in LangGraph allow pausing AI agent workflows for human review and approval before continuing, enabling controlled and safe human-in-the-loop interactions. They help ensure
    oversight on sensitive steps like tool calls or data writes.
  * Source File:https://github.com/langchain-ai/langchain-academy/blob/f3c8894426b9687de78dc8b2c91885515d171223/module-3/breakpoints.ipynb
  * Changes Made:
    * Added Exponent Method in Tools.
    * Changes Input message from a Multiplication to Exponentation.
