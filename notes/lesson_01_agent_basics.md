# Lesson 1: Introduction to Agentic AI

## Project: AI Data Analyst Agent

This repository documents my journey of learning and building an AI-powered Data Analyst Agent from beginner to advanced level.

---

## What is Artificial Intelligence?

Artificial Intelligence (AI) is a broad field that enables computers to perform tasks that normally require human intelligence.

Examples include:

* Image recognition
* Language translation
* Predictions
* Recommendations
* Spam detection

---

## What is Generative AI?

Generative AI is a type of AI that can create new content.

It can generate:

* Text
* Images
* Code
* Music
* Videos

Examples include ChatGPT and other AI models that can generate human-like responses.

---

## What is an LLM?

LLM stands for Large Language Model.

An LLM is trained on large amounts of text, documents, and code. It can understand patterns in language and generate responses by predicting the next token.

In an AI agent, the LLM acts as the brain that helps understand goals, plan tasks, and decide which tools to use.

---

## What is an AI Agent?

An AI Agent is an AI system that can work toward a goal by:

1. Understanding the goal
2. Planning the required steps
3. Using tools
4. Performing actions
5. Observing the results
6. Deciding the next step
7. Repeating the process until the task is completed

---

## Chatbot vs AI Agent

| Chatbot                         | AI Agent                           |
| ------------------------------- | ---------------------------------- |
| Answers questions               | Completes tasks                    |
| Usually gives a single response | Can perform multiple steps         |
| Limited tool usage              | Can use multiple tools             |
| Waits for the next prompt       | Can continue working toward a goal |

---

## Example: AI Data Analyst Agent

### User Request

> Analyze my sales data and identify the region with the highest profit.

### Possible Agent Workflow

1. Read the data file.
2. Identify the relevant columns.
3. Group the data by region.
4. Calculate total profit for each region.
5. Compare the results.
6. Identify the region with the highest profit.
7. Explain the result to the user.

---

## The Five Building Blocks of an AI Agent

### 1. Goal

The objective the agent needs to achieve.

Example:

> Identify the region with the highest profit.

### 2. Brain

The LLM that helps the agent understand the task, plan steps, and make decisions.

Examples include GPT, Gemini, Claude, and Llama.

### 3. Tools

External capabilities used by the agent to perform tasks.

Examples:

* Python
* Pandas
* SQL
* Calculator
* Web search

### 4. Memory

Information the agent can use from previous steps or interactions.

Examples:

* Conversation history
* User preferences
* Intermediate results

### 5. Actions

The tasks performed by the agent.

Examples:

* Read a file
* Execute Python code
* Run a SQL query
* Generate a chart

---

## The Agent Loop

A basic AI agent follows this process:

Goal
↓
Think
↓
Plan
↓
Use Tool
↓
Observe Result
↓
Decide Next Step
↓
Complete Goal

If the goal is not completed, the agent can repeat the process.

---

## My Key Learning

The most important concept I learned in this lesson is that an AI agent does not simply answer a question. It can work toward a goal by planning steps, using tools, observing results, and deciding what to do next.

I also learned to separate the components of an agent into:

**Goal + LLM (Brain) + Tools + Memory + Actions**

This foundation will be used throughout the development of my AI Data Analyst Agent.
