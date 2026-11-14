# Gen AI Daily Tech Update — November 14, 2026

> Covering the latest 24 hours in Generative AI: model releases, tools, frameworks, inference platforms, free GPU resources.

---

## 🤖 New Model Releases

### Anthropic
- **Claude Fable 5.2** (released Nov 9, 2026) — Anthropic's most capable generally available model, built for demanding reasoning and long-horizon agentic tasks. Features a 1M-token context window.
  - Source: [Opper AI Model Release Tracker](https://opper.ai/model-releases) | [CompanyFabric Nov 2026](https://creative-tim.com/blog/ai-agent/companyfabric-november-2026-releases)

### Google DeepMind
- **Gemini 4 Argon** — Ranked #1 on the Vals Index at launch; available at an introductory price until Nov 30, 2026.
- **Gemini 4 Hydrogen** (Nov 12, 2026) — Pricing: $1.50/M input tokens, $7.50/M output tokens.
- **Gemini Decision 1** (Nov 11, 2026) — Decision-focused model variant.
- **Gemini Omni 1.2 Flash** — Listed on LLM Gateway timeline.
  - Source: [LLM Gateway Timeline](https://llmgateway.io/timeline) | [Opper AI](https://opper.ai/model-releases)

### OpenAI
- **GPT-5.5** — Listed on Wikipedia as a recent GPT-family release.
- **GPT Image 2.6** — New image generation model iteration.
  - Source: [LLM Gateway Timeline](https://llmgateway.io/timeline) | [GPT-5.5 Wikipedia](https://en.wikipedia.org/wiki/GPT-5.5)

### Meta
- **Muse Ember 1.0** — New Meta model listed on the LLM Gateway timeline.
  - Source: [LLM Gateway Timeline](https://llmgateway.io/timeline)

### Thinking Machines Lab / Liquid AI
- **Inkling 2 Small** (Nov 12, 2026) — MoE multimodal model accepting text + image inputs; 594B total / 17B active parameters, released under Apache 2.0 after external safety/red-team testing.
- **LFM3** — Third generation of Liquid Foundation Models (Liquid AI); added to Hugging Face `transformers` v5.23.0 on Nov 13.
  - Source: [Transformers GitHub Releases](https://github.com/huggingface/transformers/releases) | [AI Weekly](https://aiweekly.co/ai-news-today)

### ElevenLabs
- **Scribe v3 Live** (Nov 10, 2026) — Latest in ElevenLabs' Scribe family.
  - Source: [LLM Gateway Timeline](https://llmgateway.io/timeline)

---

## 🛠 Frameworks & Tools

### Agent Frameworks
| Framework | Latest Version | Notes |
|-----------|---------------|-------|
| **CrewAI** | v1.15.34 (Nov 1, 2026) | 60K+ GitHub stars; best for role-based multi-agent Python systems |
| **LangGraph** | v1.2.7 | Standalone graph-based runtime; no longer requires other `langchain-*` packages |
| **OpenAI Agents SDK** | Python 0.24.0 / TS 0.21.0 | Still pre-1.0; replaces OpenAI Agent Builder (retiring Nov 30, 2026) |
| **Google ADK** | 2.0 | Announced + updated at Google I/O 2026 |

Sources: [Shakudo Top 9 Agent Frameworks](https://www.shakudo.io/blog/top-9-ai-agent-frameworks) | [BetterClaw AI Agent Frameworks](https://www.betterclaw.io/blog/ai-agent-frameworks) | [AI Agent News Nov 12](https://aiagentstore.ai/ai-agent-news/this-week)

### Coding & Orchestration Tools
- **Claude Code v2.1.323** (Nov 12, 2026) — Added experimental "Code Mode" where Claude writes JavaScript to call its tools.
- **Google Antigravity 2.0** (v2.29.0 as of Nov 3) — Added Orchestrator model option pairing Gemini 4 Hydrogen with Carbon/Argon models.
- **Anthropic Whiteboards & Sheets** — Entered beta Nov 10; **Claude Dashboards** became generally available as **Claude Data**.
  - Sources: [Munderdiffl Agent Tools Nov 13](https://munderdiffl.in/blog/agent-tools-today-2026-11-13/) | [Munderdiffl Nov 11](https://munderdiffl.in/blog/agent-tools-today-2026-11-11/)

### Hugging Face Ecosystem
- **Transformers v5.23.0** (Nov 13, 2026) — Adds Inkling2 and LFM3 architecture support.
- **llama.cpp & ggml v1.0.0** (Nov 13, 2026) — Major 1.0 milestone; supports 150+ model architectures across NVIDIA, AMD, Qualcomm, Arm, IBM, and Intel backends.
  - Sources: [HuggingFace Transformers Releases](https://github.com/huggingface/transformers/releases) | [HuggingFace Posts](https://huggingface.co/posts)

### Inference & Serialization
- **ONNX v1.23.2** (Oct 6, 2026) — Latest stable; cross-framework model exchange standard.
- **Ollama v0.40.14** (Nov 3, 2026) — Local LLM serving runtime.
  - Sources: [ONNX Wikipedia](https://en.wikipedia.org/wiki/Open_Neural_Network_Exchange) | [Ollama Wikipedia](https://en.wikipedia.org/wiki/Ollama)

---

## 🚀 Inference & Deployment Platforms

### vLLM
- **v0.32.0** (Oct 18, 2026) — Latest stable release.
- Recent blog highlights:
  - **Nov 12** — Day-0 support for NVIDIA Vera Rubin hardware; DeepSeek-V4.1-Flash serving on NVL72 with throughput gains.
  - **Nov 11** — Encoder disaggregation for multimodal serving.
  - **Nov 6** — LibTorch stable ABI migration.
  - **Nov 4** — Kinference: open-source inference control plane for vLLM + Kubernetes.
- Sources: [vLLM Blog](https://vllm.ai/blog) | [vLLM Project Site](https://vllm-project.github.io/) | [LeetLLM Comparison](https://leetllm.com/blog/llm-inference-engine-comparison-2026)

### NVIDIA TensorRT-LLM
- **v1.3.0 RC** (candidate as of Nov 2026) — Alongside TensorRT v11.3 and CUTLASS v4.8.0; last stable is v1.2.1 (Apr 2026).
- DFlash speculative decoding reported to deliver **15x+ gains on Blackwell**.
- Rubin and Blackwell serving paths under active development.
  - Sources: [TensorRT-LLM Release Notes](https://nvidia.github.io/TensorRT-LLM/release-notes.html) | [Spheron vLLM vs TensorRT 2026](https://www.spheron.network/blog/vllm-vs-tensorrt-llm-2026/)

### Google Cloud AI Infrastructure
- **AI-native Kubernetes stack** (announced Nov 10) — Includes **llm-d 1.0** and **KubeRay** for inference and stateful agents on GKE.
  - Source: [AI Agent News](https://aiagentstore.ai/ai-agent-news/this-week)

### SGLang
- Competing with vLLM on throughput and stack-level optimizations.
  - Source: [Inference Radar Newsletter](https://www.inference-radar.com/newsletter/2026-W38)

---

## 🆓 Free GPU & AI Resources

| Platform | Offering | Notes |
|----------|----------|-------|
| **Kaggle** | 2× T4 (16 GB each), ~30 hrs/week | P100 retired Sep 15, 2026 |
| **Google Colab** | Free sessions up to 12 hrs | Cuts off early for inactivity |
| **Hugging Face ZeroGPU** | 5 min/day GPU quota | Resets 24h after first use |
| **Modal** | $30/mo compute credit | Per-second GPU pricing, serverless autoscale |
| **Together AI** | $25–$50 signup credit | No card required |
| **Replicate** | $500 signup credit | No card required |
| **NVIDIA NIM** | Free inference API | Available via nim.developer.nvidia.com |
| **Groq** | Free tier LLM inference | High-speed LPU-based serving |
| **Cerebras** | Free tier LLM inference | Wafer-scale chip inference |
| **Lightning AI** | ~80 GPU hrs intro credits | On interruptible hardware |
| **NSF ACCESS** | Free HPC/GPU for US researchers | Application required |

Sources: [GMI Cloud Free GPU Guide](https://www.gmicloud.ai/en/blog/where-can-i-get-free-gpu-cloud-trials-in-2026-a-complete-guide) | [Modal Free GPU Tiers](https://modal.com/resources/best-free-cloud-gpu-tiers) | [AI Perks Free GPU Credits](https://www.getaiperks.com/en/ai/free-gpu-credits-for-inference) | [AIM Multiple Free GPUs](https://aimultiple.com/free-cloud-gpu)

---

## 📄 Notable arXiv Papers (Latest Available: Nov 11, 2026)

| Paper | Key Idea |
|-------|----------|
| **Falsification-Gated Self-Evolution** | LLM agents retain learned lessons only if they pass a verification test on new tasks — reduces hallucinated self-improvement |
| **Evidence-Linked Memory** | Addresses memory-induced degradation in long-context LLM agents |
| **StepBack** | Hybrid self-consistency + verifier-guided resampling cuts inference cost at test time |
| **SetPrint** | Black-box LLM fingerprinting via setwise correspondence of response changes |
| **EngineAgent** | Agentizes on-device LLM inference engines for orchestration |
| **Policy Optimization in Post-Training** | Coverage collapse and reference resets in RLHF fine-tuning |

Sources: [arXiv cs.AI New](https://arxiv.org/list/cs.AI/new) | [arXiv cs.CL Current](https://arxiv.org/list/cs.CL/current) | [ArXiv Digest Nov 11 — GitHub](https://github.com/datnguyenquy94/news-radar/issues/1054)

---

## 📌 Trending on Hugging Face (Hub)

Recent model uploads noted on the Hub (exact dates unconfirmed):
- `MiniMax-H3-Image` — MiniMax image generation model
- `Qwen3.8-27B` — Qwen 3.8 series, 27B variant
- `Zyphra/ZONOS3-Mini` — Mini version of Zyphra's ZONOS3

Source: [Hugging Face Models](https://huggingface.co/models)

---

*Compiled on 2026-11-14 from HuggingFace, arXiv, official vendor blogs, and aggregator sources. Verify version numbers and pricing directly with vendors before relying on them in production.*
