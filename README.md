# Joseph Yaksich

Founder and director of [Public Bytes](https://publicbytes.org).

I'm an AI-native technical engineering leader with over six years of experience in media and broadcast operations, and over three years of experience building generative AI tools, data pipelines, and software automations. At Tennis Channel, where I'm Senior Manager of Digital Operations, I partner with business units to run discovery sessions, frame operational problems into technical requirements, and decide whether to build custom software or buy vendor products. I've built, tested, and deployed over 25 production applications and machine learning models that automate reporting, standardize unstructured data, and replace third-party software contracts. I also train non-technical teams to use AI tools safely and effectively in their daily work. Through Public Bytes, I also quantize, optimize, and serve open models on NVIDIA DGX Spark. That work is below.

## Model work on NVIDIA DGX Spark

- [sensenova-loop-9b-nvfp4-dgx-spark](https://github.com/Public-Bytes/sensenova-loop-9b-nvfp4-dgx-spark): calibrated NVFP4 quantization of SenseNova-Loop-9B. Single-request decode went from 12.4 to about 28 tokens/sec (per the repo README).
- [glm-5.3-one-spark](https://github.com/Public-Bytes/glm-5.3-one-spark): GLM-5.3-Flash on one DGX Spark with vLLM. 64.1 tokens/sec on structured output; cold start cut from about 14 min to 3 min 21 s (per the repo README).

## Models on Hugging Face

[huggingface.co/gitcommit90](https://huggingface.co/gitcommit90)

- [SenseNova-Loop-9B-Preview-NVFP4](https://huggingface.co/gitcommit90/SenseNova-Loop-9B-Preview-NVFP4)
- [GLM-5.3-Flash-EXL3-2.05-One-Spark](https://huggingface.co/gitcommit90/GLM-5.3-Flash-EXL3-2.05-One-Spark)
- [Qwen3.8-Flash-Next-NVFP4-DenseFP8-One-Spark](https://huggingface.co/gitcommit90/Qwen3.8-Flash-Next-NVFP4-DenseFP8-One-Spark)
