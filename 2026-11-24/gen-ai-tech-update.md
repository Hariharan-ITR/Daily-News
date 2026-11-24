# Gen AI Tech Update — November 24, 2026

> Daily recap of the latest developments in Generative AI: model releases, tools, frameworks, deployment platforms, free compute resources, and research highlights.

---

## 1. Latest Model Releases

### Frontier / Closed-Source Models

| Lab | Model | Status | Notes |
|-----|-------|--------|-------|
| **OpenAI** | GPT-6.2 Astra | GA (Nov 17) | $8 / $40 per 1M tokens input/output |
| **OpenAI** | GPT-6.2 Sol | GA (Nov 17) | $2 / $10 per 1M tokens — lighter, cost-optimized |
| **OpenAI** | GPT-6-Cyber | Limited (Nov 5) | Approved for security teams only |
| **Google** | Gemini 4 Carbon | GA (Nov 10) | Part of Gemini 4 family rollout |
| **Google** | Gemini 4 Hydrogen | GA (Nov 12) | — |
| **Google** | Gemini 4 Neon | GA (Nov 18) | Latest in Gemini 4 series |
| **Google** | Gemini Decision 1 | GA (Nov 11) | Google's first decision-focused model |
| **Google** | Gemini Omni | Announced | Pairs Gemini reasoning with generative media (video output) |
| **Google** | Genie 4 | AI Ultra subscribers | Now open to AI Ultra; AI Pro waitlist open |
| **Anthropic** | Claude Fable 5.2 | GA (Nov 9) | $8 / $40 per 1M tokens |
| **Anthropic** | Claude Mythos 5.2 | GA (Nov 9) | Companion to Fable 5.2 |
| **Microsoft** | MAI Code 2 | GA (Nov 17) | Code-focused model family |
| **Moonshot AI** | Kimi K3.1 Pro Prime | GA (Nov 20) | Successor to Kimi K3.1 Pro |
| **Alibaba** | Qwen 4 Max | GA (Nov 16) | Flagship from Qwen 4 family |
| **Tencent** | Hy4 Flash | GA (Nov 16) | Fast inference variant |
| **Meta** | Muse Ember | GA (Nov 9) | — |
| **ElevenLabs** | Scribe v3 | GA (Nov 10) | Audio transcription/voice model |

> **Note:** 25 total model releases counted across 13 labs as of November 23. Prices and dates sourced from aggregators; verify against official vendor pages before relying on them for billing.

### Open-Weight / Open-Source Models (HuggingFace Trending Nov 21–23)

| Model | Org | Notes |
|-------|-----|-------|
| **Qwen3.8-27B** | Alibaba | Most popular: 20K+ likes, 6.3M+ downloads on HF Hub |
| **SAM 3 (facebook/sam3)** | Meta | Trending — latest Segment Anything Model iteration |
| **unsloth/Qwen3.8-27B-GGUF** | Unsloth | Quantized GGUF; high download count for local inference |
| **Kimi K3.1 Pro** | Moonshot AI | Weights published on HF (arrived Nov 2, two days early) |
| **SarvamMoE** | Sarvam AI | 30B-param MoE; architecture integrated in Transformers v5.24.0 |

