# Gen AI Tech Update — November 15, 2026

> Daily recap of the latest developments in Generative AI: model releases, tools, frameworks, deployment platforms, and free compute resources.
> *Coverage window: last 24–48 hours up to November 15, 2026.*

---

## 1. Latest Model Releases

### Frontier / Closed-Source Models

| Lab | Model | Date | Notes |
|-----|-------|------|-------|
| **Google DeepMind** | Gemini 4 Hydrogen | Nov 12, 2026 | Flagship release; 2.5× faster than Gemini 3.8 Flash at default reasoning; API: $1.50/M input, $7.50/M output tokens; free tier via AI Studio |
| **Google DeepMind** | Gemini 4 Carbon | ~Nov 10, 2026 | Mid-range release preceding Hydrogen |
| **Google DeepMind** | Gemini Decision 1 | ~Nov 11, 2026 | Decision-focused reasoning model |
| **Anthropic** | Claude Fable 5.2 | ~Nov 9, 2026 | Updated Fable series; latest Claude 5 family flagship |
| **Meta** | Muse Ember | ~Nov 9–10, 2026 | New creative/multimodal model from Meta |
| **DeepSeek** | V4.1 Flash 1017 Uncensored | Nov 9, 2026 | Uncensored variant of DeepSeek V4.1 Flash |

### Open-Weight / Open-Source Models

| Model | Released | Notes |
|-------|----------|-------|
| **Moonshot AI / Kimi K3.1 Pro** | Nov 2, 2026 | 2.8T total params, 104B active; largest open-weight release this month on HF |
| **Qwen3.8-27B** | Ongoing | Most-downloaded HF model mid-November (Alibaba); Apache 2.0 |
| **Lightricks / LTX-2.5** | Early Nov | Single-file text-to-video diffusion model; image-to-video support |
| **LiquidAI / LFM3-Omni-2B** | Early Nov | Any-to-any multimodal 2B model trending on HF |
| **DeepSeek V4.1 Flash-1017** | Oct–Nov | MIT-licensed high-performance Flash variant; widely adopted |

