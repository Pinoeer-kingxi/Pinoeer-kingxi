# 👋 Hi, I'm weixi

**AI Infrastructure · LLM Serving · Inference Optimization · Agent Systems**

I'm a master's student in Computer Technology at Northwestern Polytechnical University (NWPU). I work on efficient inference for language and multimodal models, from GPU/NPU kernels and runtime scheduling to KV-cache reuse and agent infrastructure.

## 🌱 Open Source

### Merged

- **verl-omni:** Migrated the SD3.5 V1 sync OCR recipe to named rewards and added compatibility tests. [#695](https://github.com/verl-project/verl-omni/pull/695)
- **MindSpore:** model ports covering [Shallow RNN](https://github.com/mindspore-ai/contrib/pull/234), [hierarchical memory for RL agents](https://github.com/mindspore-ai/contrib/pull/256), [Fisher-information analysis](https://github.com/mindspore-ai/contrib/pull/259), and [GANimation](https://github.com/mindspore-ai/contrib/pull/260)

[All merged upstream PRs](https://github.com/search?q=author%3APinoeer-kingxi+is%3Apr+is%3Amerged+-user%3APinoeer-kingxi&type=pullrequests)

### In Progress

- **vLLM-Omni:** [prefix-cache input replacement and request ownership](https://github.com/vllm-project/vllm-omni/pull/8221) · Draft
- **vLLM-Omni:** [Qwen3-Omni Code2Wav dtype correctness](https://github.com/vllm-project/vllm-omni/pull/8327) · Draft
- **vLLM-Omni:** [remote SeedVR2 video restoration in ComfyUI](https://github.com/vllm-project/vllm-omni/pull/8505) · Open
- **Megatron-LM:** [BF16/FLA GDN recurrence activation offloading](https://github.com/NVIDIA/Megatron-LM/pull/7908) · Draft
- **verl-omni:** [native reward models on CPU](https://github.com/verl-project/verl-omni/pull/694) · Open

Other ongoing contributions: **vLLM** [multimodal prefix-cache boundaries for Mamba models](https://github.com/vllm-project/vllm/pull/56818) (Draft) · **Mooncake** [multimodal and agent-state disaggregation](https://github.com/kvcache-ai/Mooncake/pull/2836) (Open) · **Relax** [speculative-decoding metrics for agentic rollouts](https://github.com/redai-studio/Relax/pull/391) (Open)

## 🛠️ Selected Engineering Work

### [MiniCPM-o on Ascend](https://github.com/Pinoeer-kingxi/llama.cpp-omni/tree/feat/ascend-cann)
Multimodal inference optimization in llama.cpp / ggml, spanning vision, language, and speech.
- Split the pipeline across two NPUs and overlapped CPU preprocessing with NPU encoding
- Optimized LLM/TTS execution with CANN Flash Attention, reusable graph execution, and reduced redundant prefill; developed AscendC operators for Token2Wav and explored mixed W8A8 quantization

### [Efficient VLM Inference](https://github.com/Pinoeer-kingxi/AICASGC)
Qwen3-VL-2B-Instruct optimization for the IEEE AICAS 2026 Grand Challenge.
- Reused bucketed static KV caches and visual prefixes, fused QKV and gate/up projections, and implemented Triton RMSNorm/SwiGLU kernels
- Built a single-token decode path with static buffers and CUDA Graph replay to reduce Python scheduling and kernel-launch overhead

### [Mooncake EPD & Agent State](https://github.com/kvcache-ai/Mooncake/pull/2836)
Encoder-Prefill-Decode disaggregation and reusable agent state. **Upstream PR open.**
- Passed visual features and KV state between stages, with version/model checks and explicit transfer lifetimes
- Implemented shared read-only KV pages, copy-on-write branching, and Store-backed state retrieval; reduced repeated media transfer through token-only Decode requests

### [MetaX C500 Kernel Optimization](https://github.com/Pinoeer-kingxi/TileOPs-Metax/tree/feat/quant-per-channel-cast-fused)
Per-channel quantization and cast fusion with TileLang.
- Unified four operator variants and tuned tiling, thread mapping, and local/shared-memory staging
- Built correctness tests, fixed-baseline benchmarks, and profiler/Roofline analysis alongside the kernel implementation

## 🔧 Toolkit

- **Inference & kernels:** Python, PyTorch, vLLM, llama.cpp / ggml, Triton, TileLang, CANN / AscendC
- **Optimization:** KV/prefix caching, CUDA Graphs, quantization, MoE expert batching, profiling, and regression testing
- **Agents & retrieval:** ReAct, RAG, Milvus, MCP, state management, and hybrid retrieval

## 🏆 Selected Competitions & Awards

- **2026 · IEEE AICAS Grand Challenge:** 7th place, efficient VLM inference and optimization
- **2026 · 8th CCF Open Source Innovation Competition:** Third Prize, Mooncake KVCache
- **2025 · Huawei MindSpore Model Development Challenge:** 3rd place (Silver), S1-MOE track
- **MetaX Open Source Talent Camp:** Best Engineering Practice Award
- **Alibaba Higress AI Gateway Development Challenge:** Third Prize

## 🎓 Education

- **Northwestern Polytechnical University** · Master's in Computer Technology · Sep 2025–present
- **Shaanxi Normal University** · Bachelor's in Software Engineering · Sep 2021–Jul 2025
