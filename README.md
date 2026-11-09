### Yashwant Bezawada

Forward Deployed Engineer at FedEx. Tinkerer.

I keep models answering questions in production. Upstream, I once fixed a race between KV-cache loads and CUDA-graph replay in vLLM, and I still bring it up unprompted.

A few fixes that got merged:

- **vLLM**: KV-cache loads could race CUDA-graph replay ([#31057](https://github.com/vllm-project/vllm/pull/31057))
- **ROCm hipDNN**: samples now fail when their output is wrong ([#3552](https://github.com/ROCm/rocm-libraries/pull/3552))
- **QuantLib**: a dangling-reference segfault from the Python bindings ([#2410](https://github.com/lballabio/QuantLib/pull/2410))
- **JAX**: `jnp.arange` compile time grew with the size of the range ([#33602](https://github.com/jax-ml/jax/pull/33602))

[yashwantbezawada.com](https://yashwantbezawada.com) · [LinkedIn](https://www.linkedin.com/in/yashwantbezawada) · me@yashwantbezawada.com
