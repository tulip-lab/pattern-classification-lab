# M10 — Large Language Models and Agentic AI

This module uses selected public exercises from [FLIP: Agentic AI in Practice](https://github.com/tulip-lab/agentic-AI-lab) rather than duplicating the notebooks in this repository. Retain each source exercise's original module identity when reporting your work.

## Practical path

1. [M01B — GenAI and Agentic AI Fundamentals](https://github.com/tulip-lab/agentic-AI-lab/blob/develop/M01-Foundations/Jupyter/M01B-GenAI-Fundamentals.ipynb): establish the LLM and agent mental model and identify where prediction, classification, and decision rules appear.
2. [M04B — LangChain Tool-Using Agents](https://github.com/tulip-lab/agentic-AI-lab/blob/develop/M04-Agent-Programming/Jupyter/M04B-LangChain-ToolAgents.ipynb): inspect tool selection, input validation, execution traces, and refusal behaviour.
3. [M08A — Hugging Face Evaluation](https://github.com/tulip-lab/agentic-AI-lab/blob/develop/M08-Agent-Engineering/Jupyter/M08A-HuggingFace-Evaluation.ipynb): define a held-out task set and compare system behaviour with explicit measures and failure categories.

## Pattern Classification focus

Treat prompts, retrieved context, model outputs, tool choices, and agent actions as observable parts of a decision system. Retain the test cases, expected behaviour, outputs, tool traces, quantitative results, and failure analysis needed to compare at least one controlled baseline with the selected LLM or agent workflow.

Do not expose API keys or private data. If an exercise requires a hosted model, keep a credential-free or local fallback for the core analysis and record model/provider versions because behaviour may change over time.
