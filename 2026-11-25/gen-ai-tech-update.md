# Gen AI Tech Update — November 25, 2026

> Daily recap of the latest developments in Generative AI: model releases, tools, frameworks, deployment platforms, and free compute resources.

---

## 1. Latest Model Releases

### Frontier / Closed-Source Models

| Lab | Model | Status | Notes |
|-----|-------|--------|-------|
| **OpenAI** | GPT-6.2 Astra & GPT-6.2 Sol | GA (Nov 17, 2026) | Dual flagship release; Agent Builder platform retires Nov 30 |
| **Anthropic** | Claude Fable 5.2 | GA (Nov 9, 2026) | Latest Claude release; Claude Mythos 5.2 restricted to verified orgs |
| **Google DeepMind** | Gemini 4 Neon | Released Nov 18, 2026 | Newest Gemini 4 variant; Gemini 4 Hydrogen (Nov 12) and Carbon (Nov 10) also on Vertex |
| **Google DeepMind** | Gemini Omni 1.2 Flash | GA (Nov 5, 2026) | Lightweight multimodal variant |
| **Moonshot AI** | Kimi K3.1 Pro Prime | Released Nov 20, 2026 | Follow-up to Kimi K3.1 Pro |
| **Alibaba** | Qwen4-Max | Released Nov 16, 2026 | 2.4T-param MoE model; 1M-token context window |
| **Mistral** | Mistral Large 4 | GA (Nov 5, 2026) | Open-weights release; non-OSI license |

### Open-Weight / Open-Source Models

| Model | Lab | Notes |
|-------|-----|-------|
| **Inkling-2-Mini** | Thinking Machines Lab | Top trending on HF Nov 24; added to Transformers v5.24.0 |
| **Inkling-2-Small** | Thinking Machines Lab | Smaller sibling; added in Transformers v5.23.0 |
| **Apertus 1.5** | Swiss AI Initiative | Multimodal (text+images+audio→text); added to Transformers v5.24.0 |
| **Ripple-65B Preview** | Ricursive | 65B dense Transformer, 12T token pretraining, up to 1Mi context; Apache 2.0 |
| **FLUX-3-Image-Klein** | Black Forest Labs | Image-to-image model; trending on HF Hub |
| **Qwen3.8-27B-pi-adapted** | HF / Harness-Hub | RL LoRA adapter with safe RL methodology; Apache 2.0 |

---

## 2. Frameworks & Tools

### Agent Frameworks

- **eve 1.0 (Vercel)** — GA on Nov 17, 2026. Open-source agent framework; median turn latency dropped from 3.04s to 414ms in this release.
- **OpenAI Agents SDK** — Python 0.24.0 / TypeScript 0.21.0 (pre-1.0); replaces Agent Builder (retiring Nov 30).
- **T3 Code 0.1.7** — MIT-licensed agent control surface; adds parent-thread child subagent approvals (released Nov 4).

### MLOps / Observability

- **LangSmith Tool Gateway (LangChain)** — Public beta Nov 19. Centralized credential management, access policies, and audit traces for all agent tool calls.
- **Databricks Genie ZeroOps** — Public beta Nov 19. Autonomous agent that continuously monitors jobs/tables, diagnoses failures using Unity Catalog metadata and lineage.

### Multi-Agent Platforms

- **Replit Missions** — Coordinates multiple AI agents to plan, build, test, and iterate toward a user-defined goal. Generally available as of late November.

### Transformers Library

- **Transformers v5.24.0** (Nov 21, 2026) — Adds support for Inkling-2-Mini, Apertus 1.5, and multilingual Omnilingual ASR.

---

## 3. Deployment & Inference Platforms

### Cloud Infrastructure

| Platform | Update | Impact |
|----------|--------|--------|
| **AWS SageMaker** | In-place rolling model updates (Nov 2026) | Zero-downtime model swaps; managed NVIDIA Dynamo on HyperPod Inference; KV-cache-aware routing |
| **Amazon ElastiCache (Valkey)** | Distributed KV caching for self-hosted LLMs (Nov 19) | Claims up to 40% cost reduction & 80% lower TTFT |
| **Together AI** | Qwen4-Max on serverless inference | 2.4T-param MoE at $1.05/M input tokens, $3.15/M output tokens; 30% limited-time discount |
| **Opper AI + DeepInfra** | Partnership (Nov 17) | 100+ DeepInfra-hosted models on the Opper gateway |

### Open-Source Inference Engines

- **SGLang Consortium** — Formed Nov 12, 2026 by LMSYS, uniting NVIDIA, AMD, Intel, Google, Meta, Cloudflare, Modal, and RadixArk to advance open-source inference tooling.
- **llama.cpp v1.0.0** — Reported milestone release (verify against official repo); widely used for local CPU/GPU inference.
- **vLLM** — Stable at v0.32.0 (Oct 18, 2026); no new November release, still the dominant serving engine.

---

## 4. Notable Research (arXiv — last 48 hrs)

