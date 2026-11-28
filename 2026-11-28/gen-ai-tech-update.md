# Gen AI Tech Update — November 28, 2026

> Daily recap of the latest developments in Generative AI: model releases, tools, frameworks, deployment platforms, and free compute resources.

---

## 1. Latest Model Releases

### Frontier / Closed-Source Models (November 2026)

| Lab | Model | Released | Status | Notes |
|-----|-------|----------|--------|-------|
| **Anthropic** | Claude Fable 5.2 | Nov 9, 2026 | GA | New top-tier model, surpasses Opus 5.5 on nearly all capability benchmarks |
| **Anthropic** | Claude Mythos 5.2 | Nov 9, 2026 | Restricted | Available to verified organizations only |
| **OpenAI** | GPT-6 Cyber | Nov 5, 2026 | Restricted | Limited/approved access |
| **OpenAI** | GPT-6.2 Astra | Nov 17, 2026 | GA | Latest public flagship |
| **OpenAI** | GPT-6.2 Sol | Nov 17, 2026 | GA | Companion release to GPT-6.2 Astra |
| **Google DeepMind** | Gemini 4 Carbon | Nov 10, 2026 | GA (Google Cloud) | General availability on Google Cloud |
| **Google DeepMind** | Gemini 4 Hydrogen | Nov 12, 2026 | GA | Default model in Google Search AI Mode |
| **Google DeepMind** | Gemini 4 Neon | Nov 18, 2026 | GA | Latest Gemini 4 variant |
| **Mistral AI** | Mistral Large 4 | Nov 5, 2026 | GA | Open weights on Hugging Face; massive MoE architecture |
| **Alibaba** | Qwen4-Max | Nov 16, 2026 | GA | Latest in the Qwen4 family |
| **Moonshot AI** | Kimi K3.1 Pro | Nov 20, 2026 | GA | Open weights released; 2.8T parameters (~1.56 TB) on HF |
| **S1** | S1 Fast | Nov 24, 2026 | GA | Latest S1 reasoning model |
| **Thinking Machines** | Inkling 2 Mini | Nov 20, 2026 | GA | Runs on a single RTX PRO 6000; weights on HF |

### Open-Weight / Open-Source Models

| Model | License | Key Features |
|-------|---------|--------------|
| **Mistral Large 4** | Open (non-OSI) | Full weights on HuggingFace; ideal for self-hosting |
| **Kimi K3.1 Pro** | Open | 2.8T parameter model; 1.56 TB of files on HF |
| **Tencent Hy4 Flash** | Open | 224B total / 12B active MoE; 1M context; native multimodal |
| **Inkling 2 Small** | Open | Weights available on HF (since Nov 12) |
| **Inkling 2 Mini** | Open | Runs inference on single RTX PRO 6000 |

