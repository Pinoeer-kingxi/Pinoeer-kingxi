# Hi, I'm weixi

I'm a master's student in Computer Technology at Northwestern Polytechnical University (NWPU). I work on LLM training and multimodal inference systems, including GPU/NPU kernels, runtime scheduling, KV caching, and agent infrastructure.

I'm seeking internship opportunities in **efficient LLM inference and AI systems**, remote or on-site. Contact: [weixilin307@gmail.com](mailto:weixilin307@gmail.com).

## Activity

![Profile views](https://komarev.com/ghpvc/?username=Pinoeer-kingxi&label=Profile+views&color=6e7781&style=flat)
[![Merged upstream PRs](https://img.shields.io/github/issues-search?query=author%3APinoeer-kingxi%20is%3Apr%20is%3Amerged%20-user%3APinoeer-kingxi%20is%3Apublic&label=merged%20upstream%20PRs&color=8957e5)](https://github.com/search?q=author%3APinoeer-kingxi%20is%3Apr%20is%3Amerged%20-user%3APinoeer-kingxi%20is%3Apublic&type=pullrequests)
[![Open upstream PRs](https://img.shields.io/github/issues-search?query=author%3APinoeer-kingxi%20is%3Apr%20is%3Aopen%20-user%3APinoeer-kingxi%20is%3Apublic&label=open%20upstream%20PRs&color=238636)](https://github.com/search?q=author%3APinoeer-kingxi%20is%3Apr%20is%3Aopen%20-user%3APinoeer-kingxi%20is%3Apublic&type=pullrequests)

<sub>PR counts cover my public authored PRs outside my own repositories; open PRs include drafts. Badges update automatically but may lag due to caching. Profile views count badge loads since this counter was enabled, not unique visitors or historical traffic.</sub>

## Open source

### Merged

- **verl-omni:** Added opt-in CPU placement for native reward models, with configurable Ray replicas and CPU resources. [#694](https://github.com/verl-project/verl-omni/pull/694)
- **vLLM-Omni:** Added remote SeedVR2 video restoration to ComfyUI, preserving frame count, source FPS and supported audio, with cancellation handling and workflow templates. [#8505](https://github.com/vllm-project/vllm-omni/pull/8505)
- **verl-omni:** Updated the SD3.5 V1 sync OCR recipe to use named rewards and added compatibility tests. [#695](https://github.com/verl-project/verl-omni/pull/695)
- **MindSpore:** Model ports covering [Shallow RNN](https://github.com/mindspore-ai/contrib/pull/234), [hierarchical memory for RL agents](https://github.com/mindspore-ai/contrib/pull/256), [Fisher-information analysis](https://github.com/mindspore-ai/contrib/pull/259), and [GANimation](https://github.com/mindspore-ai/contrib/pull/260).

[All merged upstream PRs](https://github.com/search?q=author%3APinoeer-kingxi+is%3Apr+is%3Amerged+-user%3APinoeer-kingxi&type=pullrequests)

### Open PRs

These contributions are not yet merged. Drafts are marked explicitly.

- **SGLang-Omni:**
  - Maintain PersonaPlex caller history incrementally, avoiding repeated full-history rebuilding. [#3103](https://github.com/sgl-project/sglang-omni/pull/3103)
  - Warm the PersonaPlex session LM before server readiness. [#3104](https://github.com/sgl-project/sglang-omni/pull/3104)
- **Megatron-LM:**
  - Offload BF16/FLA GDN recurrence activations. [#7908](https://github.com/NVIDIA/Megatron-LM/pull/7908); extend recurrence offloading to GDN2 and Transformer Engine CUDA graphs. [#8308](https://github.com/NVIDIA/Megatron-LM/pull/8308) (draft)
  - Fix forward chunk tracking for resident activation groups. [#8243](https://github.com/NVIDIA/Megatron-LM/pull/8243)
  - Respect deterministic settings in fused pre-GDR gate backward. [#8244](https://github.com/NVIDIA/Megatron-LM/pull/8244)
  - Log final DCP schedule balance and context-parallel size fractions. [#8431](https://github.com/NVIDIA/Megatron-LM/pull/8431)
- **verl-omni:**
  - Stream named rewards per sample. [#730](https://github.com/verl-project/verl-omni/pull/730) (draft)
  - Add diffusion V1 colocated asynchronous training. [#742](https://github.com/verl-project/verl-omni/pull/742) (draft)
- **vLLM-Omni:**
  - Preserve Qwen3-Omni Code2Wav embedding dtype. [#8327](https://github.com/vllm-project/vllm-omni/pull/8327)
  - Route stages through configured pipeline transitions. [#8745](https://github.com/vllm-project/vllm-omni/pull/8745)
  - Finalize replacement inputs and fence retired prefix-cache owners. [#8221](https://github.com/vllm-project/vllm-omni/pull/8221) (draft)
  - Isolate NIXL payload ownership during request cleanup. [#8744](https://github.com/vllm-project/vllm-omni/pull/8744) (draft)
  - Qwen3-Omni Talker codec lifecycle: [conditioning identity](https://github.com/vllm-project/vllm-omni/pull/8763), [replay after preemption](https://github.com/vllm-project/vllm-omni/pull/8764), [request-local decision batching](https://github.com/vllm-project/vllm-omni/pull/8765), and [request-end payload delivery](https://github.com/vllm-project/vllm-omni/pull/8766) (draft series)
- **vLLM:** Handle multimodal prefix-cache boundaries for Mamba models. [#56818](https://github.com/vllm-project/vllm/pull/56818)
- **Mooncake:** Disaggregate multimodal inference and agent state. [#2836](https://github.com/kvcache-ai/Mooncake/pull/2836)
- **Relax:** Aggregate speculative-decoding metrics for agentic rollouts. [#391](https://github.com/redai-studio/Relax/pull/391)

[All open upstream PRs](https://github.com/search?q=author%3APinoeer-kingxi+is%3Apr+is%3Aopen+-user%3APinoeer-kingxi&type=pullrequests)

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
