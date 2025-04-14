# Runnables in LangChain
#### In LangChain, runnables are a unified interface for executing components in a modular, composable, and asynchronous way. They were introduced to provide a consistent and flexible way to chain together different parts of a language model-powered pipeline (like prompts, models, output parsers, tools, etc.).
## What is a Runnable?
#### A Runnable is an abstraction that represents any step in a language application pipeline. It could be:
#### A prompt template
#### A language model
#### A parser
#### A retriever
#### A function
#### Or a chain of these steps
##  Common Runnable Types:
#### *RunnableLambda:* Wraps any Python function as a Runnable.
#### *RunnableSequence:* Chains multiple Runnables in sequence (like a pipeline).
#### *RunnableMap:* Runs multiple Runnables in parallel on the same input.
#### *RunnableParallel:* Like RunnableMap but returns the results as a list.
#### *RunnableBranch:* Adds conditional logic (like if-else) to the chain.
#### *RunnablePassthrough:* Passes input directly to output without change.
## Why Runnables were introduced in LangChain:
#### Runnables came to address limitations and complexities of the older Chain API. They were introduced to overcome the drawbacks of Chain components.
## Drawbacks of Chains:
### Inflexible Composition:
####        Chains were tightly coupled and hard to combine in dynamic ways.
### Inconsistent Interfaces:
####        Different components (models, prompts, tools) had inconsistent input/output patterns.
### Poor Async Support:
####        Difficult to handle async and streaming efficiently in Chains.
### Limited Debugging & Tracing:
####        Tracing and observability tools were harder to integrate cleanly.
##  Benefits of Runnables:
#### Unified and modular interface
#### Easy chaining, branching, and parallel execution
#### Native async and streaming support
#### Better debugging, logging, and deployment
