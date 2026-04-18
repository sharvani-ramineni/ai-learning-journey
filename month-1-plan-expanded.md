# Month 1 — AI Learning Plan

**Profile:** 60 min/day weekdays, ~3 hrs Saturday, strong Python, free tiers only.

**Daily flow (60 min learning + 20 min content):**
1. **Read/watch primary resource** — 25 min
2. **Code in Colab** — 30 min
3. **Write NOTES.md** — 10 min (using template)
4. **Claude Project generates content** — 5 min (paste NOTES, get 3 posts)
5. **Skim + publish** — 10 min (Medium, Substack, LinkedIn)
6. **Commit + push public repo; commit private drafts repo** — 2 min

**Saturday:** 3-hr build session + content (no new reading).
**Sunday:** End-of-week check with Claude Project + weekly summary content.

---

# Week 1 — How LLMs actually work

## Day 1 — Tokens and tokenization

**Primary:** Karpathy, "Let's build the GPT Tokenizer" — first 30 min (YouTube)

**Extra perspectives:**
- Hugging Face, "Summary of the tokenizers" — huggingface.co/docs/transformers/tokenizer_summary
- Simon Willison's blog on tokenizer oddities — simonwillison.net (tag: tokenizer)

**Code:** Install `tiktoken`. Tokenize English, code, emoji, non-English, "strawberry". Print IDs + count.

**Key question for NOTES:** Why does "strawberry" split but "cat" doesn't?

---

## Day 2 — Embeddings

**Primary:** Jay Alammar, "The Illustrated Word2vec" — jalammar.github.io/illustrated-word2vec

**Extra perspectives:**
- Cohere, "Text Embeddings Visually Explained" — cohere.com/llmu/text-embeddings
- Vicki Boykis, "What are embeddings?" — vickiboykis.com/what_are_embeddings (chapters 1-2)

**Code:** `sentence-transformers`. Embed 10 sentences, cosine similarity matrix, find closest/farthest pair.

**Key question:** What does the model think is similar about high-similarity pairs?

---

## Day 3 — Attention (part 1)

**Primary:** Jay Alammar, "The Illustrated Transformer" — stop after attention section

**Extra perspectives:**
- 3Blue1Brown, "Attention in transformers, visually explained" (YouTube)
- Sebastian Raschka, "Understanding and Coding Self-Attention" — magazine.sebastianraschka.com

**Code:** Implement scaled dot-product attention for 4-token, 8-dim input in NumPy (no PyTorch). Print attention matrix.

**Key question:** Why divide by √d_k?

---

## Day 4 — Attention (part 2, multi-head)

**Primary:** Finish "The Illustrated Transformer"

**Extra perspectives:**
- Lilian Weng, "The Transformer Family Version 2.0" — vanilla transformer section
- Peter Bloem, "Transformers from scratch" — peterbloem.nl/blog/transformers

**Code:** Extend Day 3 to 2-head attention. Visualize per-head attention patterns.

**Key question:** What does multi-head capture that single-head can't?

---

## Day 5 — Sampling + hallucination

**Primary:** Hugging Face, "How to generate text" — huggingface.co/blog/how-to-generate

**Extra perspectives:**
- Anthropic docs, temperature + sampling sections
- Chip Huyen, "Sampling for text generation" — huyenchip.com/2024/01/16/sampling.html

**Code:** GPT-2 small via `transformers`. Generate same prompt at temp 0 / 0.7 / 1.5. Try top-p 0.9 vs top-k 50.

**Key question:** At what temperature does output break and why?

---

## Day 6 (Sat, 3 hrs) — Bigram from scratch

**Primary:** Karpathy, "Let's build GPT" — bigram section

**Extra perspectives:**
- Eugene Yan, "Real-time ML: bigram to transformer" — eugeneyan.com
- nanoGPT repo README — github.com/karpathy/nanoGPT

**Code:** Type every line — no copy-paste. Train on Tiny Shakespeare. Generate.

**Key question:** Why is initial loss roughly -ln(1/vocab_size)?

---

## Day 7 — Week 1 summary

Ask Claude Project "end of week 1 check." Answer hard questions. Publish a week-summary post.

---

# Week 2 — Building the GPT + scale

## Day 8 — Self-attention in code

**Primary:** Karpathy "Let's build GPT" — self-attention section

**Extra perspectives:**
- Brendan Bycroft, "LLM Visualization" — bbycroft.net/llm (interactive — incredible)
- Sasha Rush, "The Annotated Transformer" — nlp.seas.harvard.edu/annotated-transformer

**Code:** Extend Day 6 bigram to include self-attention.

## Day 9 — Positional embeddings + blocks

**Primary:** Karpathy "Let's build GPT" — positional + block sections

**Extra perspectives:**
- Eleuther, "Rotary embeddings: A Relative Revolution" — blog.eleuther.ai
- Jay Alammar, "The Illustrated GPT-2"

**Code:** Add positional embeddings + stack blocks.

## Day 10 — Full GPT + training

**Primary:** Finish Karpathy's "Let's build GPT"

**Extra perspectives:**
- Karpathy, "State of GPT" (YouTube)
- Hugging Face NLP Course, Ch 1

**Code:** Train full tiny GPT. Generate. Save model.

## Day 11 — Read the paper

**Primary:** "Attention Is All You Need" (Vaswani et al., 2017)

