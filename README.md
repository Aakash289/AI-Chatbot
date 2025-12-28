# AI Chatbot 
## Overview

This project is a terminal-based AI chatbot built using LangChain and LangGraph that can understand natural language, respond intelligently, and dynamically invoke Python tools when required.  
The chatbot behaves like an AI agent, meaning it can decide whether to answer a question directly using knowledge or take action by calling a predefined function.

The application runs entirely in the command line and streams responses in real time, creating an interactive ChatGPT-like experience.

---

## What This Chatbot Can Do

- Engage in natural conversation
- Answer general knowledge questions across multiple domains
- Perform task-specific actions using tools
- Dynamically decide when to use a tool versus when to respond directly
- Stream responses live in the terminal
- Run continuously until the user exits

---

## How It Works

1. The user enters a message in the terminal  
2. The input is converted into a structured HumanMessage  
3. A ReAct-based AI agent analyzes the intent of the message  
4. The agent decides to:
   - Respond using its internal knowledge, or
   - Call a registered Python tool  
5. If a tool is called:
   - The function executes
   - The result is passed back to the agent  
6. The final response is streamed back to the terminal  

This reasoning and action loop allows the chatbot to behave intelligently instead of following fixed rules.

---

## Tools Available

### Calculator Tool
- Adds two numbers
- Demonstrates how the AI can delegate precise tasks to code

### Greeting Tool
- Greets users by name
- Shows parameter extraction from natural language

Tools are optional and invoked only when the agent decides they are required.

---

## Technologies Used

### Python
Core language used to build the CLI application and tools

### OpenAI Large Language Model
Provides natural language understanding and generation  
Handles reasoning and intent detection

### LangChain
Manages prompts, messages, and tool definitions  
Connects the LLM with structured workflows

### LangGraph
Controls agent behavior using a graph-based execution model  
Enables ReAct architecture and streaming responses

### dotenv
Loads environment variables securely  
Keeps API keys out of source code
