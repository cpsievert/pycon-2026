
## Title

Intro to Safe, Reliable, and Maintainable AI Apps in Python

---

## Description

Large Language Models (LLMs) are transforming how we build applications, but the path from "cool demo" to "production-ready tool" is littered with challenges: hallucinations, vendor lock-in, security concerns, explainability, and more. This tutorial covers the basics of how to build AI apps that avoid these challenges, yet are still effective and simple to build.

We'll start with [**querychat**](https://pypi.org/project/querychat/), an open-source package that lets users explore data through natural language. querychat demonstrates a powerful pattern: rather than letting an LLM access raw data directly (where it can hallucinate calculations), it constrains the LLM to generate SQL queries that are displayed and executed by a proper database engine. This "tool-based" architecture ensures reliability through transparency and precision -- users see exactly what query was executed along with it's exact results.

From there, we'll peel back the layers to reveal [**chatlas**](https://pypi.org/project/chatlas/), the foundation powering querychat. chatlas provides a unified, provider-agnostic interface to 19+ LLM providers (OpenAI, Anthropic, Google, local models via Ollama, and more). You'll learn how chatlas makes it trivial to:

- Build multi-turn conversations with history management
- Stream responses in real-time for responsive UIs
- Switch between providers with minimal code changes
- Define custom tools that let LLMs interact with external systems (safely)
- Extract structured data using Pydantic models

By the end of this tutorial, we'll have built two complete apps: a data exploration chatbot (using querychat with your own data) and a custom AI assistant with tools you define. You'll leave with practical patterns for constraining LLM behavior, validating outputs, and building apps that are genuinely useful, maintainable and production ready.

---

## Audience

This tutorial is for Python developers who want to build LLM-powered apps but aren't sure where to start -- or who have tried and found the experience frustrating or challenging. If you've used ChatGPT, Claude, or Gemini and wondered how to harness that similar capabilities in your own apps without wrestling with complex frameworks, you're in the right place. We'll show you how to build maintainable AI apps with surprisingly little code, using tools designed to handle the tedious parts for you. You should be comfortable writing Python functions and classes, and familiar with conversational AI tools as a user. This is not a tutorial about training models or deep learning—it's about building practical applications that use LLMs as a component, with an emphasis on patterns that are simple to maintain and reliable in production.

---

## Format

The outline section includes *Hands-on* label for portions of the tutorial where attendees will be expected to perform coding exercises. These exercises will start with a template and the exercise will be to tweak the template to accomplish a certain task.

---

## Outline (3 hours)

**LLMs: embrace the good, engineer around the bad (30 min)**

- LLM capabilities are jagged
  - Some "easy" tasks (e.g., counting r's in strawberry) they are terrible at, but some "hard" tasks (e.g., coding) they are awesome at!
- Key insight: focus LLMs on what they're good at (language->code) and delegate what they're bad at (computation) to proper (Python) tools
- Intro to querychat: chat with your data using natural language
- *Hands-on* (5-10 min): 
  - Run querychat locally with sample data 

**LLM fundamentals: prompts and tools (30 min)**

- User vs. system prompt
- Context is everything
  - Good AI experiences make it easy to provide the right context to the model
- Intro to tool calling
- *Demo*: Simple prompts and tools in chatlas
- *Hands-on* (10 min):
  - Run chatlas locally with some sample prompts/tools
  - Propose exercises to re-inforce mental model of prompts, tools, etc. 

**Break (10 min)**

**querychat: how does it work? (30 min)**

- The prompt engineering and tooling behind querychat
  - Discuss why it's safe and reliable
- Various ways of using querychat: notebook, streamlit, shiny, etc.
- Build your own UI on top of the programmatic endpoints
- *Hands-on* (10 min):
  - Run a pre-built custom querychat app
  - Tweak it to add the generated SQL

**Break (10 min)**

**chatlas: a deeper dive into capabilities (60 min)**

- Structured data
- Image generation
- Built-in tools
- Async streaming
- Building custom UIs
  - Including customizing of tool displays
- Evals via Inspect AI
- *Hands on* (10 min):
  - Write your own chatlas chatbot

**Recap and sendoff (10 min)**

---

## Past experience

Joe Cheng is CTO and first employee at [Posit](https://posit.co/). He has been maintaining open source software for over 15 years. More recently, he has been leading Posit's AI efforts in the form of Positron Assistant, Databot, querychat, and more. He has also given numerous keynotes and workshops over the years on a variety of technical subjects.

Carson Sievert is a principal software engineer at [Posit](https://posit.co/) where he maintains of numerous open source projects such as chatlas, querychat, plotly, and shiny. Carson has been contributing to open source for over a decade, and has delivered many talks and workshops on open source tooling over the years.

--- 

## Example presentations

https://www.youtube.com/watch?v=Kk3xZpKKMyE
https://www.youtube.com/watch?v=owDd1CJ17uQ

---

## Internet requirements

Attendees will likely be asked to sign up for a (free) Github account and also download an open source model before the event. Ideally, exercises that depend on an LLM will work through Github model marketplace (i.e., the internet), but running an LLM locally will serve as a backup option.
