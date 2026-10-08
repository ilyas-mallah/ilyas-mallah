# Ilyas Mallah

I'm a software engineer working mostly in Luau, Rust, C++ and CUDA. My main interests are compilers and runtimes (JIT code generation, WebAssembly) and making code fast, from CPU hot paths to GPU kernels.

## Recent work

- [llama.cpp #30077](https://github.com/ggml-org/llama.cpp/pull/30077): decoding with a q4_0 KV cache ran at half speed on RTX 50 series GPUs in CUDA 12.8 builds. The fix makes long-context decoding up to 2.1x faster on an RTX 5090.
- [vLLM #60464](https://github.com/vllm-project/vllm/pull/60464): pick the SM90 block-FP8 CUTLASS kernel by batch size, 17 to 52% more serving throughput on an H100.
- [vLLM #60438](https://github.com/vllm-project/vllm/pull/60438): fall back from DeepGEMM instead of crashing at startup when nvcc is older than 12.9.
- [vLLM #60481](https://github.com/vllm-project/vllm/pull/60481): remove a residual copy per layer that a compiler pass left in block-FP8 models.

Earlier open-source work, mostly on the Luau compiler, its native code generator (x64 and AArch64) and its runtime, is under [green-real](https://github.com/green-real), with seven changes merged into Luau in 2026.

More at [ilyasm.dev](https://ilyasm.dev). Open to internships and contract work: hello@ilyasm.dev
