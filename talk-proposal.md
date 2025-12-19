## Title

The Prime Directive Meets AI: Correctness, Transparency, and LLMs

## Description

The capabilities of large language models (LLMs) are "jagged": they excel at "hard" tasks like coding, while also failing miserably (yet confidently!) at "simple" tasks like counting. For Python developers in scientific and data-heavy fields, these limitations conflict with the "Prime Directive" of their technical work -- the moral obligation to provide results that are correct, transparent, and reproducible. However, with proper guardrails and transparent tooling in place, humans can still verify, reproduce, and ultimately trust results that were produced with help from an LLM.

In this talk, we'll discuss how certain guardrails can lead to more inherently trustworthy AI systems. At the same time, removing guardrails can lead to more compelling experiences for trustworthy users. Choosing the right set of guardrails largely depends on your trust in users to avoid costly mistakes. These arguments will be framed in experience building open source tools to make Pythonistas more effective with AI, with a particular focus on data science use cases.

## Outline

### LLMs: embrace the good, engineer around the bad (10 min)

- LLM intelligence is "jagged"
- Focus LLMs on what they're good at (e.g., language->code) and delegate what they're bad at (e.g., computation) to proper tooling

### Querychat: a constrained, trustworthy, AI tool  (10 min)

- Query your data using natural language.
- Safe and reliable since computation happens in a real SQL database and can be verified by a human.
- Elegant interface in Python makes it easy to build your own UIs in a framework of your choosing.

### Databot: explore data with Python, without _writing_ Python (10 min)

- Ask questions about any data that exists in Python or on your filesystem
- Less safe (but still reliable and verifiable!) since we give it full access to Python
  - A more safe version can be run via Pyodide, but again, access to a filesystem is convenient!

## Relevant links

Querychat website -- https://posit-dev.github.io/querychat/py/
Hello Databot -- https://posit.co/blog/introducing-databot/
Querychat and Databot at SciPy -- https://www.youtube.com/watch?v=Kk3xZpKKMyE