**Sources:**
- [November 2026 AI Releases: Claude Fable 5.2, Gemini 4 Carbon & 27 more — ThursdAI](https://thursdai.news/releases/2026-11)
- [November 2026 AI Models: GPT-6.2, Gemini 4 Neon, Fable 5.2](https://tecadmin.net/november-2026-ai-model-releases/)
- [LLM Release Tracker: New AI Models by Date (2026)](https://nhimg.org/llm-release-tracker)
- [LLMs Released in 2026 — AI Model Release Dates](https://llmgateway.io/timeline/2026)

---

## 2. Tools & Frameworks

### Developer & Agentic Tools (November 2026)

- **Claude Code v2.1.331** — Adds Code Mode in terminal sessions on **Amazon Bedrock**, **Microsoft Azure AI Foundry**, and other cloud platforms. Includes `claude doctor` API check and `optionalDependencies` for plugins.

- **Z.ai GLM-5.4** — Z.ai's first "Loop Transformer" model, introducing looped architectural patterns for better performance on reasoning tasks.

- **OpenCode v2.4.0** — Popular open-source coding assistant adds a built-in desktop browser for end-to-end agent capabilities.

- **OpenAI + Cisco Shirudo** — Joint open-source project for a runtime that protects running Linux systems. Addresses security and isolation concerns for agentic AI workloads.

- **Pydantic AI v2.74.0** (Nov 24, 2026) — New release adds `DeprecatedModelWarning` for requests targeting deprecated Anthropic or OpenAI model IDs. Active library for type-safe AI pipelines.

- **Transformers v5.24.0** (Nov 23, 2026) — Hugging Face's core library updated with:
  - Support for new models: Inkling 2 Mini, Apertus 1.5, multilingual Omnilingual ASR
  - Improvements to caching, generation, multimodal workflows, and model serving

- **Beacon** — Open-source tool that lets coding agents reuse lessons from past sessions across Claude Code, Cursor, and Codex. Enables persistent memory/context across coding agent sessions.

- **inferd** (by Incept5) — New Apache 2.0 inference engine built for Macs, designed to run many agents concurrently. Announced live on ThursdAI.

- **Anthropic "Install as App"** — Rolling out Nov 24, 2026. Gives eligible Artifacts their own icon and window on Mac and Windows for a native app-like experience.

- **Devin AI** — Can now build **and host** internal business applications from a natural language description — full-stack generation + deployment in one flow.

- **Rumble-2-Flash** — Open 0.5B speech model supporting 40+ languages. Covered on HF blog (Nov 18–23).

### Agent Frameworks (Current State)

| Framework | Best For |
|-----------|----------|
| **LangGraph** (LangChain) | Complex stateful multi-agent pipelines |
| **smolagents** (HF) | Agents that write and execute Python code |
| **AutoGen** (Microsoft) | Multi-agent orchestration |
| **Pydantic AI v2.74** | Type-safe AI pipelines with strict validation |
| **LlamaIndex Workflows** | RAG and document pipelines |

**Sources:**
- [Agent Tools Today (24 Nov 2026): Launches, Skills, MCP Servers](https://munderdiffl.in/blog/agent-tools-today-2026-11-24/)
- [AI developer tool & SDK news (November 2026)](https://daily.rclabs.in/t/devtools)
- [10 New AI Tools You Need To Try (November 2026)](https://travisnicholson.medium.com/10-new-ai-tools-you-need-to-try-november-2026-1c78fdaed24e)
- [Hugging Face Release Notes - November 2026](https://releasebot.io/updates/huggingface)

---

## 3. LLM Deployment & Inference Platforms

### Inference Engines — Latest Releases

| Engine | Version | Released | Key Updates |
|--------|---------|----------|-------------|
| **Ollama** | 0.40.16 | Nov 9, 2026 | Stable release; $65M raised in Jul 2026; OpenAI-compatible API |
| **vLLM** | 0.32.0 | Oct 18, 2026 | High-throughput inference; leading open framework |
| **llama.cpp** | 0.9.0 | Nov 4, 2026 | 109K+ GitHub stars; CPU-first inference for edge/consumer |
| **inferd** | New | Nov 2026 | Apache 2.0; Mac-native; designed for concurrent multi-agent runs |

### Cloud Deployment Platforms

| Platform | Key Features | Notes |
|----------|-------------|-------|
| **Amazon Bedrock** | Claude Code v2 Code Mode now available | Full managed inference + agents |
| **Microsoft Azure AI Foundry** | Claude Code Code Mode now available | Enterprise-grade deployment |
| **Google Cloud Vertex AI** | Gemini 4 Carbon & Hydrogen GA | Native Google model hosting |
| **Hugging Face Inference API** | ZeroGPU for demos; Spaces for apps | Open model hosting |
| **NVIDIA NIM** | Supports Qwen, GLM, and other open-weights | Microservices-based deployment |
| **SGLang** | High-throughput structured generation | Popular for structured output workloads |
| **Cloudflare Workers AI** | Edge inference | 10K Neurons/day free tier |
| **Groq** | Fastest commercial inference | Free tier with rate limits |

**Sources:**
- [Ollama Wikipedia](https://en.wikipedia.org/wiki/Ollama)
- [VLLM Wikipedia](https://en.wikipedia.org/wiki/VLLM)
- [Llama.cpp Wikipedia](https://en.wikipedia.org/wiki/Llama.cpp)
- [November 2026 AI Releases — ThursdAI](https://thursdai.news/releases/2026-11)

---

## 4. Notable ArXiv Papers (Nov 24–28, 2026)

| Paper | arXiv ID | Topic |
|-------|----------|-------|
| **Transformers with Signatures: Towards Universal In-Context Learning in Path Space** | 2611.31439 | Generalizes in-context learning using path-space (signature) representations |
| **ARLoop: Fully-Open Pre-trained Looped Transformers with Attention Residuals** | 2611.05234 | New looped Transformer architecture with open pre-trained weights |
| **Grammar Sparsity Sets How Transformers Learn Random Languages** | 2611.29692 | Hierarchical grammar learning order governed by sparsity structure |
| **Loopback Transformer: Towards a Unified View of Residual Looped Transformers** | 2611.07226 | Unified framework for looped Transformer variants |
| **Mixture-of-Loops Transformer** | Digest Nov 27 | Combines multiple looping strategies for better compute efficiency |
| **LoopTitan** | Digest Nov 27 | Parameter reuse in Mixture-of-Experts models |
| **Accelerating LLM Inference via Early-Exiting Algorithms** | 2509.05915 | Adaptive token-level early exits to reduce inference FLOPs |
| **LLM Routing Evaluation Benchmark** | Digest Nov 27 | Checks for prompt-specific variation in routing evaluations |
| **Trustworthiness of Distilled Language Models** | Digest Nov 27 | Studies reliability degradation in distillation pipelines |

**Key Themes This Week:**
- **Looped Transformers** — A cluster of papers re-examines parameter reuse and iterative computation inside Transformers, echoing the broader push for more efficient architectures.
- **In-Context Learning Theory** — Formal treatment of what transformers learn from context, extending from sequences to path-space representations.
- **Inference Efficiency** — Early-exit and speculative decoding research continues to mature for production use.

**Sources:**
- [ArXiv AI Research Digest 2026-11-27 — GitHub](https://github.com/HuggerHustle/ai-radar/issues/339)
- [ArXiv cs.LG / cs.CL Current Listings](https://arxiv.org/list/cs.LG/current)
- [arXiv 2611.31439 — Transformers with Signatures](https://arxiv.org/abs/2611.31439)
- [arXiv 2611.05234 — ARLoop](https://arxiv.org/abs/2611.05234)
- [arXiv 2611.29692 — Grammar Sparsity](https://arxiv.org/abs/2611.29692)
- [arXiv 2611.07226 — Loopback Transformer](https://arxiv.org/abs/2611.07226)

---

## 5. Free GPU & Compute Resources

### Free Notebook / Training GPUs

| Provider | Free Tier | GPU Type | Notes |
|----------|-----------|----------|-------|
| **Kaggle** | ~30 hrs/week | T4 / P100 | No credit card; reliable for notebooks |
| **Google Colab** | Dynamic allocation | T4 / L4 | No hard weekly limit published |
| **Lightning AI** | 50–80 GPU-hours total | T4 / A10G | Interruptible; 50 hrs standard, 80 hrs for verified students |
| **Amazon SageMaker Studio Lab** | 4 GPU-hours/day | T4 | No credit card; suitable for coursework |
| **HuggingFace ZeroGPU** | Minutes/day | A100 | Per-Space allocation; best for demos and quick inference |

### Free Inference APIs (No GPU Management)

| Provider | Free Tier | Notes |
|----------|-----------|-------|
| **Groq** | Free with rate limits | 30 RPM; fastest inference commercially available |
| **Cerebras** | Permanent free tier | Meaningful daily token volumes |
| **GMI Cloud** | Free inference on OSS models | No credit card required |
| **Cloudflare Workers AI** | 10,000 Neurons/day | Edge inference; great for low-latency |
| **Modal** | Monthly compute credits | Per-second GPU pricing; serverless |
| **HuggingFace Inference API** | Limited free calls | Good for prototyping with popular models |

### Startup / Research Credit Programs (Application Required)

| Program | Credits | Notes |
|---------|---------|-------|
| **Google for Startups AI** | Up to $350K | Terms updated June 15, 2026 |
| **Nebius AI Lift** | $150K + $10K inference | Active program |
| **NVIDIA Inception** | Access to NIM credits | For AI startups |
| **AWS Activate** | Up to $100K | Includes Bedrock and SageMaker credits |

> **Tip for Nov 2026:** With Mistral Large 4 and Kimi K3.1 Pro now fully open-weight, local inference on consumer hardware (via llama.cpp or Ollama) is a viable alternative to cloud APIs for many workloads — especially with llama.cpp 0.9.0's improved 4-bit quantization.

**Sources:**
- [How to Get Free GPU Compute: A Practical 2026 Guide (Alibaba)](https://electronics.alibaba.com/buyingguides/free-gpu-access-guide-for-developers-students)
- [Free GPU Providers for AI Beginners (Medium)](https://medium.com/data-science-in-your-pocket/free-gpu-providers-for-ai-beginners-9b6bfdc365bf)
- [Free GPU Resources to Train Deep Neural Network — GeeksforGeeks](https://www.geeksforgeeks.org/deep-learning/free-gpu-resources-to-train-deep-neural-network/)
- [How can you get free cloud GPUs for AI training? — DEV Community](https://dev.to/viswaretas_kotra/how-can-you-get-free-cloud-gpus-for-ai-training-522f)

---

## 6. Methods & Research Trends

- **Looped / Recurrent Transformers** — Multiple papers (ARLoop, Mixture-of-Loops, Loopback Transformer) are converging on a new Transformer paradigm that reuses layers across loop iterations, reducing parameter count without sacrificing expressiveness. This is emerging as a credible path to more compute-efficient large models.

- **Multi-Modal Open Models** — Tencent's Hy4 Flash ships with native multimodality at open-weight status (224B total / 12B active MoE, 1M context), bringing serious open multimodal competition to the proprietary space.

- **Loop Transformer Architecture (Z.ai GLM-5.4)** — Z.ai's deployment of a Loop Transformer in a production model (GLM-5.4) validates the looped architecture at scale beyond academic papers.

- **Local Inference Renaissance** — With llama.cpp 0.9.0, Ollama 0.40.16, and new open weights from Mistral, Moonshot, and Thinking Machines, running capable models locally is more practical than ever. Developers are increasingly choosing local inference for privacy-sensitive and cost-sensitive workloads.

- **Agent Interoperability via MCP** — The Model Context Protocol continues gaining traction; tools like Beacon enable memory persistence across Claude Code, Cursor, and Codex, signaling growing convergence on MCP as an interoperability standard for coding agents.

- **Security-First Agentic Runtimes** — OpenAI + Cisco's Shirudo addresses the growing concern about securing agentic processes that execute on live systems.

- **Hybrid Agent Build-and-Host** — Devin AI's new capability to generate and immediately host internal business applications suggests agent platforms are evolving from "code generator" to "full-stack product builder."

---

*Last updated: November 28, 2026 | Sources: HuggingFace Hub, arXiv, ThursdAI, TecAdmin, LLM Gateway, official lab blogs, AI aggregators*
