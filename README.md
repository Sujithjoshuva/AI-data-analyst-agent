# AI Data Analyst Agent

A step-by-step project where I am learning to build an AI Data Analyst Agent using Python, LLMs, APIs, tools, and agentic AI concepts.

The goal is to gradually build an agent that can understand business questions, analyze data, use appropriate tools, and provide clear business insights.

---

## Project Goal

Build an AI Data Analyst Agent that can:

- Understand natural-language business questions
- Work with Excel and CSV datasets
- Perform data analysis
- Use Python and Pandas for calculations
- Use an LLM for reasoning and communication
- Select appropriate tools
- Validate results
- Provide clear business insights
- Handle errors safely

---

## Learning Progress

| Lesson | Topic | Status |
|---|---|---|
| Lesson 1 | AI Agent Basics | Completed |
| Lesson 2 | LLM Fundamentals | Completed |
| Lesson 3 | Prompt Engineering | Completed |
| Lesson 4 | AI APIs & Python SDK | Completed |
| Lesson 5 | Guardrails | Completed |
| Lesson 6 | Tools & Function Calling | Upcoming |
| Lesson 7 | Agent Memory | Upcoming |
| Lesson 8 | Agent Loop | Upcoming |
| Lesson 9 | Building the Data Analyst Agent | Upcoming |
| Lesson 10 | Testing & Evaluation | Upcoming |
| Lesson 11 | Final Portfolio Project | Upcoming |

---

## Concepts Learned

### AI Agent Basics

- Goal
- Brain / LLM
- Tools
- Memory
- Actions
- Agent loop

### LLM Fundamentals

- Large Language Models
- Tokens
- Context window
- Temperature
- Hallucination

### Prompt Engineering

- Role
- Task
- Context
- Constraints
- Output format
- Zero-shot prompting
- One-shot prompting
- Few-shot prompting

### AI APIs

- API
- API key
- API quota
- Python SDK
- API requests and responses
- Error handling

### Guardrails

- Input guardrails
- Output guardrails
- Attempt limits
- Input validation
- Output validation
- Verified Python results
- LLM response verification
- Loop control using `break` and `continue`

---

## Lesson 5 — Guarded AI Data Analyst Agent

In Lesson 5, I built a simple guarded AI Data Analyst Agent.

The workflow is:

**Validate → Calculate → Explain → Verify → Respond**

Python and Pandas calculate and verify the numerical result.

Gemini explains the verified result in natural language.

Input and output guardrails control the agent workflow.

The agent also includes a three-attempt limit for invalid requests.

---

## Technologies

- Python
- Google Colab
- Pandas
- Gemini API
- Gemini Python SDK
- GitHub

---

## Security

API keys and other secrets are not stored in this repository.

API credentials are stored securely using Google Colab Secrets.

The project also uses a `.gitignore` file to prevent sensitive or unnecessary files from being committed.

---

## Project Structure

```text
AI-data-analyst-agent/
│
├── notes/
│   ├── lesson_01_agent_basics.md
│   ├── lesson_02_LLM_basics.md
│   ├── lesson_03_prompt_engineering.md
│   ├── lesson_04_ai_apis.md
│   └── lesson_05_Guarded_AI_Data_Analyst_Agent.ipynb
|
├── .gitignore
└── README.md
