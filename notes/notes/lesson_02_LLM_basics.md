# Lesson 2: How Large Language Models (LLMs) Work.

## Project: AI Data Analyst Agent

In this lesson, I learned how Large Language Models (LLMs) work and how they act as the reasoning component of an AI agent.

---

## What is an LLM?

LLM stands for Large Language Model.

An LLM is trained on large amounts of text, documents, and code. It learns patterns in language and generates responses by predicting the next most likely token based on the context.

In an AI agent, the LLM acts as the brain. It helps the agent understand the user's goal, plan steps, decide which tools to use, and interpret results.

---

## How Does an LLM Generate a Response?

The basic process can be understood as:

User Prompt
↓
Break Input into Tokens
↓
Analyze Context
↓
Predict Next Token
↓
Predict Next Token Again
↓
Continue Until Response Is Complete

The LLM generates responses token by token.

---

## What is a Token?

A token is a piece of text processed by an LLM.

A token is not always a complete word. A word can sometimes be split into multiple tokens.

For example:

```text
ChatGPT
```

could be processed as smaller pieces such as:

```text
Chat + GPT
```

The exact tokenization depends on the model and tokenizer being used.

---

## What is a Context Window?

A context window is the amount of information an LLM can consider at one time while generating a response.

A larger context window allows the model to consider more information, such as:

* Earlier conversation messages
* Documents
* Instructions
* Tool results
* User questions

The context window does not mean permanent memory. It is the information currently available to the model while processing a request.

---

## What is Temperature?

Temperature controls how predictable or creative an LLM's responses are.

### Low Temperature

Low temperature produces more consistent and predictable responses.

Useful for:

* SQL
* Python code
* Data analysis
* Mathematical tasks

### High Temperature

High temperature produces more varied and creative responses.

Useful for:

* Story writing
* Brainstorming
* Marketing ideas
* Creative tasks

### Example

For SQL generation, a low temperature is generally preferred because the goal is to produce consistent and reliable output.

---

## What is AI Hallucination?

An AI hallucination occurs when an AI model generates information that sounds convincing but is incorrect, unsupported, or invented.

This can happen because an LLM predicts likely text rather than automatically verifying every fact.

### How to Reduce Hallucinations

Possible approaches include:

* Providing clear instructions
* Giving the model reliable context
* Using external tools
* Using databases or documents as sources
* Asking the model to acknowledge uncertainty when information is missing
* Verifying important results

---

## LLMs in an AI Agent

In an AI agent, the LLM helps decide what should happen next.

For example:

### User Goal

> Find the top 5 customers by revenue from my Excel file.

### Possible Agent Workflow

1. The LLM understands the user's goal.
2. The LLM plans the analysis.
3. The agent selects an appropriate tool.
4. Python and Pandas read the Excel file.
5. Revenue is calculated for each customer.
6. Customers are sorted by revenue.
7. The top 5 customers are identified.
8. The LLM explains the results to the user.

This approach is more reliable than asking the LLM to guess the answer because the actual calculations are performed using the data.

---

## My Key Learning

The most important concept I learned is that an LLM does not simply store answers like a database. It processes the input as tokens and predicts the next most likely token based on the available context.

I also learned that:

* Tokens are pieces of text
* Context windows determine how much information the model can consider
* Temperature controls the randomness and creativity of responses
* LLMs can hallucinate
* Tools help AI agents perform reliable calculations and access external information

These concepts are important because the LLM acts as the reasoning component that helps an AI agent plan and coordinate tasks.