> **Sources:** [LLM Gateway Timeline](https://llmgateway.io/timeline) · [Opper Model Releases](https://opper.ai/model-releases) · [LM MarketCap LLM Updates](https://lmmarketcap.com/llm-updates) · [FelloAI Best Models Nov 2026](https://felloai.com/best-ai-models/) · [Google Blog – Gemini 4 Hydrogen](https://blog.google/innovation-and-ai/models-and-research/gemini-models/introducing-gemini-4-hydrogen/) · [VentureBeat – Gemini 4 Hydrogen](https://venturebeat.com/technology/google-launches-gemini-4-hydrogen-a-faster-smarter-pricier-flash-successor) · [HF Trending Nov 11](https://github.com/datnguyenquy94/news-radar/issues/1044)

---

## 2. Tools & Developer Platforms

### Agent Frameworks & Orchestration

| Tool | Status | Highlights |
|------|--------|------------|
| **CrewAI** | v1.15.34 (Nov 1, 2026) | Most recent stable release; widely used multi-agent orchestration |
| **OpenAI Agents SDK** | Pre-1.0 | Visual Agent Builder retiring Nov 30, 2026; Agents SDK remains the successor |
| **Microsoft Agent Framework** | GA since Apr 2026 | Successor to AutoGen + Semantic Kernel; full enterprise support |
| **Google ADK 2.0** | GA (announced Google I/O 2026) | Major update to Google Agent Development Kit |
| **Google Decision API** | Announced Nov 13, 2026 | New API for agentic decision-making workflows; part of Gemini 4 Hydrogen ecosystem |
| **AWS Bedrock AgentCore CLI** | v1.0 stable | Stable CLI for Bedrock agent lifecycle management |

### Infrastructure & Cloud AI

| Platform | Update | Notes |
|----------|--------|-------|
| **Google Cloud** | AI-native Kubernetes stack | Nov 10 announcement: **llm-d 1.0** + **KubeRay** for distributed LLM serving on GKE |
| **Google Cloud** | Agentic HPC tools at SC26 | Showcased at Supercomputing 2026 |
| **Microsoft Azure Foundry** | GA (since Build 2026) | Pay-per-token + provisioned throughput + Managed Compute with scale-to-zero |

> **Sources:** [Shakudo Top 9 AI Agent Frameworks Nov 2026](https://www.shakudo.io/blog/top-9-ai-agent-frameworks) · [AI Agent News Week of Nov 14](https://aiagentstore.ai/ai-agent-news/this-week) · [WireTensors AI Tools Roundup Nov 13](https://wiretensors.ai/news/ai-tools-roundup-2026-11-13/) · [Rio Rundown AI News Nov 14](https://riorundown.substack.com/p/ai-news-nov-14-2026-local-ai-ecosystem)

---

## 3. LLM Inference & Deployment Platforms

### Inference Engines (Self-Hosted)

| Engine | Latest Version | Key Features |
|--------|----------------|--------------|
| **vLLM** | v0.33.0rc3 (Nov 2, 2026) | Most widely adopted; PagedAttention, continuous batching; Blackwell (SM120) support in progress |
| **SGLang** | v0.5.23 (Nov 2, 2026) | Speculative decoding, MoE expert-parallelism; TRT-LLM attention kernels for DeepSeek V4's CSA/HCA layers on SM100/103 |
| **TensorRT-LLM** | v1.3.0 RC (Sep 2026) | PyTorch backend now loads HF checkpoints directly; legacy TensorRT engine backend removed |
| **LMDeploy** | Stable | Lightweight quantized inference; ideal for edge/consumer GPUs |
| **MLC-LLM** | Stable | WebAssembly + mobile inference; compiles models for browsers/iOS/Android |
| **llama.cpp** | Active | CPU + Metal + CUDA; ideal for local Mac/Linux/Windows inference |
| **Ollama** | Active | One-command local model serving; wraps llama.cpp with REST API |

### Managed Inference Platforms (Cloud APIs)

| Provider | Highlights | Pricing Tier |
|----------|------------|--------------|
| **Groq** | Ultra-low latency on custom LPU chips; Llama & Mistral models | Free tier available |
| **Cerebras** | Wafer-scale chip inference; competitive throughput | Free tier available |
| **Together AI** | Wide open-source model catalog; fine-tuning support | Pay-per-token |
| **Fireworks AI** | Low-latency serving; Fireworks Function Calling | Pay-per-token |
| **Baseten** | Custom model deployment; predictable pricing | Pay-per-token |
| **DeepInfra** | Cost-efficient open-model hosting | Pay-per-token |
| **Novita AI** | Budget-friendly GPU inference API | Pay-per-token |
| **Replicate** | Easy model deployment from HF/GitHub | Pay-per-run |
| **Nebius AI** | EU-based cloud GPU inference | Pay-per-token |
| **NVIDIA Dynamo 1.0** | Multi-node disaggregated serving on Kubernetes (Mar 2026) | Enterprise |
| **Google Vertex AI** | Gemini + open model hosting; Agent Engine | Enterprise |
| **Amazon Bedrock** | Multi-model; now with AgentCore v1.0 | Enterprise |
| **Azure AI Foundry** | OpenAI + open models; Managed Compute | Enterprise |

> **Sources:** [KDnuggets 8 LLM Inference Frameworks 2026](https://www.kdnuggets.com/8-llm-inference-frameworks-you-should-try-in-2026) · [Lyzr Best Platforms Nov 2026](https://www.lyzr.ai/blog/best-platforms-for-llm-inference-and-serving) · [Taskade Inference-as-a-Service 2026](https://www.taskade.com/blog/inference-as-a-service) · [Toolchase Best LLM API Platforms](https://toolchase.com/blog/best-llm-api-platforms-2026/) · [SGLang GitHub Releases](https://github.com/sgl-project/sglang/releases) · [Morphllm SGLang vs vLLM 2026](https://www.morphllm.com/comparisons/sglang-vs-vllm) · [Spheron vLLM vs TensorRT-LLM Benchmarks](https://www.spheron.network/blog/vllm-vs-tensorrt-llm-vs-sglang-benchmarks/)

---

## 4. Research Highlights (arXiv / Papers)

| Paper | Date | Key Contribution |
|-------|------|-----------------|
| **Adversarial Risk in the Generative AI Era** (arXiv 2611.14594) | Nov 10, 2026 | Argues adversarial robustness must move beyond small-epsilon threat models in the generative era |
| **Alignment Myopia in Generative AI** (arXiv 2611.06830) | Nov 4, 2026 | Current alignment over-optimizes short-term conversational satisfaction at the cost of long-term safety |
| **UGG: Unified Generative Geometry Model** (arXiv 2611.14440) | ~Nov 11, 2026 | 4D scene geometry, appearance, and dynamics in a single generative model |
| **Generative AI for Medical Vision Training Data** (arXiv 2611.10484) | Nov 7, 2026 | Retrospective study on using general-purpose GenAI to supply synthetic medical imaging data |
| **Agent Memory & Self-Evolution** (Nov 12 digest) | Nov 12, 2026 | Multiple papers on long-term agent memory and adaptive self-improvement; cs.AI Nov 12 batch |

> **Sources:** [arXiv 2611.14594](https://arxiv.org/abs/2611.14594) · [arXiv 2611.06830](https://arxiv.org/abs/2611.06830v1) · [arXiv 2611.10484](https://arxiv.org/abs/2611.10484) · [ArXiv Digest Nov 12](https://github.com/duanyytop/agents-radar/issues/4253) · [ArXiv Multiagent Systems List](https://arxiv.org/list/cs.MA/current)

---

## 5. Free GPU & Compute Resources

| Platform | Free Tier | Best For |
|----------|-----------|---------|
| **Kaggle Notebooks** | ~30 hrs/week (T4 / P100 GPUs) | Training experiments, competitions |
| **Google Colab** | ~15–30 hrs/week (T4 GPU) | Quick prototyping, notebooks |
| **Lightning AI Studios** | ~80 hrs/month on free tier | MLOps, full-stack ML workflows |
| **Modal** | $30/month compute credit; per-second billing | Serverless inference, batch jobs |
| **Hugging Face Spaces** | Free CPU + limited GPU Spaces | Model demos, Gradio/Streamlit apps |
| **Groq Cloud (Free)** | Rate-limited free inference | LLM API testing (Llama, Mistral, Gemma) |
| **Cerebras Cloud** | Free inference API tier | High-throughput LLM inference |
| **Google Cloud** | $300 credit (new users) | Full GCP stack; GKE + Vertex AI |
| **AWS** | Startup + Education credits | Bedrock, SageMaker; apply via programs |
| **Microsoft Azure** | $200 credit (new users) | Azure AI Foundry, OpenAI endpoint |
| **Oracle Cloud** | Always-Free GPU tier (A10) | Persistent free GPU VM |
| **NSF ACCESS** | HPC clusters with GPUs (US researchers) | Large-scale training runs |

> **Sources:** [GMI Cloud Free GPU Guide 2026](https://www.gmicloud.ai/en/blog/where-can-i-get-free-gpu-cloud-trials-in-2026-a-complete-guide) · [Modal Free Tiers](https://modal.com/resources/best-free-cloud-gpu-tiers) · [Alibaba Free GPU Guide](https://electronics.alibaba.com/buyingguides/free-gpu-access-guide-for-developers-students) · [GeeksforGeeks Free GPU Resources](https://www.geeksforgeeks.org/deep-learning/free-gpu-resources-to-train-deep-neural-network/) · [Medium Free GPU Providers](https://medium.com/data-science-in-your-pocket/free-gpu-providers-for-ai-beginners-9b6bfdc365bf)

---

## 6. Quick Digest

- **Model of the Day:** **Gemini 4 Hydrogen** (Google, Nov 12) — fastest Flash-class model from Google yet, 2.5× speed improvement; available via free AI Studio tier.
- **Open-Weight Highlight:** **Kimi K3.1 Pro** (Moonshot AI) — 2.8T parameter open-weight giant; weights available on Hugging Face.
- **Framework Watch:** OpenAI's visual Agent Builder sunsets Nov 30 → migrate to Agents SDK before cutoff.
- **Infra Watch:** Google Cloud's **llm-d 1.0** brings production Kubernetes-native LLM serving to GKE; pairs with KubeRay for distributed inference.
- **Paper Watch:** Adversarial risk & alignment myopia papers both challenge assumptions in current AI safety frameworks.
- **Free Resource Tip:** Oracle Cloud's always-free A10 GPU tier remains one of the best persistent free GPU options for developers.

---

*Compiled on November 15, 2026. All information sourced from public announcements, vendor blogs, arXiv, and Hugging Face. Verify details against official sources before production use.*
