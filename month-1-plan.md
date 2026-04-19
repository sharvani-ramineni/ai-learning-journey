# Month 1 — AI Learning Plan

**Goal:** Deeply understand how LLMs work and build a working agent. By the end of this month: a from-scratch tiny GPT, a working prompt chain, and a tool-using research agent.

---

# Week 1 — How LLMs actually work

## Day 1 — Tokens and tokenization

**What I'll learn:** How LLMs break text into tokens, why different inputs cost different amounts, and why "strawberry" splits weirdly.

**What I'll build:** Tokenize 5 different input types (English, code, emoji, non-English, tricky words) and count tokens.

---

## Day 2 — Embeddings

**What I'll learn:** How text gets converted into numbers that capture meaning, and what "semantic similarity" actually looks like numerically.

**What I'll build:** Embed 10 sentences, compute cosine similarity matrix, find the closest and farthest pairs.

---

## Day 3 — Attention (part 1)

**What I'll learn:** The core mechanism that makes transformers work — scaled dot-product attention.

**What I'll build:** Implement attention from scratch in NumPy for a toy input. No frameworks, just math.

---

## Day 4 — Attention (part 2, multi-head)

**What I'll learn:** Why one attention head isn't enough and what multi-head attention captures.

**What I'll build:** Extend Day 3 to 2-head attention. Visualize what each head attends to.

---

## Day 5 — Sampling and hallucination

**What I'll learn:** How LLMs choose the next token (greedy, top-k, top-p, temperature) and why they hallucinate.

**What I'll build:** Generate from GPT-2 at different temperatures. Find where output breaks and understand why.

---

## Day 6 (Saturday) — Bigram language model from scratch

**What I'll learn:** The simplest possible language model, coded from zero. Foundation for building a full GPT next week.

**What I'll build:** A bigram model trained on Tiny Shakespeare. Every line typed by hand — no copy-paste.

---

## Day 7 — Week 1 review + content

---

# Week 2 — Building the GPT + understanding scale

## Day 8 — Self-attention in code

**What I'll learn:** How self-attention gets implemented inside a real model.

**What I'll build:** Extend the Day 6 bigram to include self-attention.

---

## Day 9 — Positional embeddings + transformer blocks

**What I'll learn:** How the model knows word order, and how blocks stack to form a full transformer.

**What I'll build:** Add positional embeddings and stack transformer blocks.

---

## Day 10 — Full GPT + training

**What I'll learn:** Putting it all together — a complete (tiny) GPT that generates text.

**What I'll build:** Train a full tiny GPT. Generate text. Save the model.

---

## Day 11 — Read the original paper

**What I'll learn:** "Attention Is All You Need" — the paper that started it all. Readable now that I've built the thing.

**What I'll do:** Map every piece of my Day 10 GPT to the paper's figures and equations.

---

## Day 12 — Scaling laws

**What I'll learn:** Why bigger models work better, and what predicts performance — parameters, data, or compute.

**What I'll build:** Plot loss curves from training runs with different model sizes.

---

## Day 13 (Saturday) — RLHF and instruction tuning

**What I'll learn:** How a base model becomes a helpful assistant. RLHF, Constitutional AI, and the training signal behind "helpfulness."

**What I'll do:** Polish the nanoGPT repo with a clean README.

---

## Day 14 — Week 2 review + content

---

# Week 3 — Working with LLMs via APIs

## Day 15 — API basics

**What I'll learn:** How to call LLM APIs from Python. System prompts, messages, and response handling.

**What I'll build:** 3 API calls with different system prompts.

---

## Day 16 — Prompt engineering principles

**What I'll learn:** What makes a good prompt vs a bad one. Concrete techniques, not vibes.

**What I'll build:** Same task, 3 prompt versions (bad/OK/good). Compare outputs.

---

## Day 17 — System prompts, few-shot, chain of thought

**What I'll learn:** Few-shot examples, chain-of-thought prompting, and how to structure system prompts.

**What I'll build:** Add few-shot + CoT to prior task. Measure the quality gain.

---

## Day 18 — Structured outputs

**What I'll learn:** How to get reliable JSON from LLMs and handle the failure cases.

**What I'll build:** Strict JSON output with malformed-JSON error handling.

---

## Day 19 — Cost, latency, and model selection

**What I'll learn:** How to choose the right model for the job. When cheap/fast beats expensive/smart.

**What I'll build:** Run the same task on different models. Compare quality, latency, and cost.

---

## Day 20 (Saturday) — Prompt chain project

**What I'll learn:** How to chain multiple LLM calls into a pipeline.

**What I'll build:** A 2-step chain: extract claims from an article → generate critical questions per claim. Clean CLI, pushed to GitHub.

---

## Day 21 — Week 3 review + content

---

# Week 4 — First real agent

## Day 22 — What "agent" actually means

**What I'll learn:** The real definition of agent vs. workflow. What makes something agentic vs. just a prompt chain.

**What I'll do:** Read 3 different takes on "what is an agent" and write my own definition.

---

## Day 23 — Tool use basics

**What I'll learn:** How LLMs call external functions. The mechanics of tool use.

**What I'll build:** Single-turn tool use with a mock `get_weather(city)` function. End to end working.

---

## Day 24 — Multi-turn tool use

**What I'll learn:** How agents call multiple tools in sequence and combine results.

**What I'll build:** Agent that calls `get_weather()` AND `get_current_time()` and combines them into one answer.

---

## Day 25 — The ReAct pattern

**What I'll learn:** The thought → action → observation loop that most agents use under the hood.

**What I'll build:** Refactor the agent to explicitly log its reasoning trace.

---

## Day 26 — Why agents fail

**What I'll learn:** Context rot, tool confusion, planning loops — the real failure modes of agents.

**What I'll do:** Intentionally break my agent with ambiguous queries, erroring tools, and missing tools. Document every failure mode.

---

## Day 27 (Saturday) — Research agent capstone

**What I'll build:** A research assistant that takes a topic → searches the web → summarizes → returns a 300-word briefing with citations. Pushed to GitHub with a proper README.

---

## Day 28 — Month 1 retrospective

Honest reflection on what clicked, what's still fuzzy, and what Month 2 should focus on.

---

# End of Month 1

**What I'll have shipped:**
- A from-scratch tiny GPT (Karpathy-style)
- A working prompt chain
- A tool-using research agent
- 4 weekly write-ups on Medium + Substack
- A solid mental model of: tokens, embeddings, attention, sampling, training, scaling, prompting, tool use, and agent loops

**Month 2 preview:** RAG systems, vector databases, MCP, and multi-agent orchestration.
