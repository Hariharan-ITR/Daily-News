# Gen AI Tech Update — November 27, 2026

> Daily recap of the latest developments in Generative AI: model releases, tools, frameworks, deployment platforms, and free compute resources.

---

## 1. Latest Model Releases

### Frontier / Closed-Source Models

| Lab | Model | Release Date | Notes |
|-----|-------|-------------|-------|
| **Anthropic** | Claude Fable 5.2 | Nov 9, 2026 | New top model, outperforms Opus 5.5 on most benchmarks; $8/$40 per 1M tokens. Companion model *Mythos 5.2* also listed. |
| **OpenAI** | GPT-6.2 Astra | Nov 17, 2026 | Latest flagship from OpenAI |
| **OpenAI** | GPT-6.2 Sol | Nov 17, 2026 | Released alongside Astra; Sol likely a reasoning-optimised variant |
| **Google DeepMind** | Gemini 4 Carbon | Nov 10, 2026 | General-purpose Gemini 4 family member |
| **Google DeepMind** | Gemini 4 Neon | Nov 18, 2026 | Newest Gemini 4 release; Gemini Omni 1.2 Flash also released Nov 5 |
| **Alibaba** | Qwen4-Max | Nov 16, 2026 | Latest flagship from the Qwen4 family |
| **Moonshot AI** | Kimi K3.1 Pro Prime | Nov 20, 2026 | Upgraded tier of Kimi K3.1 Pro |
| **S1** | S1 Fast | Nov 24, 2026 | Most recent model tracked; details limited |

### Open-Weight / Open-Source Models

| Model | License | Notes |
|-------|---------|-------|
| **DeepSeek V4.1 Flash 1017 (HeimdaLLM)** | Custom | Uncensored variant of DeepSeek V4.1 Flash; released Nov 9, 2026 |
| **KRAFTON Raon-1 mini** | Apache 2.0 | MoE architecture; trending #29 on HuggingFace |
| **KandinskyLab ImageSR 2.0** | — | High-quality super-resolution via diffusion; published as Diffusers bundle |
| **Edge0 145B On-Device** | Open | Released Nov 13 — 145B params that run on a **single GPU or Apple Silicon Mac** |
| **Meta Muse Ember** | — | Lightweight model optimised for repeated agent tasks (tool calls, routing); added to Meta API Nov 9 |

### HuggingFace Transformers v5.24.0 (Nov 21, 2026) — New Model Support

- **Inkling 2 Mini** (Thinking Machines Lab) — multimodal, text + image input
- **Apertus 1.5** — updated vision-language model
- **WavTokenizer** — audio tokenisation model
- **Dory** — compact conversational model
- **HY4-VL** — vision-language model
- **Lara Mini** (Translated) — 7.2B total / 0.6B active params MoE multilingual base model

