# Lesson 4: AI APIs

## Project: AI Data Analyst Agent

In this lesson, I learned how a Python application communicates with an AI model through an API.

I also built my first interactive Python application using the Gemini API.

---

## What is an API?

API stands for **Application Programming Interface**.

An API allows different software applications or services to communicate and exchange information.

A simple example:

```text
Python Application
        ↓
      API
        ↓
    AI Model
        ↓
     Response
        ↓
Python Application
```

---

## What is an API Key?

An API key is a secret credential used to authenticate an application when accessing an API.

For example:

```text
Python Application
        ↓
     API Key
        ↓
      API
        ↓
    AI Model
```

API keys should never be shared publicly or uploaded to GitHub.

---

## API vs API Key vs API Quota

| Term      | Meaning                                           |
| --------- | ------------------------------------------------- |
| API       | Communication interface between software systems  |
| API Key   | Credential used to access an API                  |
| API Quota | Limit on how much or how often an API can be used |

---

## What is an SDK?

SDK stands for **Software Development Kit**.

A Python SDK provides tools that make it easier for Python programs to communicate with an external service.

For this project, I used the Gemini Python SDK.

```python
from google import genai
```

The SDK acts as a convenient layer between our Python application and the Gemini API.

```text
Python Code
     ↓
Python SDK
     ↓
Gemini API
     ↓
Gemini Model
```

---

## API vs Python Library

A Python library is a collection of code that can be imported and used inside a Python program.

Example:

```python
import pandas as pd
```

Pandas runs inside the Python environment.

An API allows a program to communicate with another service.

```text
Python Program
      ↓
    Internet
      ↓
External Service
```

In simple terms:

> **Library = code you use inside your program**

> **API = communication with another service**

---

## API Key Security

I learned that API keys should not be written directly into code that will be uploaded to GitHub.

Instead, I stored my API key using **Google Colab Secrets**.

The secret was stored using:

```text
GEMINI_API_KEY
```

Then Python accessed it securely:

```python
from google.colab import userdata

api_key = userdata.get("GEMINI_API_KEY")
```

I did not print or upload the actual API key.

---

## Connecting Python to Gemini

First, I installed the Gemini Python SDK:

```python
!pip install -q google-genai
```

Then I imported the SDK:

```python
from google import genai
```

I created a Gemini client:

```python
client = genai.Client(api_key=api_key)
```

Then I sent a prompt to the Gemini model:

```python
response = client.models.generate_content(
    model="gemini-flash-latest",
    contents="Explain what an AI agent is in simple English."
)

print(response.text)
```

---

## Dynamic Prompts

Instead of hardcoding a question, I learned how to store a question in a variable.

```python
question = "What is an AI agent?"
```

I then used an f-string to insert the variable into the prompt:

```python
response = client.models.generate_content(
    model="gemini-flash-latest",
    contents=f"""
You are an AI instructor.

Answer the following question for a beginner:

{question}

Use simple English.
Give one real-world example.
Keep the answer under 100 words.
"""
)
```

The `{question}` placeholder is replaced with the value stored in the variable.

---

## Multi-line Strings

I learned that triple quotes can be used to create multi-line strings in Python.

Example:

```python
prompt = """
You are an AI instructor.

Explain AI agents in simple English.

Keep the answer under 100 words.
"""
```

Triple quotes make long prompts easier to read and maintain.

---

## User Input

I then made the application interactive using `input()`:

```python
question = input("Ask me a question: ")
```

This allows the user to enter a question while the program is running.

The flow becomes:

```text
User enters question
        ↓
input()
        ↓
question variable
        ↓
Prompt template
        ↓
Gemini API
        ↓
AI response
```

---

## Conversation Loop

I used a `while` loop to allow the user to ask multiple questions.

```python
while True:

    question = input("Ask me a question (type 'exit' to stop): ")

    if question.lower() == "exit":
        print("Goodbye!")
        break
```

The `while True` loop keeps the program running.

The `break` statement stops the loop when the user types `exit`.

---

## Error Handling

API requests can fail.

I learned how to use `try` and `except` to handle errors:

```python
try:
    response = client.models.generate_content(
        model="gemini-flash-latest",
        contents=question
    )

    print(response.text)

except Exception as e:
    print("Something went wrong:", e)
```

This prevents the application from immediately stopping when an error occurs.

---

## Handling API Quota Errors

During this lesson, I encountered a real API error:

```text
429 RESOURCE_EXHAUSTED
```

This happened because the available free-tier API quota had been exceeded.

I learned that API failures can happen even when the Python code is correct.

I also learned how to provide a more user-friendly message:

```python
except Exception as e:

    if "429" in str(e):
        print(
            "The AI service quota has been reached. "
            "Please try again later."
        )

    else:
        print("An unexpected error occurred.")
```

Instead of showing a long technical error to a non-technical user, the application can provide a simple explanation.

---

## AI Agent Connection

The API allows our future AI Data Analyst Agent to communicate with an LLM.

The basic architecture is:

```text
User
 ↓
Python Application
 ↓
Prompt
 ↓
AI API
 ↓
LLM
 ↓
Decision
 ↓
Tool
 ↓
Result
 ↓
LLM
 ↓
Final Answer
```

The LLM can decide what needs to be done, while Python and tools can perform calculations and other actions.

For example:

```text
User:
Find the top 5 customers by revenue.

        ↓

LLM:
This requires data analysis.

        ↓

Python/Pandas:
Read data → Calculate revenue → Sort → Top 5

        ↓

LLM:
Explain the result to the user.
```

---

## Key Learnings

In this lesson, I learned:

* What an API is
* What an API key is
* What API quotas are
* What an SDK is
* Difference between an API and a Python library
* How to securely store an API key
* How to connect Python to Gemini
* How to send prompts through an API
* How to use variables in prompts
* How to create multi-line prompts using triple quotes
* How to accept user input using `input()`
* How to create a conversation loop using `while`
* How to stop a loop using `break`
* How to handle errors using `try` and `except`
* How to handle API quota errors
* How APIs connect an AI agent to an LLM

---

## Lesson 4 Outcome

I successfully built a basic interactive AI application using Python and the Gemini API.

The application can:

1. Accept a question from the user
2. Send the question to an LLM
3. Receive the AI response
4. Display the response
5. Continue accepting questions
6. Exit when the user types `exit`
7. Handle API errors

This is my first practical step toward building an **AI Data Analyst Agent**.
