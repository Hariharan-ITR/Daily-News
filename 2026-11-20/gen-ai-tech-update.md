# Gen AI Tech Update — November 20, 2026

> Daily recap of the latest developments in Generative AI: model releases, tools, frameworks, deployment platforms, and free compute resources.

---

## 1. Latest Model Releases

### Frontier / Closed-Source Models

| Lab | Model | Date | Notes |
|-----|-------|------|-------|
| **Google DeepMind** | Gemini 4 Neon | Nov 18, 2026 | Newest Gemini 4 variant; second tracker confirms Nov 18 release |
| **OpenAI** | GPT-6.2 Astra | Nov 17, 2026 | Latest GPT-6 series addition |
| **OpenAI** | GPT-6.2 Sol | Nov 17, 2026 | Dual release with Astra; ChatGPT Images 2.6 (animated GIF gen) also shipped |
| **Alibaba** | Qwen4-Max | Nov 16, 2026 | Flagship of Qwen4 family |
| **Google DeepMind** | Gemini 4 Hydrogen | Nov 12, 2026 | Also listed on Vertex AI; not yet on public Gemini API changelog |
| **Anthropic** | Claude Fable 5.2 | Nov 9, 2026 | GA; Claude Mythos 5.2 restricted to verified organizations |
| **Mistral AI** | Mistral Large 4 | Nov 5, 2026 | GA with open weights under Mistral Ecosystem Open Weight License |
| **Google DeepMind** | Gemini Omni 1.2 Flash | Nov 5, 2026 | Flash-tier multimodal model update |

> One aggregator tracked **17 new models from 9 providers** in November 2026 alone.

### Open-Weight / Open-Source Models

| Model | License | Notes |
|-------|---------|-------|
| **Mistral Large 4** | Mistral Ecosystem Open Weight License | 1T-param MoE; weights available on Hugging Face from Nov 5 |
| **Rumble-2-Flash** | Open | 0.5B speech model covering 40+ languages; listed on HF blog Nov 18 |
| **LiquidAI LFM3 family** | — | LFM3-1.7B, LFM3-VL-2B, LFM3-Omni-2B trending at start of November |
| **Lightricks LTX-2.5** | — | Text-to-video; most-liked HF model release early November |
| **Baidu Unlimited-OCR-2** | — | High-accuracy OCR model from Baidu; trending on HF early November |
| **Inkling 2 Small** | — | Multimodal model from Thinking Machines Lab; added in Transformers v5.23.0 |

