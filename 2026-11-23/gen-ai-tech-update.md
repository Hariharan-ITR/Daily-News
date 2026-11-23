# Gen AI Tech Update — November 23, 2026

> Daily recap of the latest developments in Generative AI: model releases, tools, frameworks, deployment platforms, and free compute resources.

---

## 1. Latest Model Releases

### Frontier / Closed-Source Models

| Lab | Model | Released | Notes |
|-----|-------|----------|-------|
| **OpenAI** | GPT-6.2 Astra | Nov 17, 2026 | Research, writing & coding focused; available in ChatGPT Work, Codex, and API |
| **OpenAI** | GPT-6.2 Sol | Nov 17, 2026 | Efficiency-focused counterpart to Astra; optimized for lower cost per task |
| **OpenAI** | ChatGPT Wallet | Nov 1–15 | In-product wallet feature; launched alongside GPT Image 2.6 (animated GIF generation) |
| **Google DeepMind** | Gemini 4 Neon | Nov 18, 2026 | Flagship release; details sparse — LLM Gateway lists it as a major model |
| **Google DeepMind** | Gemini 4 Hydrogen | Nov 12, 2026 | Paired with model "Carbon" inside a new multi-model Orchestrator |
| **Anthropic** | Claude Fable 5.2 | Nov 9, 2026 | Incremental update to the Fable family |
| **Moonshot AI** | Kimi K3.1 Pro Prime | Nov 20, 2026 | Latest Kimi iteration; K3.1 Pro Prime marks a Prime-tier uplift |
| **Alibaba** | Qwen4-Max | Nov 16, 2026 | Closed-source flagship from Alibaba's Qwen4 generation |
| **MiniMax** | H3 Image | Nov 10, 2026 | Text-to-image model; H3 Video variant also active |

### Open-Weight / Open-Source Models (HuggingFace Trending Nov 21–22, 2026)

| Model | Trend | Notes |
|-------|-------|-------|
| **Qwen3.8-27B** (Alibaba) | #1 by downloads | 14M+ downloads; GGUF quantizations from Unsloth dominate top slots |
| **LTX-2.5** (Lightricks) | Most-liked multimodal | Image-to-video and text-to-video diffusion; successor to LTX series |
| **ZONOS3-Mini** (Zyphra) | Top TTS | Trending text-to-speech model |
| **Inkling-2-Small** (ThinkingMachines) | Consistent trending | Appears across Nov digests; small reasoning-capable model |
| **Edge0-145B-NVFP4** (Edge0) | Large MoE trending | 145B Mixture-of-Experts, NVIDIA FP4 precision |
| **Reson8/Rumble-2-Flash** | ASR | Automatic speech recognition model trending on HF this week |
| **MiniMax H3 family** | Multi-modal | Active across text-to-image and video generation |

