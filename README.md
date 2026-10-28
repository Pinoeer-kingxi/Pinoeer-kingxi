# Hi, I'm Weixi

I'm a master's student in Computer Technology at Northwestern Polytechnical University (NWPU). I work on efficient LLM inference and training systems, with a focus on runtime performance, GPU/NPU kernels, and KV cache management.

I'm looking for internships in **LLM inference optimization and AI systems**, remote or on-site.

[Email](mailto:weixilin307@gmail.com) · [GitHub](https://github.com/WEIXILIN0307)

## Open-source contributions

### Merged

- **verl-omni:** Added CPU placement for native reward models ([#694](https://github.com/verl-project/verl-omni/pull/694)) and migrated the SD3.5 OCR recipe to named rewards ([#695](https://github.com/verl-project/verl-omni/pull/695)).
- **vLLM-Omni:** Added remote SeedVR2 video restoration for ComfyUI ([#8505](https://github.com/vllm-project/vllm-omni/pull/8505)).

### In progress

- **Megatron-LM:** Activation offloading for GDN recurrence ([#7908](https://github.com/NVIDIA/Megatron-LM/pull/7908)), plus work on GDN2 and CUDA Graph support ([#8308](https://github.com/NVIDIA/Megatron-LM/pull/8308)).
- **SGLang-Omni:** PersonaPlex streaming and startup improvements, including [incremental history](https://github.com/sgl-project/sglang-omni/pull/3103), [warmup](https://github.com/sgl-project/sglang-omni/pull/3104), and [device-resident audio codes](https://github.com/sgl-project/sglang-omni/pull/3126).
- **vLLM:** Multimodal prefix-cache boundary handling for hybrid Mamba models ([#56818](https://github.com/vllm-project/vllm/pull/56818)).
- **Mooncake:** Encoder–Prefill–Decode disaggregation and reusable agent state ([#2836](https://github.com/kvcache-ai/Mooncake/pull/2836)).

[View my upstream pull requests](https://github.com/search?q=author%3AWEIXILIN0307+is%3Apr+-user%3AWEIXILIN0307+is%3Apublic&type=pullrequests)

## Selected projects

- **[MiniCPM-o on Ascend](https://github.com/WEIXILIN0307/llama.cpp-omni/tree/feat/ascend-cann):** Optimized multimodal inference across two NPUs, including CPU/NPU overlap, CANN operators, graph execution, and W8A8 quantization.
- **[Efficient VLM inference](https://github.com/WEIXILIN0307/AICASGC):** Optimized Qwen3-VL-2B with KV cache reuse, projection fusion, Triton kernels, and CUDA Graphs.
- **[MetaX C500 kernels](https://github.com/WEIXILIN0307/TileOPs-Metax/tree/feat/quant-per-channel-cast-fused):** Built and tuned fused quantization kernels with TileLang, profiling, and correctness tests.

## Interests and tools

- LLM inference, multimodal serving, KV and prefix caching
- Distributed training, activation offloading, and runtime scheduling
- Quantization, GPU/NPU kernels, profiling, and performance analysis

Python · PyTorch · CUDA · Triton · TileLang · CANN / AscendC · vLLM · llama.cpp

## Competitions and awards

- **MiniCPM × Ascend Inference Optimization Challenge:** 5th on the public leaderboard
- **IEEE AICAS 2026 Grand Challenge:** 7th place
- **CCF Open Source Innovation Competition:** Third Prize, Mooncake KVCache
- **Huawei MindSpore Model Development Challenge:** 3rd place / Silver, S1-MoE
- **MetaX Open Source Talent Camp:** Best Engineering Practice Award

## Education

- **Northwestern Polytechnical University:** Master's in Computer Technology, 2025–present
- **Shaanxi Normal University:** Bachelor's in Software Engineering, 2021–2025
