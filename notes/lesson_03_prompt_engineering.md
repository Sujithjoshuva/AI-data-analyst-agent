# Lesson 3: Prompt Engineering

## Project: AI Data Analyst Agent

In this lesson, I learned how prompts guide the behavior and responses of Large Language Models (LLMs).

A well-designed prompt can help an LLM understand the task, use the correct context, follow constraints, and return results in a useful format.

---

## What is a Prompt?

A prompt is an instruction or input given to an LLM to guide its response or behavior.

A prompt can include:

* Instructions
* Questions
* Context
* Examples
* Constraints
* Output requirements

In an AI agent, prompts are not just questions. They help guide how the LLM understands a goal, plans actions, and decides how to respond.

---

## The Five Parts of a Strong Prompt

A useful prompt can be structured using:

**Role + Task + Context + Constraints + Output Format**

### 1. Role

The role tells the LLM what perspective or expertise to use.

Example:

> You are an experienced data analyst.

### 2. Task

The task explains what the LLM should do.

Example:

> Analyze the sales data and identify the top-performing region.

### 3. Context

Context provides the information needed to complete the task.

Example:

> The dataset contains Region, Sales, and Profit columns.

### 4. Constraints

Constraints define rules for the response and help control unwanted behavior.

Examples:

* Use only the provided data.
* Do not invent numbers.
* If information is missing, clearly state that.
* Use plain English.
* Keep the response under 200 words.

### 5. Output Format

The output format tells the LLM how to structure the response.

Example:

> Return the answer using:
>
> * Findings
> * Insights
> * Recommendations

---

## Weak Prompt vs Strong Prompt

### Weak Prompt

> Analyze this data.

This prompt is unclear because the LLM must guess what should be analyzed and how the answer should be presented.

### Strong Prompt

> You are a data analyst. Analyze the provided sales dataset and identify the top-performing regions based on total sales and profit. Use only the provided data and do not invent missing information. Return the answer using Findings, Insights, and Recommendations.

A strong prompt gives the LLM clearer instructions and helps produce more consistent output.

---

## Zero-Shot Prompting

Zero-shot prompting means giving the LLM a task without providing an example.

Example:

> Classify this customer review as Positive, Negative, or Neutral:
>
> "The delivery was very slow."

---

## One-Shot Prompting

One-shot prompting means providing one example before asking the LLM to perform the task.

Example:

> Classify customer reviews.
>
> Review: "Excellent product and fast delivery."
>
> Sentiment: Positive
>
> Now classify:
>
> Review: "The product stopped working after two days."
>
> Sentiment:

The example helps the LLM understand the expected pattern.

---

## Few-Shot Prompting

Few-shot prompting means providing multiple examples before asking the LLM to complete a similar task.

Example:

> Review: "Excellent quality."
>
> Sentiment: Positive
>
> Review: "Very poor service."
>
> Sentiment: Negative
>
> Review: "The product is okay."
>
> Sentiment: Neutral

The examples guide the model toward the expected type of response.

---

## Role Prompting

Role prompting tells the LLM which perspective or expertise to use.

Example:

> You are a senior data analyst.

Role prompting can guide the style and focus of the response, but it does not automatically give the LLM new knowledge.

---

## Context and Constraints

Context gives the LLM the information needed to complete a task.

Constraints define what the LLM should and should not do.

Example:

> You are analyzing sales data for an electronics company. Revenue increased by 15%, but profit decreased by 10%. Higher discounts were offered during this period.
>
> Explain possible reasons for the decrease in profit. Use only the provided information. Do not invent additional facts.

---

## Prompt Templates

A prompt template is a reusable prompt that contains variables.

Example:

```text
You are a data analyst.

Analyze the following dataset:

{dataset}

Answer the following question:

{question}

Rules:
- Use only the provided data.
- Do not invent information.
- Explain the result clearly.
```

The variables can change depending on the user or task.

For example:

```text
{dataset} → Sales data
{question} → Which region has the highest profit?
```

Prompt templates are useful when building AI agents because the same instructions can be reused for different datasets and questions.

---

## Prompt Design for the AI Data Analyst Agent

Example prompt:

```text
You are an AI Data Analyst.

Analyze the provided sales dataset containing Region, Sales, and Profit columns.

Task:
Identify and rank the top 3 regions by total profit.

Rules:
- Use only the provided data.
- Do not invent or assume missing values.
- If the data is insufficient, clearly state that.
- Use plain English.
- Keep the response under 200 words.

Output format:
1. Findings
2. Insights
3. Recommendation
```

This prompt clearly defines the role, task, context, constraints, and expected output format.

---

## My Key Learning

The most important concept I learned is that a prompt is not simply a question.

A prompt can guide an LLM by providing:

**Role + Task + Context + Constraints + Output Format**

I also learned that:

* Zero-shot prompting provides no examples.
* One-shot prompting provides one example.
* Few-shot prompting provides multiple examples.
* Constraints help control unwanted AI behavior.
* Output formats make responses more structured and consistent.
* Prompt templates allow instructions to be reused for different tasks.

These concepts will be used later when building the AI Data Analyst Agent.
