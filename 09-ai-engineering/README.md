# Specialization: AI Engineering
Official Curriculum for the AI Engineering Specialization Course in the AI Roadmap.

- **Course Description:** A 15-week specialization that takes engineers from a first traced LLM call to a production-grade agentic system. Learners build progressively — a minimal agent, then tool-calling and structured outputs, then controlled agent loops and multi-agent orchestration, then advanced context engineering through RAG, memory and fine-tuning — before hardening the result with evaluation, guardrails and deployment.

- **Course Objective:** Equip learners to design, build, evaluate, secure and ship production-grade LLM and agentic systems, and to justify their engineering decisions with traces, metrics and cost data rather than intuition.

- **Skills to be learned:** LangChain, LangGraph, LangSmith, Langfuse, MCP, prompt engineering & prompt caching, tool calling, structured outputs (Pydantic), multi-agent orchestration, vector/hybrid/graph/multi-modal RAG, agent memory, LoRA/PEFT fine-tuning, LLM-as-judge evaluation, guardrails & prompt-injection defence, Docker, FastAPI, Ollama, cost & latency optimisation

## Curriculum Breakdown
**Module 1: AI Engineering Foundations (Weeks 1–4)**

### Week 1: Foundations of Agentic AI
> **Objective:** Establish the mental model and vocabulary of agentic systems: learners will be able to explain the transformer architecture at an engineer's level of abstraction — tokens, context window, attention, next-token prediction — distinguish an agent from a plain model call, justify a model choice on cost, latency and capability grounds, and build and trace a minimal working agent using LangChain and LangSmith.
- Understanding LLMs: Transformers, Diffusion, Multi-modality
- Understanding agents & LLMs for engineers: model economics (pricing units, context-window cost, latency vs. quality trade-offs); model selection (benchmarking candidates against *your* task rather than leaderboards, open-weight vs. API, small vs. frontier); routing and cascades (routing by task type and difficulty, cheap-model-first cascades with escalation, measuring the cost/quality delta)
- Your first agent: the minimal agent abstraction; model + prompt + one trivial tool
- LangChain core: models, prompts, chains; LangSmith tracing on from day one to *see* the call
- **Projects:** 

### Week 2: Prompting & Tool-Calling
> **Objective:** Turn a model into a controllable component: learners will be able to write prompts that produce reliable, machine-consumable output, enforce structure with Pydantic schemas, design and register tools that the model calls correctly and cheaply, connect an agent to an external MCP server, and defend a prompt change with a measured before-and-after score rather than an impression.
- Prompt engineering: decomposition, zero/few-shot, chain-of-thought, system vs user roles; prompt caching — stable-prefix design, what is and isn't cacheable, cache hit/miss economics
- Structured outputs: parsers, Pydantic schemas, validation; machine-consumable outputs
- Tool calling: tool/function schemas, when the model should call a tool, error handling, tool design (building tools vs LangChain tools); throughput engineering — parallel tool calls, async execution, batching, rate-limit backoff and retries
- MCP: what it is and why (interoperable tools); connecting an agent to an MCP server/tool
- Eval set + one metric: building a small eval set (15–25 cases) from real failures; choosing **one** deterministic metric to start (exact match, schema-valid, correct-tool-called) with no LLM-judge yet; running it in LangSmith and recording a baseline to defend for the rest of the course (Practical: eval the tool-calling agent, make one prompt change, and show with numbers whether it improved or regressed)
- **Projects:** 


### Week 3: Agent Loops with LangGraph
> **Objective:** Move from a single call to a controlled, recoverable loop: learners will be able to model an agent as an explicit LangGraph state machine, set stopping criteria that prevent runaway execution, persist and resume a run across failure, and decide on evidence whether a task needs a workflow, a single agent, or sub-agents with isolated context.
- The agent loop formalised: goal → decide → act → observe; LangGraph nodes, edges, state
- Control flow with LangGraph: conditional edges, cycles, stopping criteria, durable execution and state persistence (checkpointers, crash recovery, resuming interrupted runs, idempotent tool calls)
- Right-sizing — when to break an agent into sub-agents. **Context bloat:** how context degrades over a long run; token budgeting, compaction/summarisation under context pressure, pruning stale tool results. **Context isolation:** giving sub-agents their own context window; what crosses the boundary vs. what stays local; isolation as the reason to split, not task labels
- When to do what? Workflow vs. single agent vs. multi-agent; the simplest thing that works; anti-patterns with in-depth reading
- **Projects:** 