**Sources:**
- [LLM Release Tracker — nhimg.org](https://nhimg.org/llm-release-tracker)
- [AI Model Release Tracker — opper.ai](https://opper.ai/model-releases)
- [LLMs Released in 2026 — llmgateway.io](https://llmgateway.io/timeline/2026)
- [Hugging Face Release Notes — Releasebot](https://releasebot.io/updates/huggingface)
- [HF Trending Models Nov 1 — agents-radar](https://github.com/bianzhilong2-ctrl/agents-radar/issues/1615)

---

## 2. Tools & Frameworks

### Transformers v5.23.0 (Hugging Face)

- Added support for new multimodal, language, and coding models
- Unified model export and sharing workflow introduced
- Notable new model additions: **Inkling 2 Small** (multimodal), **Mistral Large 4** (open weights)

### Agent Frameworks — Current State (November 2026)

| Framework | Version | Last Updated | Highlights |
|-----------|---------|-------------|------------|
| **LangGraph** (LangChain) | 1.2.19 | Oct 30, 2026 | Managed platform renamed **LangSmith Deployment** (GA Jun 2026) |
| **CrewAI** | 1.15.35 | Nov 3, 2026 | **Crew Studio** GA (Jul 2026); Agent Control Plane on AMP platform (Oct 16) |
| **smolagents** (HF) | v1.26.0 | — | Rebranded from Transformers Agents; agents write & execute Python directly |
| **AG2** | — | Active | Continuation of original AutoGen project |
| **Claude Agent SDK (Python)** | 0.2.177 | Nov 3, 2026 | Tracks closely with CrewAI release cadence |

### Hugging Face — Decision Models Hub

- Launched officially on **November 10, 2026** as a dedicated repository for agent-focused and decision-making models
- Targets reinforcement learning, multi-step planning, and tool-use optimized models

### Key Observations

- **smolagents** distinguishes itself by having agents write executable Python code (vs. JSON tool calls), reducing tool call overhead on complex multi-step tasks
- **LangSmith Deployment** (formerly LangGraph Platform) is now the production hosting path for LangGraph agents
- CrewAI's **Agent Control Plane** on AMP provides orchestration visibility for enterprise agentic workloads

**Sources:**
- [Top 9 AI Agent Frameworks — Shakudo](https://www.shakudo.io/blog/top-9-ai-agent-frameworks)
- [LangGraph vs CrewAI vs smolagents — DEV Community](https://dev.to/pooyagolchian/ai-agents-in-2026-langgraph-vs-crewai-vs-smolagents-with-real-benchmarks-on-local-llms-4ma1)
- [HF Decision Models Hub — emergent.sh](https://emergent.sh/news/hugging-face-launches-decision-models-hub-ai)
- [Framework versions — tech-insider.org](https://tech-insider.org/sv/?p=4471)

---

## 3. LLM Deployment & Inference Platforms

### vLLM — v0.32.0 (Oct 18, 2026 — latest stable)

- v0.32.0 is the current stable; v0.22.0 (EAGLE 3.1) listed as pending in the release pipeline
- Recommended by Hugging Face for new production deployments (replacing TGI)
- Key strength: PagedAttention, speculative decoding, high-throughput multi-model serving

### Ollama — v0.40.14 / v0.40.15

- v0.40.14 published November 3; one tracker also reports v0.40.15 as of November 7
- **MLX backend for Apple Silicon** now in preview — accelerated inference on M-series Macs
- OpenAI-compatible endpoints now respect per-model packaged sampling defaults

### Text Generation Inference (TGI) — Maintenance Mode

- Hugging Face archived TGI (last release: v3.3.7, Dec 19, 2025)
- Official recommendation: migrate to **vLLM** or **SGLang** for new production builds
- Existing TGI deployments continue to function

### Other Notable Platforms

| Platform | Notes |
|----------|-------|
| **SGLang** | High-throughput structured generation; now co-recommended by HF alongside vLLM |
| **GPUStack** | Open-source GPU cluster manager for distributed LLM inference; works across GPU types |
| **LLMPanel** | Open-source LLM deployment platform built on vLLM + Ollama; self-hostable |
| **NVIDIA NIM** | Supports Qwen4, Mistral Large 4, and open-weight models on NVIDIA infrastructure |
| **Google Vertex AI** | Gemini 4 Hydrogen listed in preview; broader model catalog expanding |
| **Cloudflare Workers AI** | Edge inference with 10K Neurons/day free tier; daily free allocation confirmed |
| **Amazon Bedrock** | Multi-agent engineering assistants; AWS guidance released this week |
| **Groq** | Fastest commercial inference; free tier with 30 RPM rate limit |
| **Cerebras** | Cloud inference; meaningful daily volumes on permanent free tier |

**Sources:**
- [vLLM vs Ollama vs TGI — tryginger.ai](https://tryginger.ai/blog/vllm-vs-ollama-vs-tgi)
- [vLLM vs Ollama vs SGLang vs TensorRT-LLM — The AI Engineer](https://theaiengineer.substack.com/p/vllm-vs-ollama-vs-sglang-vs-tensorrt)
- [Ollama Wikipedia](https://en.wikipedia.org/wiki/Ollama)
- [VLLM Wikipedia](https://en.wikipedia.org/wiki/VLLM)
- [10 AI Inference Platforms — DigitalOcean](https://www.digitalocean.com/resources/articles/ai-inference-platforms)
- [Open-Source GPU Cluster Manager — DEV Community](https://dev.to/gpustack/introducing-gpustack-an-open-source-gpu-cluster-manager-for-running-llms-5dmj)

---

## 4. Notable ArXiv Papers (Nov 18–20, 2026)

| Paper | arXiv ID | Topic |
|-------|----------|-------|
| **How Generative Models Generate: A Concise Guide to the Generative AI Landscape** | 2611.24728 | Survey of GenAI architectures and generation mechanisms; v1 submitted Nov 18 |
| **Generative AI in Software Testing** | 2611.23349 | Using GenAI to automate and improve software testing workflows |
| **Generative AI-Augmented Requirements Engineering** | cs.AI, Nov 19 | LLM-assisted requirements elicitation and specification |
| **Ambient LLMs: Data-Efficient SFT via Temperature Matching** | — | Prevents overfitting in small post-training datasets using temperature matching |
| **Alignment Myopia in Generative AI** | 2611.06830 | Studies short-sighted alignment failures in generative systems |
| **FrontierPhysics: Evaluating Agents for End-to-End Physics Research** | — | Benchmark for open-ended physics: hypothesis generation, experiment design, interpretation |
| **When Should Agents Remember? Falsification-Gated Self-Evolution** | — | Agents only retain lessons that pass a verification test against new task performance |
| **Paper Reconstruction Evaluation: Hallucination in AI-written Papers** | 2604.01128 | Evaluates factual accuracy and hallucination in AI-generated research |

**Key Research Themes:**
- **Agent memory and self-improvement** — falsification-gated learning ensures quality before retention
- **Alignment failures** — "alignment myopia" characterizes failure modes where models optimize short-term proxies
- **Data efficiency in fine-tuning** — temperature matching reduces fine-tuning data requirements
- **AI for scientific research** — agents benchmarked on real physics research workflows

**Sources:**
- [arXiv cs.AI Current Listings](https://arxiv.org/list/cs.AI/new)
- [ArXiv AI Research Digest 2026-11-18](https://github.com/datnguyenquy94/news-radar/issues/1124)
- [ArXiv AI Research Digest 2026-11-11](https://github.com/datnguyenquy94/news-radar/issues/1043)
- [ArXiv AI Research Digest 2026-11-06](https://github.com/HuggerHustle/ai-radar/issues/162)
- [arXiv:2611.24728](https://arxiv.org/abs/2611.24728)

---

## 5. Free GPU & Compute Resources

### Free Notebook / Training GPUs

| Provider | Free Tier | Limits | Notes |
|----------|-----------|--------|-------|
| **Kaggle** | ~30 GPU hrs/week | 12 hrs/session | T4 GPU; no credit card; P100 retired Sep 15, 2026 |
| **Google Colab** | T4 GPU (dynamic) | 12 hrs/session, 90 min idle | No hard weekly limit; Colab Pro for Education (US) closed to new signups |
| **Lightning AI** | ~15 credits/month (~22 T4 hrs) | 4-hr session limit; 1 active Studio | Phone verification required; some sources cite up to 80 hrs |
| **HuggingFace ZeroGPU** | ~5 min GPU/day | Demo-only (Gradio) | Not for general inference; ideal for quick demos |
| **Paperspace Gradient** | 8 GB M4000 GPU, 5 GB storage | Interruptible | Free plan with basic GPU |

### Free Inference APIs (No GPU Management Needed)

| Provider | Free Tier | Notes |
|----------|-----------|-------|
| **Groq** | Permanent free tier | 30 RPM cap; fastest inference available today |
| **Cerebras** | Permanent free tier | Meaningful daily volumes |
| **GMI Cloud** | Free inference on select OSS models | No credit card required |
| **Cloudflare Workers AI** | 10,000 Neurons/day | Edge inference; daily allocation |
| **HuggingFace Inference Providers** | Small monthly free credit | Covers basic model inference |
| **Modal** | $30/month compute credit | Per-second GPU pricing; serverless functions |

### Pay-As-You-Go Options (Cheapest Paid)

| Platform | Model | Notes |
|----------|-------|-------|
| **Vast.ai** | GPU marketplace | Host-set prices; best for fault-tolerant batch/training jobs |
| **RunPod** | On-demand GPU pods | Spot instances for cost savings |

### Self-Hosting (Free If You Have Hardware)

- **vLLM** — Apache 2.0, production-grade inference server
- **Ollama** — MIT, easy local model management; MLX support for Apple Silicon (preview)
- **GPUStack** — Open-source GPU cluster manager for distributed inference
- **llama.cpp** — CPU/GPU hybrid inference, runs on consumer hardware

**Sources:**
- [Best Free GPU Cloud Options — GMI Cloud](https://www.gmicloud.ai/en/blog/best-free-gpu-cloud-options-for-ai-startups-and-researchers)
- [Awesome Free Compute 2026](https://amitpandeytiktok.github.io/awesome-free-compute-2026/compute.html)
- [Free Cloud GPUs 2026 — gpuperhour.com](https://gpuperhour.com/blog/free-cloud-gpus-and-credits)
- [Google Colab Alternatives 2026 — Spheron](https://www.spheron.network/blog/google-colab-alternatives-8-gpu-clouds-compared-2026/)
- [Free GPU Cloud Trials 2026 — GMI Cloud](https://www.gmicloud.ai/en/blog/best-gpu-cloud-free-trials-for-llm-inference-in-2026)
- [free-gpus — GitHub (loganthorneloe)](https://github.com/loganthorneloe/free-gpus)
- [LLM Inference Platforms — DigitalOcean](https://www.digitalocean.com/resources/articles/ai-inference-platforms)

---

## 6. Methods & Research Trends

- **Falsification-gated agent memory** — Agents only commit a learned lesson to long-term memory if it passes a re-test on new tasks; prevents agents from cementing incorrect generalizations.

- **Temperature matching for SFT** — "Ambient LLMs" technique aligns the temperature of the base model distribution with the supervised fine-tuning distribution, dramatically improving efficiency on small post-training datasets (< 1K examples).

- **Code-writing agents (Python-first)** — smolagents v1.26.0 reinforces the trend of agents generating and executing Python code directly rather than calling predefined JSON tool schemas, yielding more flexible multi-step task completion.

- **Alignment myopia** — Emerging concern that RLHF-tuned models optimize for immediate human approval rather than longer-horizon alignment objectives; arXiv:2611.06830 formalizes this failure mode.

- **Agent evaluation rigor (FrontierPhysics)** — Benchmark requiring agents to form hypotheses, design experiments, run simulations, and interpret results — moving beyond Q&A to end-to-end scientific reasoning evaluation.

- **Decision Models as a category** — Hugging Face's Decision Models Hub formalizes agent-optimized models as a distinct class: separate from general chat/instruction models, targeted at planning, RL, and tool-use tasks.

- **MLX for Apple Silicon inference** — Ollama's preview MLX backend marks mainstream adoption of Apple Silicon as a first-class inference platform, enabling efficient local LLM serving without CUDA.

---

## 7. Quick Summary Snapshot

| Category | Headline |
|----------|---------|
| **Top new model** | Google Gemini 4 Neon (Nov 18) |
| **Top open-weight release** | Mistral Large 4 — open weights on HF (Nov 5) |
| **Framework to watch** | smolagents v1.26.0 — Python-code agents |
| **Inference engine news** | Ollama MLX preview; TGI now archived |
| **Research highlight** | Falsification-gated agent memory (arXiv) |
| **Free GPU pick** | Kaggle (~30 hrs/week, no card required) |
| **Free API pick** | Groq (fastest, permanent free tier) |

---

*Last updated: November 20, 2026 | Sources: HuggingFace Hub, arXiv, official lab blogs, AI aggregators*
