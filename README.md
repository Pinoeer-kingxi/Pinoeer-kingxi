# Hi, I'm weixi

I'm a master's student in Computer Technology at Northwestern Polytechnical University (NWPU). I work on LLM and multimodal inference, including GPU/NPU kernels, runtime scheduling, KV caching, and agent infrastructure.

## Open source

### Merged

- **verl-omni:** Updated the SD3.5 V1 sync OCR recipe to use named rewards and added compatibility tests. [#695](https://github.com/verl-project/verl-omni/pull/695)
- **MindSpore:** model ports covering [Shallow RNN](https://github.com/mindspore-ai/contrib/pull/234), [hierarchical memory for RL agents](https://github.com/mindspore-ai/contrib/pull/256), [Fisher-information analysis](https://github.com/mindspore-ai/contrib/pull/259), and [GANimation](https://github.com/mindspore-ai/contrib/pull/260)

[All merged upstream PRs](https://github.com/search?q=author%3APinoeer-kingxi+is%3Apr+is%3Amerged+-user%3APinoeer-kingxi&type=pullrequests)

### Open PRs

- **vLLM-Omni:**
  - [Fix prefix-cache input replacement and request ownership](https://github.com/vllm-project/vllm-omni/pull/8221) (draft)
  - [Fix Qwen3-Omni Code2Wav dtype handling](https://github.com/vllm-project/vllm-omni/pull/8327) (draft)
  - [Add remote SeedVR2 video restoration to ComfyUI](https://github.com/vllm-project/vllm-omni/pull/8505) (open)
- **Megatron-LM:** [Offload BF16/FLA GDN recurrence activations](https://github.com/NVIDIA/Megatron-LM/pull/7908) (draft)
- **verl-omni:** [Run native reward models on CPU](https://github.com/verl-project/verl-omni/pull/694) (open)
- **vLLM:** [Handle multimodal prefix-cache boundaries for Mamba models](https://github.com/vllm-project/vllm/pull/56818) (draft)
- **Mooncake:** [Disaggregate multimodal inference and agent state](https://github.com/kvcache-ai/Mooncake/pull/2836) (open)
- **Relax:** [Add speculative-decoding metrics for agentic rollouts](https://github.com/redai-studio/Relax/pull/391) (open)

## Projects

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

## Tools

- **Inference & kernels:** Python, PyTorch, vLLM, llama.cpp / ggml, Triton, TileLang, CANN / AscendC
- **Optimization:** KV/prefix caching, CUDA Graphs, quantization, MoE expert batching, profiling, and regression testing
- **Agents & retrieval:** ReAct, RAG, Milvus, MCP, state management, and hybrid retrieval

## Competitions and awards

- **2026 · IEEE AICAS Grand Challenge:** 7th place, efficient VLM inference and optimization
- **2026 · 8th CCF Open Source Innovation Competition:** Third Prize, Mooncake KVCache
- **2025 · Huawei MindSpore Model Development Challenge:** 3rd place (Silver), S1-MOE track
- **MetaX Open Source Talent Camp:** Best Engineering Practice Award
- **Alibaba Higress AI Gateway Development Challenge:** Third Prize

## Education

- **Northwestern Polytechnical University** · Master's in Computer Technology · Sep 2025–present
- **Shaanxi Normal University** · Bachelor's in Software Engineering · Sep 2021–Jul 2025
