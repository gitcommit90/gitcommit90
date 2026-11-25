# Joseph Yaksich

Founder and director of [Public Bytes](https://publicbytes.org).

I'm an AI-native technical engineering leader with over six years of experience in media and broadcast operations, and over three years of experience building generative AI tools, data pipelines, and software automations. At Tennis Channel, where I'm Senior Manager of Digital Operations, I partner with business units to run discovery sessions, frame operational problems into technical requirements, and decide whether to build custom software or buy vendor products. I've built, tested, and deployed over 25 production applications and machine learning models that automate reporting, standardize unstructured data, and replace third-party software contracts. I also train non-technical teams to use AI tools safely and effectively in their daily work. Through Public Bytes, I also quantize, optimize, and serve open models on NVIDIA DGX Spark. That work is below.

## Model work on NVIDIA DGX Spark

### Quantization and decode optimization

- [sensenova-loop-9b-nvfp4-dgx-spark](https://github.com/Public-Bytes/sensenova-loop-9b-nvfp4-dgx-spark): calibrated NVFP4 quantization of SenseNova-Loop-9B. Single-request decode went from 12.4 to about 28 tokens/sec (per the repo README).
- [qwen38-flash-next-nvfp4-one-spark](https://github.com/Public-Bytes/qwen38-flash-next-nvfp4-one-spark): NVIDIA Qwen3.8-Flash-Next-NVFP4 on one DGX Spark, with the remaining large BF16 dense projections quantized to FP8 at load time and MTP speculation at K=3.
- [ripple-65b-dgx-spark](https://github.com/Public-Bytes/ripple-65b-dgx-spark): single-request decode optimizations for Ripple-65B Preview NVFP4 with its DFlash2 drafter: tree verification, fused MLP and an attention fix.

### Serving and deployment packages

- [glm-5.3-one-spark](https://github.com/Public-Bytes/glm-5.3-one-spark): GLM-5.3-Flash on one DGX Spark with vLLM. 64.1 tokens/sec on structured output; cold start cut from about 14 min to 3 min 21 s (per the repo README).
- [qwen38-27b-dgx-spark](https://github.com/Public-Bytes/qwen38-27b-dgx-spark): Qwen 3.8 27B NVFP4 on one DGX Spark with DFlash 2 speculative decoding, 262K context, vision and tool calling.
- [qwen38-flash-next-dgx-spark](https://github.com/Public-Bytes/qwen38-flash-next-dgx-spark): Qwen3.8-Flash-Next UD-IQ4_XS GGUF on one DGX Spark with llama.cpp: 262K context, vision and thinking controls.
- [laguna-s-2.1-nvfp4-dgx-spark](https://github.com/Public-Bytes/laguna-s-2.1-nvfp4-dgx-spark): Poolside Laguna S 2.1 NVFP4 with DFlash speculative decoding on vLLM, with concurrent benchmarks.
- [nvidia-qwen36-35b-nvfp4-dgx-spark](https://github.com/Public-Bytes/nvidia-qwen36-35b-nvfp4-dgx-spark): vLLM serving config for nvidia/Qwen3.6-35B-A3B-NVFP4 with NVFP4 MoE via Marlin, FP8 KV cache and MTP speculative decoding.
- [diffusiongemma-26b-a4b-it-nvfp4-dgx-spark](https://github.com/Public-Bytes/diffusiongemma-26b-a4b-it-nvfp4-dgx-spark): vLLM deployment of nvidia/diffusiongemma-26B-A4B-it-NVFP4, measured at 10 concurrent sessions.
- [internscience-agents-a1-dgx-spark](https://github.com/Public-Bytes/internscience-agents-a1-dgx-spark): vLLM deployment of InternScience Agents-A1, a 35B-A3B agentic vision-language model, measured at 10 concurrent sessions.
- [step37-flash-iq4xs-dgx-spark](https://github.com/Public-Bytes/step37-flash-iq4xs-dgx-spark): StepFun Step-3.7-Flash IQ4_XS GGUF (about 105 GB) on one DGX Spark with llama.cpp, aiming for the full 256K context.
- [deepseek-v4-flash-q4-dgx-spark](https://github.com/Public-Bytes/deepseek-v4-flash-q4-dgx-spark): llama.cpp serve config for a DeepSeek-V4-Flash Q4 GGUF (about 91 GB). Single-stream is measured; multi-concurrent is still broken.
- [angelslim-hy3-iq1m-mtp-dgx-spark](https://github.com/Public-Bytes/angelslim-hy3-iq1m-mtp-dgx-spark): AngelSlim Hy3 IQ1_M MTP GGUF on one DGX Spark with a patched llama.cpp (hy_v3 and MTP).

## Models on Hugging Face

[huggingface.co/gitcommit90](https://huggingface.co/gitcommit90)

- [SenseNova-Loop-9B-Preview-NVFP4](https://huggingface.co/gitcommit90/SenseNova-Loop-9B-Preview-NVFP4): community NVFP4 post-training quantization of sensenova/SenseNova-Loop-9B-Preview.
- [GLM-5.3-Flash-EXL3-2.05-One-Spark](https://huggingface.co/gitcommit90/GLM-5.3-Flash-EXL3-2.05-One-Spark): GLM-5.3-Flash on one DGX Spark using a 2.05-bpw EXL3 checkpoint and a DFlash2 drafter.
- [Qwen3.8-Flash-Next-NVFP4-DenseFP8-One-Spark](https://huggingface.co/gitcommit90/Qwen3.8-Flash-Next-NVFP4-DenseFP8-One-Spark): nvidia/Qwen3.8-Flash-Next-NVFP4 with in-loader FP8 conversion of the large dense projections and MTP K=3.

## Contributions to other model projects

- [spark-arena/community-recipe-registry #14](https://github.com/spark-arena/community-recipe-registry/pull/14): added the GLM-5.3-Flash EXL3 2.05-bpw one-Spark vLLM serving recipe (merged).
- [mllam/neural-lam #688](https://github.com/mllam/neural-lam/pull/688): fixed graph LAM GNN argument handling in model training and checkpoint loading for neural weather prediction (merged).
