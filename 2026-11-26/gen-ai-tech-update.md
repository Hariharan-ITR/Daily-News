# Gen AI Tech Update — November 26, 2026

> Daily recap of the latest developments in Generative AI: model releases, tools, frameworks, deployment platforms, and free compute resources.

---

## 1. Latest Model Releases

### Frontier / Closed-Source Models

| Lab | Model | Status | Notes |
|-----|-------|--------|-------|
| **OpenAI** | GPT-6.2 Astra | GA | Released Nov 17, 2026 — latest OpenAI flagship |
| **OpenAI** | GPT-6.2 Sol | GA | Released Nov 17 alongside Astra; task-optimized variant |
| **Anthropic** | Claude Fable 5.2 | GA | Released Nov 9, 2026; successor to Fable 5.1 |
| **Anthropic** | Claude Mythos 5.2 | Restricted | Verified organizations only; released Nov 9, 2026 |
| **Google DeepMind** | Gemini 4 Carbon | GA | Released Nov 10, 2026 |
| **Google DeepMind** | Gemini 4 Hydrogen | GA | Released Nov 12, 2026 |
| **Google DeepMind** | Gemini 4 Neon | GA | Released Nov 18; $3/M input tokens, $15/M output tokens, 1M-token context |
| **Alibaba** | Qwen4-Max | GA | Released Nov 16, 2026; available on Together AI serverless |
| **Moonshot AI** | Kimi K3.1 Pro Prime | GA | Released Nov 20, 2026; latest in K3.1 series |
| **S1** | S1 Fast | GA | Released Nov 24, 2026 — newest model tracked |
| **Tencent** | Hy4 | Announced | Announced Nov 4; weights release pending safety hardening |

### Open-Weight / Open-Source Models

| Model | License | Notes |
|-------|---------|-------|
| **Mistral Large 4** | Custom (non-OSI) | Generally available open weights as of Nov 5, 2026; 1T-param MoE |
| **Qwen/Qwen3.8-27B** | Apache 2.0 | Trending on Hugging Face; highest community activity |
| **tencent/Hy4-flash** | — | Trending on Hugging Face this week (Nov 24 digest) |
| **Inkling 2 Small** | — | Multimodal (text + image); added to 🤗 Transformers v5.23.0 |
| **Inkling 2 Mini** | — | Lightweight multimodal; added in Transformers v5.24.0 |
| **Apertus 1.5** | — | Added in Transformers v5.24.0 |
| **Omnilingual ASR** | — | Multilingual speech recognition; Transformers v5.24.0 |
| **Z.ai GLM-5.4** | — | Uses looped transformer architecture; open weights pending safety review |
| **inworld/voice-isolator** | — | Trending on Hugging Face (Nov 24 digest) |