**Sources:**
- [LLM Gateway Model Timeline — Nov 2026](https://llmgateway.io/timeline)
- [AI Model Release Tracker (Opper.ai)](https://opper.ai/model-releases)
- [HuggingFace Trending Models 2026-11-22](https://github.com/datnguyenquy94/news-radar/issues/1167)
- [HuggingFace Trending Models 2026-11-21](https://github.com/datnguyenquy94/news-radar/issues/1159)
- [GPT-6.2 Details (Geotoolbox)](https://geotoolbox.ai/blog/gpt-6-2)
- [AI Weekly: GPT-6.2 & Gemini 4 Hydrogen (DEV Community)](https://dev.to/alexmercedcoder/ai-weekly-gpt-62-gemini-4-hydrogen-nvidia-shake-up-11h9)
- [GPT-6.2 vs Gemini 4 Hydrogen (Tom's Guide)](https://www.tomsguide.com/ai/i-tested-gpt-6-2-vs-gemini-4-hydrogen-on-5-tasks-it-wasnt-even-close)

---

## 2. Tools & Frameworks

### Agent Frameworks Update

| Framework | Version / Status | Notes |
|-----------|-----------------|-------|
| **CrewAI** | 1.15.34 (Nov 1) | Most recent stable; role-based multi-agent; ~60K GitHub stars; enterprise platform active |
| **LangChain** | ~1.4.x (est.) | Widest integration catalogue; ~149K GitHub stars; LangSmith as commercial platform |
| **LlamaIndex** | Workflows 1.0 (Jun 22) | Company focus shifted to LlamaParse; Workflows 1.0 is event-driven, async-first |
| **Google ADK** | GA | Google's open-source Agent Development Kit; now listed on allAilists |
| **OpenAI Agents SDK** | Active | Replacement for Agent Builder (see below) |
| **AutoGen** (Microsoft) | Maintenance mode | In maintenance since October 2025; no active feature releases |
| **Pydantic AI** | Active | Strong adoption — 820+ projects import alongside LlamaIndex |

> ⚠️ **Breaking change (Nov 30, 2026):** OpenAI's legacy **Agent Builder** retires on November 30. Code users must migrate to the **Agents SDK**; no-code users move to **Workspace Agents** in ChatGPT.

### Protocol & Standards
- All major frameworks (LangChain, CrewAI, LlamaIndex, Google ADK) now support **Model Context Protocol (MCP)** for standardized tool and context access.

### Claude Integration Highlights (Nov 1–15 roundup)
- Claude gained **Sheets**, **Whiteboards**, and **Meetings** tools (new productivity integrations).

**Sources:**
- [Best AI Agent Frameworks 2026 — Nov Update (BetterClaw)](https://www.betterclaw.io/blog/ai-agent-frameworks)
- [LangChain vs LlamaIndex vs CrewAI 2026 (Tech Insider)](https://tech-insider.org/langchain-vs-llamaindex-vs-crewai-2026/)
- [LangChain Alternatives by PyPI Imports (py-code.org)](https://py-code.org/blog/ai-agent-frameworks-pypi/)
- [New AI Tools Nov 1–15, 2026 (Elite Growth Marketing)](https://www.elitegrowthmarketing.com/blog/new-ai-tools-november-2026)
- [323 New AI Tools — November 2026 (All AI Lists)](https://allailists.com/new-ai-tools/)

---

## 3. LLM Deployment & Inference Platforms

### vLLM — v0.33.0 stable / v0.34.0rc4 pre-release

- **Stable:** v0.33.0 (Nov 2, 2026) — CUDA 13.0 wheels; older driver stacks may need v0.32.0 (Oct 18)
- **Pre-release:** v0.34.0rc0 → rc4 available as of Nov 19; not production-ready
- **Security:** Medium-severity advisory **GHSA-xgh8-qwjh-q853** affects 0.33.0 floor — monitor for patch

### Ollama — v0.40.17 (Nov 10, 2026)

- v0.40.17 added **Inkling-2-Mini** from ThinkingMachines to the model library
- v0.40.16 (Nov 9): `ollama launch claude` now always routes to the user-selected model (Claude Code fix)
- OpenAI-compatible endpoints now respect each model's packaged sampling defaults
- In-progress: per-model prompt cache budgets, CORS hardening, MLX runners, tokenization endpoints

### Other Notable Inference & Deployment Platforms

| Platform | Type | Notes |
|----------|------|-------|
| **NVIDIA NIM** | Managed inference | 91 free endpoint models (LLMs, vision, audio, scientific AI) |
| **Groq** | Inference API | Permanent free tier; 30 RPM cap; fastest raw token throughput |
| **Cerebras** | Inference API | Free tier with meaningful daily volumes |
| **Cloudflare Workers AI** | Edge inference | 10,000 Neurons/day free; resets 00:00 UTC |
| **HuggingFace ZeroGPU / Spaces** | Notebook & demo | ZeroGPU for quick GPU sessions; ideal for model demos |
| **SGLang** | Self-hosted | High-throughput structured generation; active development |
| **Amazon Bedrock AgentCore** | Cloud managed | Multi-agent orchestration on AWS |
| **Oracle Cloud Free Tier** | CPU-only | 4 ARM Ampere cores, 24 GB RAM — **no GPU on free tier** |

**Sources:**
- [Ollama Release Notes](https://ollamaherd.com/guides/ollama-release-notes)
- [Ollama Models List Nov 2026 (Convly)](https://convly.ai/ollama-models-list-2026/)
- [AI Infrastructure Digest 2026-11-08](https://github.com/wxt040218-source/agents-radar/issues/16)
- [vLLM Advisory Watch 2026-11-19](https://github.com/DamienBecherini/ia-on-prem-vault/issues/90)
- [LLM vs vLLM 2026 (Kanerika)](https://kanerika.com/blogs/llm-vs-vllm/)
- [Ollama vs vLLM Pricing 2026 (Shattered)](https://shattered.io/ollama-cloud-pricing-vs-self-hosted-vllm-20-pro-plan-2026/)
- [Best Free GPU Cloud for AI Startups (GMI Cloud)](https://www.gmicloud.ai/en/blog/best-gpu-cloud-free-trials-for-llm-inference-in-2026)
- [The $0 Inference Stack (DEV Community)](https://dev.to/yukichi-emotisa/the-0-inference-stack-running-an-ai-agent-on-free-tier-llm-apis-measured-36ln)

---

## 4. Notable ArXiv Papers (Nov 20–22, 2026)

| Paper | ID (est.) | Topic |
|-------|-----------|-------|
| **Alignment Myopia in Generative AI** | 2611.06830 | Argues alignment tuning optimizes short-horizon conversational satisfaction while ignoring longitudinal harms from sustained human-AI interaction |
| **FrontierPhysics** | — | Benchmark for evaluating AI agents on end-to-end physics research workflows |
| **ReTrace** | — | Distills complex tool-using LLM agents into simpler, planner-free workflows; reduces latency and cost |
| **One Prior, Two Dynamics** | — | Repurposes video diffusion transformers for self-supervised latent action learning in RL |
| **How Generative Models Generate** | 2611.24728 | Concise survey of the generative AI landscape (submitted Nov 18, 2026) |
| **Open-Ended Scientific Discovery with LLM Agents** | — | Framework for competing hypothesis comparison in automated research |
| **Dexterous Robotic Hands in the Foundation Model Era** | — | Survey: foundation models for robot dexterity |

**Sources:**
- [ArXiv AI Research Digest 2026-11-20](https://github.com/datnguyenquy94/news-radar/issues/1145)
- [ArXiv AI Research Digest 2026-11-11](https://github.com/datnguyenquy94/news-radar/issues/1043)
- [ArXiv AI Research Digest 2026-11-06 (HuggerHustle)](https://github.com/HuggerHustle/ai-radar/issues/162)
- [How Generative Models Generate — arXiv:2611.24728](https://arxiv.org/abs/2611.24728)

---

## 5. Free GPU & Compute Resources

### Free Notebook / Training Compute

| Provider | Free Tier | Notes |
|----------|-----------|-------|
| **Google Colab** | Dynamic T4 GPU | Sessions scope-limited; ~12h cap; idle timeouts apply |
| **Kaggle** | ~30 hrs/week | T4 / P100; no credit card required |
| **Lightning AI** | ~22 GPU hrs/month | T4/A10G; interruptible; multi-GPU on paid tiers |
| **HuggingFace Spaces / ZeroGPU** | ~5 min GPU/session | Ideal for demos; ZeroGPU growing with Gradio integration |

### Free Inference APIs (No GPU Management)

| Provider | Free Tier | Limits |
|----------|-----------|--------|
| **Groq** | Permanent free tier | 30 RPM; fastest raw throughput |
| **Cerebras** | Permanent free tier | Meaningful daily quota |
| **NVIDIA NIM** | 91 free endpoints | LLMs, vision, audio, scientific AI |
| **Cloudflare Workers AI** | 10K Neurons/day | Edge inference; resets daily |
| **OpenRouter** | Free-tier models | Rate limits vary; model availability fluctuates |
| **GMI Cloud** | Free OSS model inference | No credit card required |

### Trial Credits (Application or Sign-Up)

| Program | Credits | Notes |
|---------|---------|-------|
| **Oracle Cloud** | $300 for 30 days (new accounts) | No GPU on Always Free tier — paid account needed for GPU shapes |
| **Google for Startups AI** | Up to $350K | Application required |
| **Nebius AI Lift** | $150K + $10K inference | Active program |

> ⚠️ **Oracle Always Free reminder:** Titles claiming "free GPU on Oracle" are misleading — the always-free tier is CPU-only (4 ARM Ampere cores, 24 GB RAM). GPUs require a paid account.

**Sources:**
- [Best Free Cloud GPU Tiers 2026 (GMI Cloud)](https://www.gmicloud.ai/ja/blog/best-gpu-cloud-options-for-ai-startups-and-researchers)
- [Free GPU Providers for AI Beginners (Medium)](https://medium.com/data-science-in-your-pocket/free-gpu-providers-for-ai-beginners-9b6bfdc365bf)
- [10 Free Resources for LLM Engineering (DEV Community)](https://dev.to/ai-ops/10-free-resources-for-llm-engineering-32dk)
- [Oracle Cloud Free Tier for LLMs (EaseCloud)](https://blog.easecloud.io/ai-cloud/launch-oracle-cloud-llms-in/)
- [Free GPU Services Comparison (Murat Karakaya)](https://www.muratkarakaya.net/2025/03/free-gpu-services-for-llm-enthusiasts.html)
- [AI Inference Resources (AER Labs GitHub)](https://github.com/aerlabsAI/ai-inference-resources)

---

## 6. Methods & Research Trends

- **Long-horizon alignment** — The "Alignment Myopia" paper surfaces a systematic gap: RLHF/RLAIF optimizes for single-turn satisfaction but doesn't capture multi-session longitudinal effects. Expect this to shape alignment research priorities in 2027.
- **Agent distillation (ReTrace)** — Compressing full tool-using agent pipelines into planner-free workflows substantially reduces latency and inference cost, making agents practical for latency-sensitive production workloads.
- **Video diffusion for RL** — "One Prior, Two Dynamics" shows video-generation pretraining produces strong action representations, bridging the gap between generative models and RL policy learning.
- **Physics-AI benchmarking** — FrontierPhysics marks a push toward domain-specific agentic benchmarks beyond coding/math, measuring end-to-end research capability.
- **Foundation models for robotics** — Open-weight foundation models (including small vision-language models) are being adapted for dexterous robotic control, reducing dependence on proprietary robot AI stacks.
- **MoE at scale** — Edge0's 145B-NVFP4 and Mistral Large 4 (1T-param A52B MoE) indicate continued industry preference for Mixture-of-Experts over dense models at frontier scale for cost-efficiency.
- **CUDA 13 migration pressure** — vLLM v0.33.0's CUDA 13.0-only wheels signal the ecosystem moving on from older driver stacks; operators on legacy CUDA should plan upgrades.

---

*Last updated: November 23, 2026 | Sources: HuggingFace Hub, arXiv, DEV Community, Tom's Guide, official lab trackers*
