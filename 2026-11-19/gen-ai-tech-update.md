# Gen AI Tech Update — November 19, 2026

> Daily recap of the latest developments in Generative AI: model releases, tools, frameworks, deployment platforms, and free compute resources.

---

## 1. Latest Model Releases

### Frontier / Closed-Source Models

| Lab | Model | Released | Notes |
|-----|-------|----------|-------|
| **OpenAI** | GPT-6.2 Astra | Nov 17, 2026 | Flagship; $8/$40 per million tokens (input/output) |
| **OpenAI** | GPT-6.2 Sol | Nov 17, 2026 | Leaner variant; $2/$10 per million tokens |
| **OpenAI** | ChatGPT Images 2.6 | Nov 17, 2026 | Now generates animated GIFs |
| **Anthropic** | Claude Fable 5.2 | Nov 9, 2026 | Updated Fable with improved reasoning; $8/$40 per million tokens |
| **Anthropic** | Claude Mythos 5.2 | Nov 9, 2026 | New creative/narrative-focused variant |
| **Google** | Gemini 4 Hydrogen | Nov 12, 2026 | Latest Gemini 4 series model |
| **Google** | Gemini 4 Carbon | Nov 10, 2026 | Generally available in the API |
| **Google** | Gemini Decision 1 | Nov 11, 2026 | Google's first dedicated decision/reasoning model |
| **Alibaba** | Qwen4-Max | Nov 16, 2026 | 1M context window; $1.50/$4.50 per million tokens |
| **Tencent** | Hy4-Flash | Nov 16, 2026 | Low-cost flash-tier model |
| **Meta** | Muse Ember | Nov 9, 2026 | New creative/multimodal model from Meta |
| **ElevenLabs** | Scribe v3 & Scribe v3 Live | Nov 10, 2026 | Advanced speech-to-text and real-time transcription |

### Open-Weight / Open-Source Models

| Model | License | Notes |
|-------|---------|-------|
| **Mistral Large 4** | Custom | Available with open weights on Hugging Face; 1T+ param MoE |
| **MiniMax H3-Image** | Community | Open-weight image generation model from MiniMax |
| **NVIDIA GR00T 2** | Open | Nvidia's robot foundation model, now on Hugging Face |
| **Rumble-2-Flash** | Open | Small speech model covering 40+ languages (Nov 18) |
| **ZONOS3-Mini** | Open | Open-source voice cloning and TTS model (Nov 18) |
| **llama.cpp v1.0.0** | MIT | Major milestone release for local AI inference |
| **thinkingmachines/Inkling-2-Small** | — | New small model on HF hub |

---

## 2. Platforms & Infrastructure

### Commercial Cloud Inference Platforms

| Platform | Update | Details |
|----------|--------|---------|
| **Microsoft Azure AI Foundry** | Ignite 2026 | New MAI Code 2 coding models + MAI Cyber 2 Flash security model; expanded Foundry Tools ecosystem |
| **Microsoft Azure** | Nov 17 | MAI Image 2.7 image model, MAI Realtime 1 speech model, Dragon Copilot Transcribe |
| **Microsoft IQ** | Nov 17 | New product that gathers organizational knowledge for enterprise AI |
| **Perplexity Orchestrator** | Nov 17 | Single API for multi-model inference with automatic failover across providers |
| **Google AI Studio** | Ongoing | Still offering ~1,000–1,500 free requests/day on Gemini models |
| **Groq** | Ongoing | Ultra-fast LPU inference; ~1,000–1,500 free requests/day |
| **Cloudflare Workers AI** | Ongoing | 10,000 free Neurons/day for edge AI inference |

### Self-Hosted / Local Inference Tools

| Tool | Status | Best For |
|------|--------|---------|
| **vLLM** | Production standard | High-throughput multi-GPU production serving; PagedAttention + continuous batching |
| **Ollama** | v1.0+ (wraps llama.cpp) | Local development; 1-command server; excellent Apple Silicon support |
| **SGLang** | Competitive with vLLM | High-concurrency workloads; benchmarks competitive with vLLM on Qwen3.8-27B |
| **llama.cpp v1.0.0** | Major milestone | CPU + Metal + CUDA; backbone of Ollama; universal compatibility |
| **LM Studio** | Active | GUI for local model management; ideal for evaluating models before deploying |

