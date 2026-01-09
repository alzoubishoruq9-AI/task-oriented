# task-oriented
Building a Text Summarizer and Translator with LangChain

Overview

This tutorial demonstrates how to create a language model application that summarizes text and translates the summary to Spanish using LangChain. The application uses a combination of custom functions, structured tools, and an agent to process input text efficiently.

 Motivation:

In today's data-rich world, the ability to quickly summarize information and translate it into different languages is invaluable. This tutorial aims to show how to leverage language models and the LangChain framework to create a tool that can:

1. Summarize lengthy text
2. Translate the summary to Spanish
3. Do both tasks in a single, streamlined process

This type of tool can be useful for various applications, including content curation, multilingual communication, and rapid information processing.

Key Components:

1. Custom Functions: For summarization and translation
2. Structured Tools: Wrappers for the custom functions
3. Prompt Template: Instructions for the agent
4. Agent: Orchestrates the use of tools based on the prompt
5. Agent Executor: Runs the agent with specified parameters

 Method Details:

 1. Custom Functions:

Two main functions are defined:

- A summarization function that takes input text and returns a summary
- A translation function that takes input text and returns its Spanish translation

Both functions use a PromptTemplate and a language model to perform their tasks.

 2. Structured Tools:

The custom functions are wrapped as StructuredTool objects. This allows the agent to use these functions as tools, providing a name, description, and input schema for each.

 3. Prompt Template:

A PromptTemplate is created with detailed instructions for the agent. It outlines the steps the agent should follow:
1. Summarize the input text
2. Translate the summary to Spanish
3. Format the output with both the English summary and Spanish translation

 
 4. Agent and Agent Executor:

An agent is created using the tools and prompt. This agent is then wrapped in an AgentExecutor, which manages the execution of the agent. The executor is configured with parameters such as the maximum number of iterations and the early stopping method.

 5. Running the Agent:

A helper function is created to simplify running the agent. This function takes the agent executor and a query, runs the agent, and returns the output. The tutorial demonstrates this with a sample query about pangrams, showing how the entire pipeline works together to process the input text.

Conclusion:

This project demonstrates how to create a powerful text processing tool using LangChain. By combining custom functions, structured tools, and an agent, we've created an application that can summarize text and translate the summary to Spanish in one seamless operation. 