**Sources:**
- [New AI Models November 2026 (LLMGateway)](https://llmgateway.io/timeline)
- [AI Model Releases November 2026 (BeevR)](https://beevr.ai/blog/ai-model-releases-november-2026)
- [New AI Models November 2026 (Capital & Compute)](https://capitalandcompute.net/blog/new-ai-models-november-2026/)
- [HuggingFace Trending 2026-11-23 (GitHub Digest)](https://github.com/datnguyenquy94/news-radar/issues/1176)
- [HuggingFace Trending 2026-11-21 (GitHub Digest)](https://github.com/datnguyenquy94/news-radar/issues/1159)
- [AI News Today (DonVitoCodes)](https://www.donvitocodes.com/ai-news)

---

## 2. Hugging Face & Transformers Updates

### Transformers v5.24.0 (~ Nov 21, 2026)

New model integrations added:

| Model | Notes |
|-------|-------|
| **Inkling 2 Mini** | Multimodal (text + image) from Thinking Machines Lab |
| **Apertus 1.5** | General-purpose LLM |
| **Omnilingual ASR** | Multilingual automatic speech recognition |
| **SarvamMoE** | Architecture for Sarvam AI's 30B-param MoE |

### Transformers v5.23.0 (Nov 13, 2026)

Seven new model integrations:

| Model | Notes |
|-------|-------|
| **Inkling 2 Small** | Smaller multimodal variant |
| **JEV** | — |
| **LFM3** | Liquid Foundation Model 3 |
| **LFM3-VL** | Vision-language variant |
| **Dots 3 Note Preview** | — |
| **IQuestCoder** | Code-focused model |
| **InternLM3** | From Shanghai AI Lab |

**Sources:**
- [Hugging Face Transformers 5.23.0 (OpenTools)](https://opentools.ai/news/hugging-face-transformers-5-23-0-model-support-and-upgrade-caveats-for-deployers-and-fine-tuners-c7cf8fc7dd)
- [Hugging Face Release Notes (Releasebot)](https://releasebot.io/updates/huggingface)
- [AI Models Released November 2026 (The AI Engineering)](https://theaiengineering.com/releases/2026/11)

---

## 3. Tools & Frameworks

### AI Agent Frameworks (Current State)

| Framework | Best For |
|-----------|----------|
| **LangChain + LangGraph** | Multi-step pipelines, heavily customized agents |
| **smolagents** (HF) | Code-writing agents; executes Python directly vs. JSON tool calls |
| **AutoGen** (Microsoft) | Multi-agent orchestration |
| **Pydantic AI V2** | Type-safe AI pipelines |
| **DSPy** | Declarative LLM program optimization |
| **Semantic Kernel** | Enterprise integration (Python + Java) |
| **Microsoft Agent Framework** | Enterprise multi-agent systems |

### LLM Inference Frameworks (vLLM, SGLang, etc.)

| Framework | Strength |
|-----------|----------|
| **vLLM** | High-throughput production serving, paged KV attention |
| **SGLang** | Structured generation, RadixAttention for KV sharing |
| **TensorRT-LLM** | NVIDIA-optimized serving |
| **LMDeploy** | Efficient deployment for LLaMA-family models |
| **llama.cpp** | CPU/edge inference, GGUF format |
| **Ollama** | Local model management and serving |
| **MLC-LLM** | Portable inference across hardware backends |

### Observability & Dev Tooling

| Tool | Purpose |
|------|---------|
| **Langfuse** | LLM tracing and observability |
| **Weights & Biases** | Experiment tracking |
| **MLflow** | ML lifecycle management |
| **Helicone** | Cost tracking and visibility |
| **Vercel AI SDK** | Frontend/full-stack AI integrations |
| **LM Studio** | Local model testing GUI |

### Content Authenticity

- **SynthID watermarking** now adopted by **OpenAI**, **Kakao**, and **ElevenLabs** for AI-generated content — Google's watermarking standard gaining cross-industry traction.
- **Apple** opened its Siri AI developer preview to all apps (reported Nov 24, unverified against official channels).

**Sources:**
- [8 LLM Inference Frameworks 2026 (KDnuggets)](https://www.kdnuggets.com/8-llm-inference-frameworks-you-should-try-in-2026)
- [Best LLM Development Frameworks 2026 (RyzLabs)](https://learn.ryzlabs.com/llm-development/best-llm-development-frameworks-for-2026)
- [15 Best LLM Tools 2026 (Guideflow)](https://www.guideflow.com/blog/llm-tools)
- [40 Best LLM Development Tools 2026 (Zfort)](https://www.zfort.com/blog/40-best-llm-development-tools-in-2026)

---

## 4. LLM Deployment & Inference Platforms

### Key Serving Platforms

| Platform | Notes |
|----------|-------|
| **vLLM** | v0.33.0 (Nov 2) — SSD KV-cache offloading, 27 GiB VRAM savings |
| **Ollama** | v0.40.14 — per-model prompt cache budgets, OpenAI-compat defaults |
| **NVIDIA NIM** | Supports GLM-5.2, Qwen 4 Max, and other open-weight models |
| **Hugging Face Inference API** | ZeroGPU + Spaces deployment; Transformers-native |
| **Amazon Bedrock AgentCore** | Multi-agent engineering; AWS guidance released this month |
| **SAP Joule Studio** | No-code/pro-code agents, 70+ models, multistep workflow planning |
| **SGLang** | High-throughput structured generation, RadixAttention |
| **Cloudflare Workers AI** | Edge inference; 10K Neurons/day free tier |
| **Google Vertex AI** | Hosts Gemini 4 family + third-party models |

### Production Inference Platforms (Managed APIs)

| Platform | Strength |
|----------|----------|
| **Groq** | 300+ tok/s on Llama 3.3 70B; fastest free API |
| **Cerebras** | Wafer-scale chip inference; competitive throughput |
| **Together AI** | Broad model catalog; $5 minimum prepay |
| **Fireworks AI** | Optimized serving for open-weight models |
| **Replicate** | Serverless model hosting, pay-per-second |
| **Modal** | Serverless GPUs, $30/month compute credit |

**Sources:**
- [10 AI Inference Platforms 2026 (DigitalOcean)](https://www.digitalocean.com/resources/articles/ai-inference-platforms)
- [Ollama Release Notes (Releasebot)](https://releasebot.io/updates/ollama)
- [Best AI Models November 2026 (FelloAI)](https://felloai.com/best-ai-models/)

---

## 5. Notable ArXiv Research (Nov 2026)

| Paper / Method | Topic | Source |
|----------------|-------|--------|
| **PRKV** — Personalized PageRank KV Eviction | Training-free KV cache eviction using attention-based transition graphs; reduces memory for long-context inference | arXiv cs new listings |
| **RecPIE** — Recommendation with Explanation | Trains predictions + NL explanations jointly using LoRA + RL with accuracy-linked reward | arXiv cs new listings |
| **StrataFlux** | Memory-hierarchy-aware low-bit quantization for LLM inference | ArXiv Digest Nov 6 |
| **ReTrace** | Distills tool-using LLM agents into planner-free workflows; reduces inference cost | ArXiv Digest Nov 11 |
| **Anchor and Check** | Deterministic cross-prompt, cross-model reconciliation for auditable LLM decisions | ArXiv Digest Nov 20 |
| **Agent Tool Use Framework** | Experience storage + retrieval + diagnostic observation for complex tool arguments | arXiv cs new listings |
| **Request-Adaptive Hybrid LLM Inference** | Routing between local and remote LLM depending on request complexity | arXiv:2610.37432 |

**Sources:**
- [arXiv cs.AI Current Listings](https://arxiv.org/list/cs.AI/current)
- [arXiv Computation and Language Current](https://arxiv.org/list/cs.CL/current)
- [ArXiv AI Research Digest 2026-11-06 (GitHub)](https://github.com/datnguyenquy94/news-radar/issues/1001)
- [ArXiv AI Research Digest 2026-11-11 (GitHub)](https://github.com/datnguyenquy94/news-radar/issues/1043)
- [ArXiv AI Research Digest 2026-11-20 (GitHub)](https://github.com/kouweizhu/agents-radar/issues/1046)
- [Request-Adaptive Hybrid LLM Inference (arXiv PDF)](https://arxiv.org/pdf/2610.37432)

---

## 6. Free GPU & Compute Resources

### Free Notebook / Training GPUs

| Provider | Free Tier | Notes |
|----------|-----------|-------|
| **Kaggle** | ~30 hrs/week GPU | No credit card; T4 / P100; best free quota |
| **Google Colab** | Dynamic T4 allocation | No hard weekly limit; throttled during peak |
| **Lightning AI** | ~22 GPU hrs/month (T4/A10G) | Interruptible; multi-GPU on Pro plan |
| **HuggingFace ZeroGPU** | ~5 min GPU/day | Good for Gradio demos and quick tests |

### Free Inference APIs (No GPU Management)

| Provider | Free Tier | Notes |
|----------|-----------|-------|
| **Groq** | Free with rate limits (30 RPM) | Llama 3.3 70B at 300+ tok/s; no credit card |
| **Cerebras** | Permanent free tier | Meaningful daily volumes |
| **GMI Cloud** | Free inference on OSS models | DeepSeek R1 Distill Llama 70B, Llama 3.3 70B Instruct Turbo |
| **Cloudflare Workers AI** | 10,000 Neurons/day | Edge inference, no sign-up required |
| **Google AI Studio** | ~1,500 req/day | Gemini models; no credit card |
| **HuggingFace Inference API** | Limited free tier | Broad model catalog |

### Cloud Startup Credit Programs (Application Required)

| Program | Credits | Notes |
|---------|---------|-------|
| **Google for Startups AI** | Up to $350K | Terms updated Jun 2026 |
| **Nebius AI Lift** | $150K + $10K inference | Active program |
| **AWS Activate** | Varies | Startup program; education credits also available |
| **Microsoft for Startups** | $200 (new account) | Azure credits |
| **Oracle Cloud** | Always-free tier | ARM CPU only (4 cores, 24 GB RAM) — no GPU |

> ⚠️ **Oracle Cloud Always Free:** CPU only, no GPU tier. Together AI dropped its free tier — $5 minimum prepay now required. Verify current limits before committing to any workflow.

**Sources:**
- [Best Free GPU Cloud Options 2026 (GMI Cloud)](https://www.gmicloud.ai/ja/blog/best-free-gpu-cloud-options-for-ai-startups-and-researchers)
- [Best GPU Cloud Free Trials for LLM Inference 2026 (GMI Cloud)](https://www.gmicloud.ai/en/blog/best-gpu-cloud-free-trials-for-llm-inference-in-2026)
- [Free GPU Cloud Credits 2026 (Spheron)](https://www.spheron.network/blog/free-gpu-cloud-credits-2026/)
- [Free GPU Providers for AI Beginners (Medium)](https://medium.com/data-science-in-your-pocket/free-gpu-providers-for-ai-beginners-9b6bfdc365bf)
- [Free GPU Credits for Students and Researchers (Aquanode)](https://www.aquanode.io/blog/free-gpu-credits-for-students-and-researchers)
- [Where to Get Free GPU Cloud Trials 2026 (GMI Cloud)](https://www.gmicloud.ai/blog/where-can-i-get-free-gpu-cloud-trials-in-2026-a-complete-guide)
- [How to Get a Free GPU for AI 2026 (AiFree)](https://aifree.dev/learn/free-gpu-for-ai)

---

## 7. Methods & Research Trends Summary

- **KV Cache Efficiency** — PRKV (PageRank-based eviction) and StrataFlux (low-bit quantization) are the two new hardware-agnostic approaches for reducing inference memory pressure without retraining.
- **Request-Adaptive Hybrid Inference** — Routing queries between local small models and remote large models based on complexity; reduces cost without sacrificing quality.
- **Agent Distillation** — ReTrace converts complex tool-using agents into simpler planner-free workflows, cutting inference cost for production agent deployments.
- **Auditable LLM Decisions** — Anchor and Check enables deterministic, cross-model reconciliation — important for compliance-sensitive enterprise deployments.
- **SynthID Watermarking Adoption** — OpenAI, Kakao, and ElevenLabs joining Google's SynthID standard marks a potential inflection toward industry-wide AI content provenance.
- **Mixture-of-Experts at Scale** — SarvamMoE (30B active from larger total params) and Qwen 4 Max continue the trend of MoE architectures delivering frontier-class performance at reduced serving cost.
- **Multimodal via Transformers** — Transformers v5.24.0 adding Inkling 2 Mini and Omnilingual ASR shows the library keeping pace with multimodal (text+image+audio) model releases.

---

*Last updated: November 24, 2026 | Sources: HuggingFace Hub, arXiv, official lab blogs, AI aggregators*