> **Recommended tiered workflow:** Evaluate with LM Studio → Develop with Ollama → Deploy with vLLM

---

## 3. Tools, Frameworks & Agent Platforms

### Agent Frameworks

| Framework | Version / Status | Notes |
|-----------|-----------------|-------|
| **Microsoft Agent Framework** | v1.0 GA (Apr 2026) | Production-grade; integrated into Agent 365 |
| **Google ADK** | 2.0 (Google I/O 2026) | Major update to Android/Google AI Dev Kit for agents |
| **Agent 365** | Expanded (Ignite 2026) | Governs AI agents across Microsoft 365, Azure, Windows; hundreds of new connectors |
| **Azure AI Search (Agentic Retrieval)** | Preview | Query planning capabilities for multi-step retrieval |
| **Microsoft Fabric Data Agent** | GA | End-to-end data analytics agent now generally available |

### RAG & Retrieval Methods (Latest Research)

- **RAG-FGO:** Dynamic optimization of query-rewriting agents for generative RAG (arxiv, Nov 17)
- **Trustworthy RAG:** Evaluation agent for detecting misinformation and knowledge poisoning in GenAI systems (Nov 10)
- **HiVe-Mem:** Hierarchical vector memory for multimodal agents (Nov 11 digest)
- **Agentic Search Stack:** Amazon Science research showing agentic keyword search achieves 94.5% of RAG faithfulness with zero vector store (presented at AAAI 2026)
- **Conformal Factuality in Agentic RAG:** New evaluation framework ensuring statistically certified factual outputs

### Developer Tools

| Tool | Notes |
|------|-------|
| **Strike Graph Integration AI** | Agentic compliance tool connecting to any software API for GRC evidence (Nov 18) |
| **Apple Core AI** | New on-device framework for running models natively in Apple OS ecosystem |

---

## 4. Research Highlights (arXiv — Nov 17–18, 2026)

| Paper | Topic |
|-------|-------|
| **AutoScaffold** | AI-guided scaffolding for reinforcement learning of language models |
| **Falsification-Gated Self-Evolution for LLM Agents** | Agents that use self-falsification to improve reasoning |
| **Ambient LLMs: Data-Efficient SFT via Temperature Matching** | Parameter-efficient fine-tuning approach |
| **Federated Architecture for Cross-Org Agent Identity** | Accountability and verification for multi-org agent deployments |
| **Beyond the Text: Verifying Agent-Written Papers Against Artifacts** | Hallucination detection in research contexts |
| **Isolation Is Not Confidentiality** | Security boundaries of geometric access control in RAG systems |

