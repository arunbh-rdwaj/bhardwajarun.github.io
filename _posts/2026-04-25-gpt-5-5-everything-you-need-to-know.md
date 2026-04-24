---
title: GPT-5.5 Is Here — Everything You Need to Know
date: 2026-04-24
categories: [AI Tools]
tags: [chatgpt, gpt-5.5, openai, ai, codex, agentic-ai, llm, benchmarks, pricing]
image:
  path: /assets/images/gpt-5-5.png
  alt: GPT-5.5 — OpenAI's Newest AI Model
---

OpenAI dropped GPT-5.5 yesterday — April 23, 2026 — just **seven weeks** after GPT-5.4. Internally codenamed "Spud", it's the first fully retrained base model since GPT-4.5, and OpenAI is calling it *"a new class of intelligence for real work."* Here's everything that actually matters.

---

## What Is GPT-5.5?

GPT-5.5 is OpenAI's latest frontier model, designed primarily for **agentic and multi-step work** — the kind of tasks where previous models needed constant hand-holding. Greg Brockman, OpenAI's President, described it as *"a big step towards more agentic and intuitive computing"* and a foundation for OpenAI's long-discussed **super app** — a unified platform combining ChatGPT, Codex, and an AI browser into one tool for enterprise customers.

The model comes in two variants:

| Variant | Description | Available To |
|---|---|---|
| GPT-5.5 (Thinking) | Faster, smarter answers for complex work | Plus, Pro, Business, Enterprise |
| GPT-5.5 Pro | Deepest reasoning, best for demanding tasks | Pro, Business, Enterprise only |

---

## What's New and Actually Better

### Agentic Coding — The Biggest Jump

GPT-5.5 is now the strongest coding model OpenAI has ever shipped. You can hand it a **messy, multi-part engineering problem** without step-by-step prompting — it plans, uses tools, checks its own work, and works toward a result autonomously.

Early testers reported saving up to **10 hours of work per week** on engineering tasks. One founder described asking GPT-5.5 to diagnose and rewrite a broken system that had stumped his best engineer for days — GPT-5.4 couldn't do it; GPT-5.5 could.

With GPT-5.5, **Codex** now goes further too — it can interact with web apps, test flows, click through pages, capture screenshots, and iterate on what it sees until the task is done.

### Long-Context — A Massive Leap

This is arguably the most impressive improvement. On the MRCR v2 benchmark — which tests how reliably a model finds information buried deep in very long documents:

| Model | MRCR v2 Score (512K–1M tokens) |
|---|---|
| GPT-5.4 | 36.6% |
| **GPT-5.5** | **74.0%** |

That's more than doubling long-context performance in a single generation. For anyone working with large codebases, legal documents, research papers, or lengthy contracts — this is a practical, immediate upgrade.

### Speed — Same Latency, More Intelligence

Bigger models are usually slower. GPT-5.5 is an exception — it **matches GPT-5.4's per-token latency** in real-world serving while delivering significantly higher quality. It also uses **~40% fewer tokens** to complete the same tasks, which partially offsets the higher API price.

### Computer Use

GPT-5.5 understands intent better, making it faster and more reliable at complex multi-step computer use tasks — navigating GUIs, filling forms, reading screens, and completing workflows with less guidance required.

---

## Benchmarks vs The Competition

| Benchmark | GPT-5.5 | Claude Opus 4.7 | Gemini 3.1 Pro |
|---|---|---|---|
| Terminal-Bench 2.0 (agentic coding) | **82.7%** | 69.4% | 68.5% |
| FrontierMath Tier 4 (advanced math) | **35.4%** | 22.9% | 16.7% |
| GDPval (knowledge work, 44 occupations) | **84.9%** | — | — |
| SWE-Bench Pro (GitHub issue resolution) | 58.6% | **64.3%** | — |
| MCP Atlas (tool use, Scale AI) | 75.3% | **79.1%** | 78.2% |
| BrowseComp (web research) | 84.4% | — | **85.9%** |
| AI Intelligence Index | **#1 — 60 points** | 57 points | 57 points |

GPT-5.5 leads on coding, math, and agentic work. Claude Opus 4.7 still wins on real-world GitHub issue resolution (SWE-Bench Pro) and tool use (MCP Atlas). Gemini 3.1 Pro edges ahead on web research and vision tasks.

### ⚠️ One Weakness — Hallucinations

Despite topping the accuracy benchmark (57% on AA Omniscience), GPT-5.5 has an **86% hallucination rate** — the highest of the three frontier models tested. Claude Opus 4.7 sits at 36% and Gemini 3.1 Pro at 50%. For factual recall tasks where fabricated answers are costly, this is worth keeping in mind.

