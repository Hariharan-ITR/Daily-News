# Gen AI Tech Update — November 22, 2026

> Daily recap of the latest developments in Generative AI: model releases, tools, frameworks, deployment platforms, free compute resources, and research. Covers approximately the last 24–72 hours (weekend window: Nov 20–22, 2026).

---

## 1. Latest Model Releases

### Frontier / Closed-Source Models (Past Week)

| Lab | Model | Released | Notes |
|-----|-------|----------|-------|
| **Moonshot AI** | Kimi K3.1 Pro Prime | Nov 20, 2026 | Latest in the Kimi K3 series; tops HuggingFace trending |
| **Google DeepMind** | Gemini 4 Neon | Nov 18, 2026 | Positioned between everyday-fast and full frontier tier |
| **OpenAI** | GPT-6.2 Astra | Nov 17, 2026 | Flagship variant; $8/$40 per M in/out tokens |
| **OpenAI** | GPT-6.2 Sol | Nov 17, 2026 | Efficient variant; $2/$10 per M in/out tokens |
| **Alibaba** | Qwen4-Max | Nov 16, 2026 | 2.4T total params, ~71B active/token; API-only, no open weights; 1M-token context |
| **Google DeepMind** | Gemini 4 Hydrogen | Nov 12–13, 2026 | Pre-Neon lighter Gemini 4 model |
| **Anthropic** | Claude Fable 5.2 | Nov 9, 2026 | $8/$40 per M tokens; 20% cheaper and 30% faster than Fable 5.1; improved coding, reasoning, vision |
| **Anthropic** | Claude Mythos 5.2 | Nov 9, 2026 | Same model as Fable 5.2 without safety restrictions; available to vetted life sciences / cybersecurity orgs only |