**Sources:**
- [LLM Release Timeline — llmgateway.io](https://llmgateway.io/timeline)
- [November 2026 AI Model Releases — tecadmin.net](https://tecadmin.net/november-2026-ai-model-releases/)
- [AI Model Release Tracker — opper.ai](https://opper.ai/model-releases)
- [HuggingFace Trending Models 2026-11-24](https://github.com/datnguyenquy94/news-radar/issues/1189)
- [Hugging Face Release Notes — releasebot.io](https://releasebot.io/updates/huggingface)

---

## 2. Tools & Frameworks

### Hugging Face Transformers

- **v5.23.0** — Adds support for **Inkling 2 Small** (multimodal: text + image input) from Thinking Machines Lab
- **v5.24.0** — Adds **Inkling 2 Mini**, **Apertus 1.5**, and **Omnilingual ASR** (multilingual)
- HuggingFace blog post: "Welcome Inkling 2 Mini" published alongside v5.24.0

### Agent Frameworks (November 2026 State)

| Framework | Version | Key News |
|-----------|---------|----------|
| **LangChain** | 1.5.0 (Nov 11) | Drops Python 3.10 support; native MCP in `langchain.mcp` namespace (beta, replaces langchain-mcp-adapters) |
| **CrewAI** | 1.15.34 (Nov 1) | Native MCP support — MCP tool servers as agent tools |
| **Google ADK** | 2.14.1 (Nov 12) | Latest stable release |
| **OpenAI Agent Builder** | Retiring Nov 30 | Deprecated; users migrated to OpenAI Agents SDK (pre-1.0) |
| **Microsoft AutoGen** | Maintenance mode | Superseded by **Microsoft Agent Framework** and **AG2** |
| **smolagents (HF)** | Active | Python-writing agents; all 8 major frameworks now ship MCP support |

### Developer Tools

- **llama.cpp** — Stable release `0.9.0` dated November 4, 2026; ggml on track for 1.0 stable API milestone
- **Ollama** — Stable release `0.40.16` dated November 9, 2026

**Sources:**
- [Top 9 AI Agent Frameworks Nov 2026 — shakudo.io](https://www.shakudo.io/blog/top-9-ai-agent-frameworks)
- [AI Agent Frameworks Timeline — nhimg.org](https://nhimg.org/ai-agent-frameworks-timeline)
- [AI Agent Frameworks in 2026: LangGraph vs CrewAI — synthhires.com](https://synthhires.com/journal/ai-agent-frameworks-compared-2026)
- [Talent500 Developer Guide to Agentic AI Frameworks (Nov 25)](https://www.manilatimes.net/2026/11/25/tmt-newswire/globenewswire/talent500-publishes-developer-guide-to-agentic-ai-frameworks/2477455)
- [Hugging Face Release Notes — releasebot.io](https://releasebot.io/updates/huggingface)
- [Ollama Wikipedia](https://en.wikipedia.org/wiki/Ollama)
- [Llama.cpp Wikipedia](https://en.wikipedia.org/wiki/Llama.cpp)

---

## 3. LLM Deployment & Inference Platforms

### AWS: Major Inference Infrastructure Upgrades

- **Amazon SageMaker HyperPod Inference** — Added managed **NVIDIA Dynamo** support:
  - Supports **vLLM**, **SGLang**, and **TensorRT-LLM** backends
  - KV-cache-aware routing: routes each request to the instance holding the longest cached prefix
  - Available in all regions where HyperPod is supported

- **Amazon ElastiCache for Valkey** — Now offers distributed KV caching for self-hosted LLM inference:
  - Up to **40% cost reduction** and **80% lower time-to-first-token**
  - Works with vLLM, SGLang, and TensorRT-LLM via the **LMCache connector**
  - Drop-in configuration change — no rewrite required

**Sources:**
- [Amazon SageMaker Inference 2026 Launches Review — AWS Blog](https://aws.amazon.com/blogs/machine-learning/amazon-sagemaker-inference-2026-launches-in-review-part-2/)
- [Amazon ElastiCache Distributed KV Caching for LLM Inference — HPCwire](https://www.hpcwire.com/aiwire/2026/11/19/amazon-elasticache-now-supports-distributed-kv-caching-for-self-hosted-llm-inference/)

### SGLang Consortium

- Major tech firms formed the **SGLang Consortium** to accelerate open-source inference software across diverse hardware platforms
- No specific product version released at announcement, but signals broad industry adoption of SGLang for multi-vendor inference

**Source:** [AI News Nov 14, 2026 — riorundown.substack.com](https://riorundown.substack.com/p/ai-news-nov-14-2026-local-ai-ecosystem)

### Together AI — Qwen4-Max Serverless Inference

- Qwen4-Max added to Together AI serverless platform
- Introductory pricing (through Nov 22): **$1.05/M input tokens**, **$0.0525/M cached input tokens**, **$3.15/M output tokens** (~30% off standard)

**Source:** [Together AI Brings Qwen4 Max to Serverless — futurumgroup.com](https://futurumgroup.com/insights/together-ai-brings-qwen4-max-to-serverless-inference-at-30-off/)

### Hardware & HPC — SC26 (Nov 16–21, 2026)

- **Intel + SambaNova** demonstrated disaggregated inference on **Intel D270 GPU** and **SambaNova SN50 RDU** at Supercomputing 2026 (SC26)
- **AMD** showcased the new **MI400-series GPUs** at SC26

**Source:** [Intel and SambaNova Showcase at SC26 — casrai.org](https://casrai.org/news/intel-sambanova-d270-sn50-disaggregated-inference-sc26-2026)

### Other Notable Platforms

| Platform | Notes |
|----------|-------|
| **vLLM** | v0.32.0 stable (Oct 18); active development; AWS SageMaker now manages it |
| **Ollama** | v0.40.16 (Nov 9); local deployment for Mac/Linux/Windows |
| **llama.cpp** | v0.9.0 (Nov 4); approaching 1.0 stable ABI milestone |
| **NVIDIA NIM** | Supports GLM-5.4, Qwen4, and other open-weight models |
| **Cloudflare Workers AI** | Edge inference; 10K Neurons/day free tier |
| **HuggingFace Inference API** | ZeroGPU for Spaces, free tier with daily quota |
| **Groq** | Free tier with rate limits; industry-leading inference speed |
| **Cerebras** | Permanent free tier; meaningful daily volume limits |

---

## 4. Notable ArXiv Papers (Nov 24–26, 2026)

| Paper | Topic | Key Insight |
|-------|-------|-------------|
| Masked Diffusion Language Models | Discrete generative modeling | Geometric view of discrete diffusion sampling |
| How Generative Models Generate (arXiv:2611.24728) | Survey — LLM landscape | Concise technical guide to the generative AI landscape; submitted ~Nov 18 |
| Adversarial Risk in the Generative AI Era (arXiv:2611.14594) | Safety / adversarial robustness | Argues small-epsilon ball threat models are insufficient for modern GenAI risks |
| Survival-Model Time-Horizon Curves | ML methodology | Highlights how time-horizon curves can mask within-task hazard dynamics |
| Statistical Methods in Generative AI | Reliability | Proposes statistical frameworks to improve GenAI reliability |

**Sources:**
- [arXiv cs.AI Current Listings](https://arxiv.org/list/cs.AI/current)
- [ArXiv AI Research Digest 2026-11-25](https://github.com/HuggerHustle/ai-radar/issues/321)
- [How Generative Models Generate (arXiv:2611.24728)](https://arxiv.org/abs/2611.24728)
- [Adversarial Risk in GenAI Era (arXiv:2611.14594)](https://arxiv.org/abs/2611.14594)

---

## 5. Free GPU & Compute Resources

### Free Notebook / Training GPUs

| Provider | Free Tier | Notes |
|----------|-----------|-------|
| **Kaggle** | ~30 hrs/week GPU + 20 hrs/week TPU | No credit card required; T4/P100 available |
| **Google Colab** | Dynamic GPU allocation | Access "heavily restricted" for free users; not guaranteed |
| **Lightning AI** | ~22–80 GPU hrs/month | Interruptible T4; range depends on plan tier |
| **HuggingFace ZeroGPU** | ~5 min GPU/day (logged in) | 2 min/day without login; best for Spaces demos |

### Free Inference APIs (No GPU Management)

| Provider | Free Tier | Notes |
|----------|-----------|-------|
| **Groq** | Free with rate limits | 30 RPM cap; fastest inference available publicly |
| **Cerebras** | Permanent free tier | Meaningful daily token volumes |
| **Google Gemini API** | Free tier | Rate-limited; Gemini 4 Carbon available |
| **Cloudflare Workers AI** | 10,000 Neurons/day | Edge inference; great for low-latency use cases |
| **Modal** | $30/month compute credit | Per-second GPU billing; serverless autoscaling |
| **HuggingFace Inference API** | Limited free quota | Access to open-weight models without self-hosting |

### Startup & Researcher Credit Programs

| Program | Credits | Notes |
|---------|---------|-------|
| **Google for Startups AI** | Up to $350K | Terms updated June 15, 2026 |
| **Nebius AI Lift** | $150K + $10K inference | Active program as of Nov 2026 |
| **Aquanode** | Free GPU credits | Student and researcher program; application required |
| **fal.ai / Baseten** | Signup credits | GPU-backed serverless; amount varies |

> ⚠️ **Note:** Free tiers are designed for prototyping, education, and small experiments — not production workloads, sustained inference, or large-model training.

**Sources:**
- [Best Free Cloud GPU Tiers 2026 — modal.com](https://modal.com/resources/best-free-cloud-gpu-tiers)
- [Free GPU for AI Startups — gmicloud.ai](https://www.gmicloud.ai/ja/blog/best-free-gpu-cloud-options-for-ai-startups-and-researchers)
- [Free GPU Credits for Students and Researchers — aquanode.io](https://www.aquanode.io/blog/free-gpu-credits-for-students-and-researchers)
- [How to Get Free GPU for AI 2026 — aifree.dev](https://aifree.dev/learn/free-gpu-for-ai)
- [Free Cloud GPU for AI — synpixcloud.com](https://www.synpixcloud.com/guides/free-cloud-gpu)

---

## 6. Methods & Research Trends

- **Discrete Diffusion for Language** — Masked diffusion language models are advancing as an alternative to autoregressive generation, with new geometric perspectives on the sampling process making them more principled.

- **Disaggregated Inference** — SC26 (Supercomputing 2026) showcased disaggregated prefill/decode as a production trend, with Intel D270 + SambaNova SN50 demonstrating cross-vendor disaggregation. This separates the memory-intensive prefill step from the compute-bound decode step, improving GPU utilization.

- **Distributed KV Caching** — AWS ElastiCache + LMCache connector integration shows distributed KV caching moving from research to production infrastructure, with claimed 80% TTFT improvement and 40% cost savings.

- **Multi-vendor MCP adoption** — All major agent frameworks (LangChain, CrewAI, Google ADK, OpenAI Agents SDK, smolagents, Pydantic AI) now ship MCP support natively, signaling MCP as the de facto inter-agent protocol standard.

- **Looped Transformers** — Z.ai's GLM-5.4 uses a looped transformer architecture (weight-sharing across depth), a departure from standard scaled transformer stacks; a potential path to parameter efficiency at scale.

- **KV-cache-aware routing** — AWS SageMaker HyperPod now routes inference requests to the instance holding the longest prefix cache match, reducing redundant computation on long-context workloads.

- **Multimodal foundation models on HuggingFace** — Inkling 2 (from Thinking Machines Lab) is the week's standout open multimodal model, with both Small and Mini variants merged into Transformers, lowering the barrier for text+image inference.

---

*Last updated: November 26, 2026 | Sources: HuggingFace Hub, arXiv, official lab blogs, AWS Blog, HPCwire, AI aggregators*