---

## Pricing

### ChatGPT Subscription (No Change)

| Plan | Monthly Price | GPT-5.5 Access |
|---|---|---|
| Free | $0 | ❌ Not available |
| Plus | $20/month | ✅ GPT-5.5 Thinking |
| Pro | $200/month | ✅ GPT-5.5 Thinking + Pro |
| Business / Enterprise | Custom | ✅ Full access |

### API Pricing (Coming Very Soon)

| Model | Input (per 1M tokens) | Output (per 1M tokens) |
|---|---|---|
| GPT-5.4 | $2.50 | $15.00 |
| **GPT-5.5** | **$5.00** | **$30.00** |
| GPT-5.5 Pro | $30.00 | $180.00 |

The API price **doubled** on paper — but because GPT-5.5 uses ~40% fewer tokens to complete the same tasks, the **net real-world cost increase is closer to 20%**. Batch and Flex modes are available at half the standard rate. Priority processing is 2.5x.

> 💡 **Sam Altman's take on pricing:** Token efficiency gains mean the effective cost increase is much smaller than the sticker suggests — GPT-5.5 completes Codex tasks in fewer passes, meaning cheaper total runs despite the higher per-token rate.

### Codex Bonus for Pro Users
OpenAI is giving **Pro users 2x Codex usage through May 31, 2026** as a launch incentive.

---

## What Hasn't Changed

- Same **1M token context window** on the API (400K in Codex)
- Same text + image input modalities
- Same Responses and Chat Completions endpoints
- API not live yet — coming *"very soon"* pending additional cybersecurity safeguards

---

## The Super App Vision

Beyond the model itself, OpenAI used this launch to move closer to its "super app" ambition — a unified platform combining ChatGPT, Codex, and an AI browser for enterprise customers. Brockman described GPT-5.5 as *"setting the foundation for how we're going to use computers going forward."*

With **900 million weekly active users**, **50 million subscribers**, **9 million paying business users**, and **4 million active Codex users**, OpenAI is betting that GPT-5.5 also puts to rest the recent narrative that Anthropic has overtaken them in the enterprise race.

---

## Who Should Upgrade?

| Use Case | Recommendation |
|---|---|
| Hard coding, agentic tasks, multi-step work | ✅ Upgrade to GPT-5.5 |
| Long document analysis, large codebases | ✅ Upgrade — long-context is dramatically better |
| High-volume summarization, classification | ⏳ Stick with GPT-5.4 or 5.4-mini |
| Correctness-critical legal / financial work | ✅ GPT-5.5 Pro (but watch the hallucination rate) |
| Free tier users | ❌ No access — Plus plan required |

---

## Tips

- **Don't switch everything at once** — route easy, high-volume tasks (classification, summaries) to GPT-5.4-mini; escalate hard ones to GPT-5.5. A smart router saves more than any prompt-level optimization.
- **Use Batch mode** for offline evaluations, backfills, and nightly jobs — it's 50% cheaper than standard API pricing.
- **Watch your reasoning tokens** — the biggest billing surprises on GPT-5.5 come from reasoning-token spend at high effort. Set hard `max_output_tokens` caps on every call.
- **Cache your system prompts** — cached input tokens are billed at a fraction of the standard rate. Anything reused across requests (system prompts, tool schemas, repo context) should be cached.
- **SWE-Bench Pro caveat** — Claude Opus 4.7 still wins on real-world GitHub issue resolution at 64.3% vs 58.6%. If your primary use case is GitHub issue resolution at scale, benchmark both models on your own data before switching.
- **API isn't live yet** — if you need API access right now, GPT-5.4 is still the option. GPT-5.5 API is coming *very soon* per OpenAI.

---

## Quick Reference

| | |
|---|---|
| Released | April 23, 2026 |
| Internal codename | Spud |
| Weeks since GPT-5.4 | 7 weeks |
| Biggest improvement | Long-context reasoning (36.6% → 74.0% on MRCR v2) |
| Best benchmark win | Terminal-Bench 2.0 coding — 82.7% (vs 69.4% Claude) |
| Known weakness | 86% hallucination rate (vs 36% for Claude Opus 4.7) |
| API price vs GPT-5.4 | 2x sticker / ~20% net after token efficiency |
| Token efficiency | ~40% fewer tokens vs GPT-5.4 |
| ChatGPT availability | Plus, Pro, Business, Enterprise — April 23, 2026 |
| API availability | Coming very soon |
| Free tier access | ❌ Not available |