**Sources:**
- [LLM Timeline — November 2026 Releases](https://llmgateway.io/timeline)
- [November 2026 AI Model Releases Overview](https://tecadmin.net/november-2026-ai-model-releases/)
- [AI Models Released in November 2026 (The AI Engineering)](https://theaiengineering.com/releases/2026/11)
- [HuggingFace Transformers 5.24.0 Release](https://freedom.tech/posts/2026-11-21-hugging-face-transformers-5-24-0/)
- [ZeroHour HuggingFace Tracker](https://zerohour.day/entity/vendor/hugging%20face)

---

## 2. Tools & Frameworks

### Developer & Agent Tools

- **LangSmith Tool Gateway (Public Beta, Nov 19, 2026)** — Handles credentials, access policies, and audit traces for agent tool calls; works with MCP-compatible clients including Claude Code and Cursor. Major step for enterprise agent observability.

- **Tether 0.4.0 (Nov 22, 2026)** — Adds a test harness that replays recorded agent runs, letting developers verify which tools were called and whether cost or step limits were respected.

- **Google ADK 2.0** — Agent Development Kit 2.0 announced; major update from Google I/O 2026 thread. Works alongside CrewAI v1.15.34 and LangGraph v1.2.7 in multi-framework stacks.

- **OpenAI Agent Builder retirement (Nov 30, 2026)** — Code-based users directed to Agents SDK (pre-1.0); no-code users directed to Workspace Agents in ChatGPT.

- **Databricks Genie ZeroOps (Public Beta, Nov 19, 2026)** — Monitors data jobs/tables and proposes fixes autonomously, but requires human approval before changing production.

### Platform Feature Launches

| Platform | Feature |
|----------|---------|
| **Claude** (Anthropic) | Added Whiteboards, Sheets, and Meetings integrations |
| **ChatGPT** (OpenAI) | ChatGPT Wallet — agents complete purchases with user approval at checkout |
| **Devin Apps** (Cognition) | Describe an internal business app → Devin builds and hosts it |

### Agent Framework Status (Nov 2026 Comparison)

| Framework | Version | Strength |
|-----------|---------|----------|
| **LangGraph** | v1.2.7 | Complex stateful pipelines |
| **CrewAI** | v1.15.34 | Role-based multi-agent workflows |
| **Google ADK** | 2.0 | Google ecosystem integration |
| **smolagents** (HF) | — | Python-writing agents; lightweight |
| **AutoGen** (Microsoft) | — | Multi-agent orchestration |
| **Pydantic AI** | — | Type-safe, structured LLM pipelines |

**Sources:**
- [Top 9 AI Agent Frameworks Nov 2026 (Shakudo)](https://www.shakudo.io/blog/top-9-ai-agent-frameworks)
- [AI Agents News Week of Nov 26 (AI Agent Store)](https://aiagentstore.ai/ai-agent-news/this-week)
- [New AI Tools This Week Nov 24 (The Tool Nerd)](https://www.thetoolnerd.com/p/new-ai-tools-this-week-nov-24-2026)
- [Best AI Agent Frameworks 2026 (BetterClaw)](https://www.betterclaw.io/blog/ai-agent-frameworks)

---

## 3. LLM Deployment & Inference Platforms

### Cloud Platform Updates

#### Amazon SageMaker (November 2026)
- **NVIDIA Dynamo on HyperPod Inference** — AWS added managed support for NVIDIA Dynamo, an open-source framework for multi-node serving with **disaggregated prefill and decode**.
- Adds KV-cache-aware routing for better GPU memory utilisation.
- Supports in-place rolling model updates, eliminating cold-start downtime.

#### Inference API Landscape

| Platform | Key Models Served | Pricing / Notes |
|----------|------------------|-----------------|
| **Anthropic API** | Fable 5.2, Opus 5.5, Sonnet 5.5 | Fable 5.2 at $8 input / $40 output per 1M tokens |
| **OpenAI API** | GPT-6.2 Astra, GPT-6.2 Sol | — |
| **Groq** | Open-weight models (Llama family) | Lowest latency; free tier available |
| **Cerebras** | Open-weight models | Wafer-scale inference; free tier |
| **DeepInfra** | 100+ models | Opper partnership announced Nov 17 brings DeepInfra's 100+ models to Opper gateway |
| **GMI Cloud** | Llama 3.3 70B, others | No credit card for free inference |
| **NVIDIA NIM** | Qwen4, GLM-5.2, etc. | Production-grade microservices |
| **Cloudflare Workers AI** | Variety | Edge inference; 10K Neurons/day free |
| **Hugging Face ZeroGPU** | Community models | Spaces-based, ~5 min GPU sessions |

### Inference Engine Updates

| Engine | Status / Notes |
|--------|---------------|
| **vLLM** | v0.11.0+ in active development; V1 engine decouples execution loop, C++ lightweight scheduler, continuous pipeline with minimal Python overhead; KV-cache-aware scheduling improvements |
| **SGLang** | v0.5.10; achieves ~16,200 tok/s on Llama 3.1 8B (H100) vs vLLM's ~12,500 in 3rd-party tests |
| **TGI** | In **maintenance mode** (since ~Dec 2025 / Mar 2026); HuggingFace directs new users to vLLM or SGLang |
| **llama.cpp** | Active; runs on CPU + GPU; widely used for local/edge inference |
| **Ollama** | v0.40.x series; popular for local model management |

**Sources:**
- [Amazon SageMaker Inference 2026 Launches Review (AWS)](https://aws.amazon.com/blogs/machine-learning/amazon-sagemaker-inference-2026-launches-in-review-part-2/)
- [LLM API Providers & Pricing November 2026 (MorphLLM)](https://www.morphllm.com/llm-api)
- [Best Open Source LLM API Providers 2026 (DeepInfra)](https://deepinfra.com/blog/best-open-source-llm-api-providers)
- [vLLM vs SGLang vs TGI vs TensorRT-LLM 2026 (PremAI)](https://www.premai.io/blog/llm-inference-servers-compared-vllm-vs-tgi-vs-sglang-vs-triton-2026/)
- [AI Models Released in November 2026 (nocode.mba)](https://www.nocode.mba/ai-release-tracker/2026/11)

---

## 4. Notable ArXiv Papers (Nov 25–27, 2026)

| Paper | Category | Key Contribution |
|-------|----------|-----------------|
| Looped LLMs with Shared Layer Stacks | cs.CL | Reuses a shared transformer block N times per token; trades parameter count for depth at inference |
| "Late Entry" Token Mechanism | cs.CL | New tokens skip early passes of a looped model, joining only final layers; reduces redundant computation |
| Real-Time Reasoning Training for Agents | cs.AI | Training LLMs to reason under strict time constraints for latency-critical agent deployments |
| ROAM-GRPO | cs.LG | Targets reasoning diversity in GRPO-style RL fine-tuning; improves generalisation across problem types |
| Causal Counterfactual Policy Optimisation | cs.LG | Pushes LLMs toward reasoning patterns that transfer across questions via causal counterfactual training |
| CogLoadBench | cs.AI | Benchmark testing how presentation factors (formatting, layout, length) affect LLM reasoning accuracy |
| LLM Triage in Security Detection | cs.AI | Empirical study of RL fine-tuning of LLMs for cybersecurity alert triage |
| GenAI Integration in Agile Transformation | cs.AI | Case study of barriers to GenAI adoption at a Nordic media org (arXiv: 2611.25967) |

**Sources:**
- [arXiv cs.AI Current Listings](https://arxiv.org/list/cs.AI/new)
- [arXiv cs.CL Current Listings](https://arxiv.org/list/cs.CL/new)
- [arXiv cs.LG Current Listings](https://arxiv.org/list/cs.LG/new)
- [ArXiv AI Research Digest 2026-11-20 (agents-radar)](https://github.com/kouweizhu/agents-radar/issues/1046)
- [arXiv:2611.25967 — Barriers to GenAI in Agile Transformation](https://arxiv.org/abs/2611.25967)

---

## 5. Free GPU & Compute Resources

### Free Notebook / Training Compute

| Provider | Free Quota | Notes |
|----------|-----------|-------|
| **Kaggle** | ~30 hrs/week GPU | No credit card; T4/P100 available |
| **Google Colab** | Dynamic GPU sessions (~12 hrs) | Free tier still available; premium for more |
| **Lightning AI** | ~22 GPU hrs/month | T4/A10G; interruptible; multi-GPU on Pro |
| **HuggingFace ZeroGPU** | ~5 min GPU/session | Ideal for demos and quick experiments |

### Free Managed Inference APIs

| Provider | Free Tier | Notes |
|----------|-----------|-------|
| **Groq** | Free with rate limits (30 RPM cap) | Fastest inference; Llama, Mixtral, etc. |
| **Cerebras** | Permanent free tier | Meaningful daily volumes |
| **GMI Cloud** | Free inference (Llama 3.3 70B etc.) | No credit card required |
| **Cloudflare Workers AI** | 10,000 Neurons/day | Edge inference; great for low-latency use |
| **OpenRouter** | Free-tier models available | Aggregates multiple providers; daily limits vary |
| **NVIDIA NIM (community)** | Free access to select models | Via NVIDIA developer program |

### Monthly Compute Credits

| Provider | Credit | Notes |
|----------|--------|-------|
| **Modal** | $30/month | Serverless GPU; per-second billing |
| **DigitalOcean** | $5 for 90 days | New-account credit only (recently reduced) |
| **RunPod, Lambda Labs, fal.ai, Baseten** | Varies | Signup credits; check current terms |

> **New:** Edge0's 145B open model (Nov 13, 2026) enables single-GPU or Apple Silicon Mac inference for a 145B-class model, drastically lowering local compute requirements for large models.

**Sources:**
- [Best GPU Cloud Free Trials for LLM Inference 2026 (GMI Cloud)](https://www.gmicloud.ai/en/blog/best-gpu-cloud-free-trials-for-llm-inference-in-2026)
- [Free & Low-Cost GPU Cloud Providers for AI 2026 (OpsNexus)](https://opsnexusai.com/labs/free-low-cost-gpu-hosting-ai-models/)
- [Where to Get Free GPU Compute for AI/ML in 2026 (PerkStack)](https://perkstack.co/blog/free-gpu-for-ai)
- [Free GPU Providers for AI Beginners (Medium / Data Science in Your Pocket)](https://medium.com/data-science-in-your-pocket/free-gpu-providers-for-ai-beginners-9b6bfdc365bf)
- [Edge0 145B On-Device Model (TechJack Solutions)](https://techjacksolutions.com/ai-brief/edge0-145b-open-source-on-device-inference-single-gpu/)
- [Daily-Updated Free Inference Catalog (GitHub: surendranb/free-inference)](https://github.com/surendranb/free-inference)

---

## 6. Methods & Research Trends

- **Disaggregated Prefill & Decode** — AWS SageMaker's NVIDIA Dynamo integration brings this production-grade technique to managed infra: prefill (processing prompt tokens) and decode (generating output tokens) run on separate GPU pools, improving utilisation and latency.

- **Looped / Recurrent Transformers** — New arXiv work explores reusing a shared transformer block multiple times per token (looped LLMs), trading model size for inference-time depth; "late entry" tokens optimise this further.

- **RL for Reasoning Diversity (ROAM-GRPO)** — GRPO-style reinforcement learning is being refined to generate more diverse reasoning paths, addressing the tendency of RL-trained models to overfit to narrow solution patterns.

- **Causal Counterfactual Policy Optimisation** — A causal approach to RL fine-tuning that selects training signals based on counterfactual reasoning, improving cross-task transfer.

- **Real-Time Constrained Reasoning** — Training paradigm where models learn to reason within hard wall-clock limits, enabling deployment in latency-critical agent environments.

- **On-Device 100B+ Inference** — Edge0's 145B model on a single GPU or Apple Silicon Mac marks a new milestone for local large-model inference without data-centre hardware.

- **MCP-Native Agent Tooling** — LangSmith Tool Gateway's public beta signals that MCP is becoming the standard protocol for agent tool access, with credential management and audit trails built in from the start.

---

*Last updated: November 27, 2026 | Sources: HuggingFace Hub, arXiv, official lab blogs, AI aggregators*