| Paper | ID | Highlight |
|-------|----|-----------|
| **How Generative Models Generate: A Concise Guide to the GenAI Landscape** | arXiv:2611.24728 | Taxonomizes generation paradigms across modalities (submitted Nov 18) |
| **A Statistical Measure of Trust in Generative AI** | arXiv:2611.30286 | Proposes formal trust metrics for GenAI outputs (submitted Nov 23) |
| **ComplexIF: Multi-Turn, Multi-Constraint Instruction-Following Benchmark** | Nov 24 digest | Challenging benchmark for evaluating complex instruction following in LLMs |
| **RL from LLM-Generated (Suboptimal) Demonstrations** | Nov 24 digest | Explores using imperfect LLM-generated data as RL training signal |
| **CrysLDM: Latent Diffusion Model for Crystal Material Generation** | Nov 24 digest | GenAI applied to materials science / crystal structure prediction |
| **HandiVid: High-Quality Dataset for Hand-Driven Interactive Video Generation** | Nov 24 digest | Dataset + model for controllable video generation via hand poses |

> Source: [ArXiv AI Research Digest 2026-11-24](https://github.com/HuggerHustle/ai-radar/issues/315) · [arxiv.org cs.AI current](https://arxiv.org/list/cs.AI/current)

---

## 5. Free GPU & Compute Resources

### Persistent Free Tiers

| Platform | What You Get | Notes |
|----------|-------------|-------|
| **Kaggle Notebooks** | ~30 GPU hours/week | T4 or P100; best free notebook GPU |
| **Google Colab (free)** | 15–30 GPU hours/week | T4 (16GB); may be pre-empted |
| **Modal Starter** | $30/month compute credits | Serverless; works on GPU workloads |
| **Lightning AI** | ~80 GPU hours intro credits | Interruptible hardware |
| **Groq Cloud** | Permanent free inference tier | Fast LLM inference API (no GPU mgmt) |
| **Cerebras Inference** | Permanent free tier | Ultra-low-latency inference API |
| **Google AI Studio** | Gemini free-tier inference | Generous daily limits |

### One-Time / Program Credits

| Program | Credit | Notes |
|---------|--------|-------|
| **Modal startup program** | Up to $50,000 | Application-based |
| **NVIDIA NIM** | Free inference API | No credits required for many models |
| **Replicate** | $500 (no card) | On signup |
| **NSF ACCESS** | HPC GPU clusters | For qualifying US academic researchers |
| **DigitalOcean** | $5 for 90 days | Reduced from previous offers |

---

## 6. Quick Bytes

- **Anthropic IPO** referenced in November 2026 roundups — reportedly a major milestone.
- **Meta Muse Ember** — Listed among November 2026 AI releases; likely a generative media model from Meta.
- **MiniMax H3-Image** — Listed in the Nov 12 release batch alongside Fable 5.2 and Gemini 4 Carbon.
- **ElevenLabs Scribe v3** — Speech-to-text/transcription model, released Nov 10.

---

## Sources

- [LLM Gateway Timeline — November 2026](https://llmgateway.io/timeline)
- [LLMs Released in 2026 — Model Release Dates](https://llmgateway.io/timeline/2026)
- [ThursdAI — November 2026 Releases](https://thursdai.news/releases/2026-11)
- [AI Agent News Week of Nov 24, 2026](https://aiagentstore.ai/ai-agent-news/this-week)
- [Developer Tools & Platforms Weekly — Nov 23, 2026](https://www.originbrief.app/en/reports/developer-tools-platforms/2026-11-23/weekly)
- [Amazon ElastiCache KV Caching for LLM Inference](https://www.hpcwire.com/aiwire/2026/11/19/amazon-elasticache-now-supports-distributed-kv-caching-for-self-hosted-llm-inference/)
- [Together AI — Qwen4 Max Serverless Inference](https://futurumgroup.com/insights/together-ai-brings-qwen4-max-to-serverless-inference-at-30-off/)
- [ArXiv AI Research Digest 2026-11-24](https://github.com/HuggerHustle/ai-radar/issues/315)
- [arXiv cs.AI — Current Submissions](https://arxiv.org/list/cs.AI/current)
- [HuggingFace Transformers Releases](https://github.com/huggingface/transformers/releases)
- [HuggingFace Trending Models — Nov 24](https://trendoday.com/hugging-face/models/2026/11/24)
- [HF Qwen3.8-27B-pi RL Adapter](https://ashutoshai.com/ai-compass/2026/11/17/hugging-face-qwen3-8-27b-pi-harness-adapter/)
- [Best Free Cloud GPU Tiers 2026 — Modal](https://modal.com/resources/best-free-cloud-gpu-tiers)
- [Free GPU Credits for Inference — 2026 Comparison](https://www.getaiperks.com/en/ai/free-gpu-credits-for-inference)
- [Best Open Source LLM API Providers 2026 — DeepInfra](https://deepinfra.com/blog/best-open-source-llm-api-providers)
- [Amazon SageMaker Inference 2026 Launches](https://aws.amazon.com/blogs/machine-learning/amazon-sagemaker-inference-2026-launches-in-review-part-2/)
- [LMSYS SGLang Consortium Announcement](https://www.lmsys.org/blog/)