**Sources:**
- [Weekly Dose #27 — GPT-6.2, Gemini 4 Neon (MLPills)](https://mlpills.substack.com/p/weekly-dose-27-gpt-62-gemini-4-neon)
- [New AI Models — November 2026 LLM Releases (LLM Gateway)](https://llmgateway.io/timeline)
- [Anthropic releases Claude Fable 5.2 and Mythos 5.2 (CNBC)](https://www.cnbc.com/2026/11/09/anthropic-claude-fable-5-2-mythos-5-2.html)
- [Claude Fable 5.2 (Anthropic official)](https://www.anthropic.com/claude/fable)
- [Qwen 4: Qwen4-Max Release, Specs (Geotoolbox)](https://geotoolbox.ai/blog/qwen-4)

---

### Open-Weight / Open-Source Models (HuggingFace Trending — Nov 21, 2026)

| Model | Type | Notes |
|-------|------|-------|
| **Qwen/Qwen3.8-27B** | LLM | #1 on HF; ~20,800 likes, 6.5M downloads |
| **moonshotai/Kimi-K3.1-Pro** | LLM | Trending alongside Kimi K3.1 Pro Prime release |
| **MiniMaxAI/MiniMax-H3** | LLM | Trending hybrid architecture model |
| **google/gemma-4-31B-it** | LLM | Google's open-weight instruction-tuned Gemma 4 |
| **hexgrad/Kokoro-82M** | TTS | Lightweight text-to-speech, widely deployed |
| **facebook/sam3** | Vision | New Segment Anything 3 — video segmentation support |

**Sources:**
- [HuggingFace Trending Models 2026-11-21 (GitHub digest)](https://github.com/datnguyenquy94/news-radar/issues/1159)
- [HuggingFace Trending Models page](https://huggingface.co/models?sort=trending)

---

## 2. Tools & Frameworks

### llama.cpp v1.0.0 — Nov 13, 2026 (First Stable Release)

This is the most significant local inference release in years: llama.cpp finally hits 1.0.0 with a stable, semantically versioned API.

**Key changes:**
- **API stability:** 35 deprecated functions removed; `libllama` and `libggml` now use semantic versioning — breaking changes will bump major version
- **FP8 KV cache:** OCP FP8 support halves KV cache VRAM (1,792 MiB vs 3,584 MiB on f16)
- **MoE expert offloading:** Host-memory expert cache with configurable CPU share for large MoE models
- **New model support:** Kimi-K3.1-Pro, Ripple, xing4_0 architectures; MageVL-Cowork and Kimi-K3.1 vision
- **Server additions:** `/v1/audio/speech` endpoint, redesigned web UI
- **Security fixes:** SSRF, CORS, DNS rebinding vulnerabilities patched; MCP tool cancellation added

**Sources:**
- [llama.cpp v1.0.0 release (GitHub)](https://github.com/ggml-org/llama.cpp/releases/tag/v1.0.0)
- [llama.cpp 1.0 arrives with stable API (Pasquale Pillitteri)](https://pasqualepillitteri.it/en/news/33241/llama-cpp-1-0-stable-api-ggml)
- [llama.cpp v1.0.0 Brings API Stability (TUN)](https://www.tun.com/home/llama-cpp-v1-0-0-brings-api-stability-to-local-ai-ecosystem/)

---

### Ollama — v0.40.16 / v0.40.17-RC (Nov 9–10, 2026)

| Version | Date | Notable Changes |
|---------|------|-----------------|
| **v0.40.16** | Nov 9 | `ollama launch claude` passes through token limits; CUDA 13.5 for Windows ARM |
| **v0.40.17-RC** | Nov 10 | Vulkan GPU memory mapping; concurrent MLX generation on Apple Silicon |

**Sources:**
- [Ollama Release Notes (Releasebot)](https://releasebot.io/updates/ollama)
- [Ollama Release Notes (OllamaHerd)](https://ollamaherd.com/guides/ollama-release-notes)

---

### Agent Frameworks — New Entries

| Framework | Description |
|-----------|-------------|
| **Neurolink** | Single interface across 12+ LLM providers (added to awesome-llm-agents Nov 15) |
| **ProtoLink** | Python agent framework with native A2A (agent-to-agent) communication |
| **Google ADK 2.0** | Google's Agent Development Kit 2.0, tied to Google I/O 2026 announcements |

**Sources:**
- [awesome-llm-agents (GitHub)](https://github.com/kaushikb11/awesome-llm-agents)
- [Top 9 AI Agent Frameworks Nov 2026 (Shakudo)](https://www.shakudo.io/blog/top-9-ai-agent-frameworks)

---

### Unsloth v0.1.920-beta

- AMD NPU support: Q4NX models now run on Ryzen AI hardware
- sd.cpp: CPU-only image and video inference solidly supported

**Source:** [AI Infrastructure Digest 2026-11-20 (GitHub)](https://github.com/duanyytop/agents-radar/issues/4399)

---

## 3. LLM Deployment & Inference Platforms

### Infrastructure State (Nov 20–21, 2026)

| Engine | Status | Best For |
|--------|--------|----------|
| **vLLM** | v0.33.0rc3 live; v0.33.0 stable expected | High-throughput cloud-scale inference |
| **SGLang** | v0.5.23 stable; 1.0 release tracker active (#50045) | Agentic workloads with tools and state |
| **Ollama** | v0.40.17-RC | Local development, cross-platform |
| **llama.cpp** | v1.0.0 stable | Edge, embedded, CPU inference |
| **Unsloth** | v0.1.920-beta | Fine-tuning + fast inference; now on AMD NPUs |

### SGLang 1.0 Milestone in Progress

The [SGLang 1.0 release tracker #50045](https://github.com/sgl-project/sglang) is active. The 1.0 release is focused on API stability and scalability for agentic multi-step workloads.

**Sources:**
- [AI Infrastructure Digest 2026-11-21 (GitHub)](https://github.com/duanyytop/agents-radar/issues/4411)
- [AI Infrastructure Digest 2026-11-20 (GitHub)](https://github.com/duanyytop/agents-radar/issues/4399)
- [SGLang vs vLLM 2026 (Morphllm)](https://www.morphllm.com/comparisons/sglang-vs-vllm)
- [LLM Inference Engines Compared (LeetLLM)](https://leetllm.com/blog/llm-inference-engine-comparison-2026)

---

## 4. Notable arXiv Papers (Nov 13–21, 2026)

| Paper | arXiv ID | Topic |
|-------|----------|-------|
| Large Language Models for AI Infrastructure | 2611.19061 | LLM-assisted accelerator design, kernel engineering, compilation, ops, data mgmt, energy optimization |
| What LLM Agents See and What Users Say | 2611.17639 | When agents should act on assumptions; presupposition theory applied to agents |
| Think with Skills: Pseudocode Planning Before Execution | 2611.02830 | Pseudocode planning pass to improve LLM code-reasoning chains |
| Skill Adapter: Online Routing of LLM Agent Skills | — | Personalizing and routing reusable agent skills; from Nanjing/Jiangnan universities |

> arXiv does not publish new listings on weekends (Nov 21–22 is Sat–Sun), so the most recent listing date is Friday, Nov 19, 2026.

**Sources:**
- [arXiv 2611.19061 — LLMs for AI Infrastructure](https://arxiv.org/abs/2611.19061)
- [arXiv 2611.17639 — What LLM Agents See](https://arxiv.org/abs/2611.17639)
- [arXiv 2611.02830 — Think with Skills](https://arxiv.org/pdf/2611.02830)
- [Skill Adapter paper (CASRAI)](https://casrai.org/news/skill-adapter-online-routing-llm-agent-skills-2026)
- [arXiv cs.CL current listings](https://arxiv.org/list/cs.CL/current)

---

## 5. Free GPU & Compute Resources (Current State)

### Free Notebook / Training GPUs

| Provider | Free Tier | Notes |
|----------|-----------|-------|
| **Kaggle** | ~30 hrs/week | T4/P100; no credit card required |
| **Google Colab** | Dynamic quota (~12 hrs/notebook) | No hard weekly limit published |
| **Lightning AI** | 50 free GPU hrs (interruptible) | Multi-GPU on paid tiers |
| **HuggingFace ZeroGPU** | 5 min GPU/day | Spaces demos and quick tests |

### Free Inference APIs (No GPU Management)

| Provider | Free Tier | Notes |
|----------|-----------|-------|
| **Groq** | Free with rate limits (30 RPM cap) | Fastest inference available |
| **Cerebras** | Permanent free tier | Meaningful daily volumes |
| **GMI Cloud** | Free inference on OSS models | No credit card required |
| **Cloudflare Workers AI** | 10,000 Neurons/day | Edge inference globally |
| **Modal** | $30/month compute credit | Per-second GPU pricing, serverless |
| **India AIKosh** | 4 hrs GPU/day (basic tier) | For Indian researchers/developers |

### New / Changed This Month

- **Lightning AI** updated free tier to 50 GPU hours (up from ~22) — verify on pricing page
- **Colab Pro for Education** closed to new signups
- **Together AI** dropped free credits; $5 minimum prepay now required
- **Oracle Cloud Always Free** remains CPU-only (4 ARM cores, 24 GB RAM) — no GPU

### Startup Credit Programs

| Program | Credits | Status |
|---------|---------|--------|
| **Google for Startups AI** | Up to $350K | Active |
| **Nebius AI Lift** | $150K + $10K inference | Active |
| **NSF ACCESS** | Multi-GPU cluster access | Merit-based, US academic |

**Sources:**
- [Best Free Cloud GPU Tiers 2026 (Modal)](https://modal.com/resources/best-free-cloud-gpu-tiers)
- [Free GPU Cloud Credits: 9 Programs That Changed in 2026 (Spheron)](https://www.spheron.network/blog/free-gpu-cloud-credits-2026/)
- [Free GPU Providers for AI Beginners (Medium)](https://medium.com/data-science-in-your-pocket/free-gpu-providers-for-ai-beginners-9b6bfdc365bf)
- [Where Can I Get Free GPU Cloud Trials in 2026 (GMI Cloud)](https://www.gmicloud.ai/en/blog/where-can-i-get-free-gpu-cloud-trials-in-2026-a-complete-guide)
- [Free Cloud GPUs in 2026: What Works and What Closed (GPUperHour)](https://gpuperhour.com/blog/free-cloud-gpus-and-credits)
- [India AIKosh Notebook Platform](https://aikosh.indiaai.gov.in/home/notebook)

---

## 6. Methods & Research Trends

- **FP8 KV Caching** — llama.cpp v1.0.0 ships OCP FP8 KV cache as standard, cutting VRAM for large context by ~50%. Expect this to propagate to vLLM and SGLang.
- **AMD NPU Inference** — Unsloth's AMD NPU support brings Q4NX model inference to Ryzen AI chips, opening a new class of on-device edge inference beyond Apple Silicon.
- **Pseudocode Planning** — "Think with Skills" (arXiv 2611.02830) demonstrates that inserting a pseudocode planning pass before code execution significantly improves chain-of-thought reasoning in advanced models.
- **A2A Communication** — ProtoLink's native agent-to-agent (A2A) protocol signals a shift toward standardized multi-agent communication at the framework level.
- **Skill Routing in Agents** — The Skill Adapter paper proposes online skill routing: routing agent requests to the most specialized skill based on task embedding, reducing per-task fine-tuning needs.
- **MoE Expert CPU Offloading** — Host-memory expert caching in llama.cpp enables running very large MoE models (like DeepSeek-V4.1) on systems with less VRAM by streaming experts from RAM.
- **LLM-Assisted AI Infrastructure** — A new survey (arXiv 2611.19061) documents how LLMs are being used for accelerator design, kernel engineering, and auto-deployment — meta-use of LLMs to build and optimize the infrastructure they run on.

---

*Last updated: November 22, 2026 | Sources: HuggingFace Hub, arXiv, Anthropic, OpenAI, Google, GitHub release digests, AI aggregators*