### Week 4: Multi-Agent Orchestration
> **Objective:** Coordinate multiple agents without losing control of the system: learners will be able to select an orchestration topology — hand-off, supervisor, or decentralised — for a given problem, implement delegation and parallel fan-out, explain what the A2A protocol standardises, and articulate the failure modes and cost multipliers that make multi-agent the wrong default.
- Hand-off patterns: Sequential, Executor-Validator
- Supervisor patterns: Hierarchical Delegation, Parallel Fan-out
- Decentralised patterns: Agent Swarm, Parallel Dispatch, Agent Teams (Queue)
- A2A Protocol
- **Projects:** 

**Module 2: Advanced Context Engineering and Fine Tuning (Weeks 5–8)**

### Week 5: Retrieval & Vector RAG Foundations
> **Objective:** Build a retrieval system that works and know why it works: learners will be able to decide when retrieval beats a larger context window, choose between structured and vector retrieval for a given source, build an end-to-end vector pipeline with loaders, embedding models and a vector store, and measure retrieval quality with precision and recall instead of eyeballing answers.
- Retrieval foundations: when do we need retrieval? When sources exceed context windows (Practical: how to do retrieval if sources are structured — SQL/structured folders)
- Vector RAG foundations: how does vector RAG work? When basic retrieval breaks, i.e. no structured data (Practical: vectorisation using document loaders, embedding models and vector stores)
- Vector retrieval: what makes retrieval good or bad; measuring retrieval precision/recall; failure modes (Practical: build an agent that answers from a vector store)
- Vector RAG optimization: chunking strategies; embedding choices (multi-modal embedding); top-k & metadata filtering
- **Projects:** Build a Vector RAG system for Healthcare, Legal or Research

### Week 6: Advanced, Multi-modal & Graph RAG
> **Objective:** Take a working retrieval system to production quality: learners will be able to diagnose a failing retrieval and apply the right fix — hybrid search, re-ranking, or query transformation — route across multiple stores, handle multi-modal and graph-structured sources, and quantify the cost and accuracy trade-off of each optimisation against their Week 5 baseline.
- Advanced vector RAG optimisation: hybrid approach — keyword (BM25) + vector; re-ranking; query transformation/expansion & multi-query
- Cost-aware RAG: cache-augmented generation; agentic RAG with 2+ vector databases (routing)
- Multi-modal RAG: handling documents with a mix of text, images, etc.
- Graph RAG: knowledge graphs, when vectorisation fails and how graphs fix that (Practical: retrieval system using knowledge graphs)
- **Projects:** Optimise the Week 5 vector RAG, add graphs and compare output

### Week 7: Memory
> **Objective:** Give agents state that survives the conversation: learners will be able to distinguish memory from retrieval and choose correctly between them, manage conversation state under context-window pressure, implement long-term cross-session recall with explicit read and write policies, and reason about staleness, privacy, and what an agent should deliberately forget.
- Memory vs. retrieval revisited: what persists vs. what's fetched; types (short/long-term, episodic, semantic)
- Session memory: conversation state, summarisation, context-window management under memory pressure
- Long-term / cross-session memory: storing, updating, recalling; memory stores; read vs. write policies
- Memory architectures & pitfalls: what to remember, staleness, privacy; integrating memory into an agent
- **Projects:** 

### Week 8: Fine Tuning
> **Objective:** Treat weight-level adaptation as a last resort with evidence behind it: learners will be able to diagnose whether a quality gap calls for better prompting, better retrieval, or fine-tuning, curate and format a training dataset, run a LoRA fine-tune on a small open-weight model within realistic compute limits, and prove the result beats both the base model and a prompted baseline.
- When to fine tune: fine-tuning vs. retrieval vs. prompting — what actually changes at the weights level vs. what doesn't (Practical: check the outputs of a model and decide whether it needs fine-tuning, better retrieval, or better prompting)
- The fine-tuning workflow and techniques: dataset preparation → training → versioning; LoRA/PEFT fundamentals — adapters, the hyperparameters that matter, realistic compute requirements (Practical: curate and format a small fine-tuning dataset)
- Running a fine-tune: the end-to-end training run — monitoring, checkpoints, reading early failure signals (Practical: run a guided LoRA fine-tune on a small open-weight model)
- Evaluating a fine-tune: comparing against the base model and a prompted baseline; spotting overfitting vs. wrong-problem framing (Practical: take a real quality gap, choose an adaptation path with evidence, then implement and evaluate it)
- **Projects:** 

**Module 3: AI Systems in Production (Weeks 9–12)**
### Week 9: Tracing & Basic Evaluation — LangSmith
> **Objective:** Make agent behaviour observable and measurable: learners will be able to instrument chains and agents so that every step is inspectable, read a trace to locate the cause of a failure, assemble eval sets with ground truth, choose appropriate retrieval and generation metrics, and build an LLM-as-judge while accounting for its known biases.
- Tracing: instrumenting chains/agents; reading traces to debug; what to log
- Evaluation foundations: why eval is the dividing line; eval sets, ground truth, offline vs. online
- Metrics & LLM-as-judge: choosing retrieval + generation metrics; building judges; judge pitfalls
- Running evals: LangSmith and Langfuse datasets/experiments; error analysis; cost-aware RAG
- **Projects:** 