> Full listings: [cs.AI/current](https://arxiv.org/list/cs.AI/current) · [cs.LG/current](https://arxiv.org/list/cs.LG/current)

---

## 5. Free GPU & Compute Resources

### Free Inference APIs

| Provider | Free Tier | Notes |
|----------|-----------|-------|
| **Google AI Studio** | ~1,000–1,500 req/day | Access to Gemini models |
| **Groq** | ~1,000–1,500 req/day | Fastest LPU inference for open models |
| **Cloudflare Workers AI** | 10,000 Neurons/day | Edge inference; great for serverless AI apps |
| **Hugging Face Inference API** | Removed Oct 2026 | Free monthly credits discontinued; must purchase or use PRO ($9/mo for $2 credit + 25 min ZeroGPU) |

> **Important:** Hugging Face removed free inference credits in October 2026. PRO plan ($9/mo) includes $2/month credits and 25 min/day of ZeroGPU (NVIDIA RTX PRO 6000 Blackwell or H200).

### Free GPU Notebooks / Platforms

| Platform | Allowance | GPU |
|----------|-----------|-----|
| **Kaggle Notebooks** | ~30 GPU hours/week | NVIDIA P100 or T4 |
| **Google Colab (Free)** | Daily limit (variable) | T4 or L4 (limited hours) |
| **Lightning AI** | 15 credits/month (~22 hrs) | T4 equivalent |
| **Hugging Face ZeroGPU (PRO)** | 25 min/day | RTX PRO 6000 Blackwell |

### Free GPU Cloud Credits Programs

- **Google Cloud:** $300 free credits for new accounts (AI-eligible)
- **Azure:** $200 free credits for new accounts + AI services free tier
- **Spheron Network:** Decentralized GPU marketplace with startup credit programs
- **Aquanode:** Free GPU credit programs for students and academic researchers

---

## 6. Key Trends to Watch

1. **Decision/Reasoning Models:** Google's Gemini Decision 1 marks a new category of specialized decision-making models separate from general-purpose LLMs
2. **Multi-Model Orchestration:** Perplexity Orchestrator and similar APIs abstracting away single-provider lock-in
3. **Agentic RAG maturation:** Moving from retrieval pipelines to full agent-driven search with self-verification
4. **On-device AI push:** Apple Core AI, llama.cpp v1.0, and Ollama all maturing for offline/edge use cases
5. **LLM-generated research:** Growing academic concern (and tooling) around AI-written papers and verifiability
6. **Inference cost compression:** Qwen4-Max at $1.50/$4.50 and Tencent Hy4-Flash pushing frontier performance to commodity pricing

---

## Sources

- [New AI Models — November 2026 LLM Releases (LLM Gateway)](https://llmgateway.io/timeline)
- [New AI Models in November 2026: Every Major Release (BeevR)](https://beevr.ai/blog/ai-model-releases-november-2026)
- [New AI Models Released in November 2026: Prices (Capital & Compute)](https://capitalandcompute.net/blog/new-ai-models-november-2026/)
- [LLM News Today — November 2026 (LLM Stats)](https://llm-stats.com/ai-news)
- [Microsoft Ignite 2026: 7 Exciting AI Announcements (The Digital Brief)](https://thedigitalbriefnews.com/microsoft-ignite-2026-ai-models-tools/)
- [Microsoft MAI Models to Cut Cost of AI Coding (PYMNTS)](https://www.pymnts.com/news/artificial-intelligence/2026/microsoft-introduces-new-models-to-cut-the-cost-of-ai-coding-and-cybersecurity/)
- [Nvidia Open-Source AI Strategy After Huang Exit (Technology.org)](https://technology.org/2026/11/18/nvidia-open-source-ai-strategy-hugging-face-kress-huang-exit)
- [Hugging Face Blog](https://huggingface.co/blog)
- [Agentic RAG in 2026: 7 Patterns (Kanerika)](https://kanerika.com/blogs/agentic-rag/)
- [AI Agents Don't Need Vector Search Anymore (Medium)](https://buzzgrewal.medium.com/ai-agents-dont-need-vector-search-anymore-inside-the-agentic-search-stack-replacing-rag-in-2026-58efcabe4f6f)
- [ArXiv Daily Digest — Nov 17 (DailyArXiv)](https://github.com/jyyang621/DailyArXiv/issues/456)
- [ArXiv AI Research Digest — Nov 18 (news-radar)](https://github.com/datnguyenquy94/news-radar/issues/1124)
- [ArXiv cs.AI Current](https://arxiv.org/list/cs.AI/current)
- [ArXiv cs.LG Current](https://arxiv.org/list/cs.LG/current)
- [Free GPU Cloud Credits: 9 Programs That Changed in 2026 (Spheron)](https://www.spheron.network/blog/free-gpu-cloud-credits-2026/)
- [Free Cloud GPUs in 2026 (GPU Per Hour)](https://gpuperhour.com/blog/free-cloud-gpus-and-credits)
- [Hugging Face Pricing 2026 (MetaCTO)](https://www.metacto.com/blogs/the-true-cost-of-hugging-face-a-guide-to-pricing-and-integration)
- [Free GPU Credits for Students and Researchers (Aquanode)](https://www.aquanode.io/blog/free-gpu-credits-for-students-and-researchers)
- [Running AI Models Locally in 2026: Ollama, vLLM & Quantization (DEV)](https://dev.to/privatejack/running-ai-models-locally-in-2026-ollama-vllm-quantization-1222)
- [Local LLM Inference in 2026: Complete Guide (StarMorph)](https://blog.starmorph.com/blog/local-llm-inference-tools-guide)
- [vLLM vs Ollama vs SGLang: LLM Inference Compared 2026 (Winder.ai)](https://winder.ai/vllm-vs-ollama-vs-sglang-llm-inference-comparison/)
- [Top 9 AI Agent Frameworks as of November 2026 (Shakudo)](https://www.shakudo.io/blog/top-9-ai-agent-frameworks)
- [Perplexity Orchestrator (Future Tools)](https://futuretools.io/news)