**Extra perspectives:**
- Yannic Kilcher's "Attention Is All You Need" breakdown (YouTube)
- Re-read "The Annotated Transformer" — hits differently now

**Code:** No new code. Map your Day 10 GPT to paper figures. Comment the code.

## Day 12 — Scaling laws

**Primary:** "Scaling Laws for Neural Language Models" (Kaplan et al., 2020) — skim

**Extra perspectives:**
- Lilian Weng scaling overview
- Dario Amodei, "Machines of Loving Grace" — anthropic.com

**Code:** Plot loss curves at n_embd = 32 / 64 / 128.

## Day 13 (Sat) — RLHF + instruction tuning

**Primary:** Chip Huyen, "RLHF" — huyenchip.com/2023/05/02/rlhf.html

**Extra perspectives:**
- Nathan Lambert, interconnects.ai
- Anthropic, "Constitutional AI" summary

**Code:** Rest day. Polish your nanoGPT repo folder with clean README.

## Day 14 — Week 2 summary

---

# Week 3 — Working with LLMs via APIs

## Day 15 — API basics

**Primary:** Anthropic Quickstart — docs.claude.com

**Extra perspectives:**
- OpenAI Cookbook, "How to call the API"
- Simon Willison's `llm` CLI posts

**Code:** 3 API calls with different system prompts.

## Day 16 — Prompt principles

**Primary:** Anthropic prompt engineering overview

**Extra perspectives:**
- OpenAI GPT best practices
- Learn Prompting guide — learnprompting.org

**Code:** Same task, 3 prompt versions (bad/OK/good). Compare.

## Day 17 — System prompts, few-shot, CoT

**Primary:** Anthropic "Be clear" + "Use examples" + "Let Claude think" docs

**Extra perspectives:**
- Wei et al., "Chain-of-Thought" paper — arxiv.org/abs/2201.11903
- Eugene Yan, "Prompting Fundamentals" — eugeneyan.com/writing/prompting

**Code:** Add few-shot + CoT to prior task. Measure gain.

## Day 18 — Structured outputs

**Primary:** Anthropic docs on tool use / structured output

**Extra perspectives:**
- Instructor library — python.useinstructor.com
- OpenAI JSON mode + function calling

**Code:** Strict JSON output. Handle malformed-JSON failure.

## Day 19 — Cost, latency, model selection

**Primary:** Anthropic pricing + "Choosing a model"

**Extra perspectives:**
- Artificial Analysis — artificialanalysis.ai
- Latent Space, "Benchmarks 201"

**Code:** Same task on Haiku vs Opus. Compare.

## Day 20 (Sat) — Prompt chain project

**Primary:** Anthropic "Building effective agents" — prompt chaining section

**Extra perspectives:**
- Hamel Husain, "Your AI product needs evals" — hamel.dev/blog/posts/evals

**Code:** 2-step chain: extract claims → generate critical questions. CLI. Push to `projects/prompt-chain/`.

## Day 21 — Week 3 summary

---

# Week 4 — First real agent

## Day 22 — What "agent" means

**Primary:** Anthropic, "Building effective agents" — read TWICE

**Extra perspectives:**
- Lilian Weng, "LLM Powered Autonomous Agents"
- Simon Willison, "What are LLM agents?" — simonwillison.net

**Code:** Write your own agent definition in NOTES after reading 3 takes.

## Day 23 — Tool use basics

**Primary:** Anthropic tool use docs

**Extra perspectives:**
- OpenAI function calling guide
- Gorilla paper summary

**Code:** Single-turn tool use with `get_weather(city)` mock.

## Day 24 — Multi-turn tool use

**Primary:** Anthropic multi-turn tool use docs

**Extra perspectives:**
- LangChain Agents conceptual guide — python.langchain.com
- Hugging Face Agents Course — huggingface.co/learn/agents-course

**Code:** Add `get_current_time()`. Agent calls both, combines.

## Day 25 — ReAct

**Primary:** ReAct paper (Yao et al., 2022) — intro + method

**Extra perspectives:**
- Prompting Guide's ReAct page — promptingguide.ai/techniques/react
- Toolformer summary on Lilian Weng

**Code:** Log thought → action → observation → final.

## Day 26 — Why agents fail

**Primary:** Lilian Weng's limitations section

**Extra perspectives:**
- Hamel Husain, "Field Notes on AI Agents" — hamel.dev
- Anthropic engineering blog on context management

**Code:** Break agent on purpose. Document failure modes.

## Day 27 (Sat) — Research agent

**Primary:** Build.

**Extra perspectives:**
- Tavily docs — tavily.com
- Anthropic cookbook — github.com/anthropics/anthropic-cookbook (agents)

**Code:** Research assistant — topic → Tavily search → summarize → 300-word briefing with citations. `projects/research-agent/`.

## Day 28 — Month 1 retrospective

Ask Claude Project "end of month check." Honestly reflect on what's fuzzy. Shape Month 2.

---

# End of Month 1

**You'll have:**
- 24 Colab notebooks, 24 NOTES.md files
- 24 Medium posts + 24 Substack posts + 24 LinkedIn posts
- 3 shipped projects: nanoGPT, prompt chain, research agent
- Green GitHub graph
- Real mental model of: tokens, embeddings, attention, sampling, training, scaling, prompting, tool use, agent loops