### Week 10: Advanced Evaluation and Monitoring — Langfuse
> **Objective:** Run evaluation as the engineering discipline that gates releases: learners will be able to set quality bars and decide release readiness from eval results rather than intuition, calibrate a judge against hand-labelled ground truth and state how far to trust it, catch regressions across prompt, model, RAG and fine-tuning changes, and close the loop by turning production traces and drift into new eval cases.
- Eval-driven development: from ad hoc checks to eval as the backbone of iteration — setting quality bars, deciding release readiness from eval results, not gut feel
- Grading: building and calibrating an LLM-as-judge against human-labelled ground truth; rubric grading vs. deterministic checks; pairwise comparison; known judge pitfalls (bias, inconsistency, gameable rubrics) (Practical: build a judge in Langfuse, calibrate it against a small hand-graded gold set, and quantify how much you trust it)
- Regression testing & experiment tracking: datasets as guardrails — catching regressions across prompt, model, RAG and fine-tuning changes; running experiments head-to-head in Langfuse; evaluating agent performance using MLflow scoring and tracing
- Production monitoring and feedback loops: online evaluation in production; drift detection (input drift, behaviour drift); alerting on quality/cost/latency; closing the loop by turning production traces and user feedback into new eval cases (Practical: instrument the deployed agent with Langfuse production tracing, simulate drift, catch it, and feed the failing case back into the eval set)
- **Projects:** 

### Week 11: Safety, Security and Guardrails
> **Objective:** Build agents that fail safely under adversarial and untrusted input: learners will be able to enforce and repair structured output, ground claims in sources with citations, defend against prompt injection and tool abuse, detect and handle PII, design retries, fallbacks and graceful degradation, and prevent data leakage across tenants.
- Input and output validation and grounding: structured-output enforcement, schema conformance, rejecting and repairing bad output; hallucination detection, grounding output in sources, citation
- Injection defence and PII protection: prompt-injection and tool-abuse, handling untrusted input and content; PII detection and handling
- Guardrails: safe failure modes and resilience — retries, fallbacks, timeouts, graceful degradation; content filtering, rate limiting, abuse prevention
- Data security and risk: tenancy, isolation, preventing leakage across users; legal/licensing requirements for data sources to avoid legal risk
- **Projects:** 

### Week 12: Serving, Cost Optimization and Integration
> **Objective:** Ship and operate the system within real cost and latency budgets: learners will be able to containerise and deploy an agent, serve local and offline models, apply token-level and caching optimisations with measured savings rather than assumed ones, and read and present current research on inference efficiency to peers.
- Docker deployment: Ollama, FastAPI
- Serving local models
- Offline tiny models
- Cost & latency optimization techniques: token-level, caching, etc.
- Student presentation: assign research papers to students to present different techniques
- **Projects:** 

**Capstone & Buffer (Weeks 13–15)**
### Week 13 - 15: Capstone Project — Build, Buffer & Next Steps
- Scope and build the capstone system, applying the agent, tool-calling, retrieval and memory patterns from Modules 1–2
- Evaluate, harden and deploy the capstone, then present it: eval results, guardrails, cost and latency figures
- **Optional Bonus Lessons:** Bridging course — FastAPI backend development (recommended for learners without backend experience)

- **Post-Capstone AI Tooling & Certification:** Databricks, CrewAI, AWS Bedrock & SageMaker


- **Projects:** Capstone build 


## Course Contributors
### Course Owner(s)
- Cyril Michino
- Christopher Aloo

### Acknowledgements and Resources
- [Choosing the Right Multi-Agent Architecture](https://www.langchain.com/blog/choosing-the-right-multi-agent-architecture) — LangChain
- [Multi-Agent Coordination Patterns](https://claude.com/blog/multi-agent-coordination-patterns) — Anthropic
- [Building Multi-Agent Systems: When and How to Use Them](https://claude.com/blog/building-multi-agent-systems-when-and-how-to-use-them) — Anthropic
- [LangChain Documentation](https://python.langchain.com/docs/introduction/)
- [LangGraph Documentation](https://langchain-ai.github.io/langgraph/)
- [LangSmith Documentation](https://docs.smith.langchain.com/)
- [Langfuse Documentation](https://langfuse.com/docs)
- [Model Context Protocol (MCP)](https://modelcontextprotocol.io/)
