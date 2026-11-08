### Yashwant Bezawada

Forward deployed engineer at FedEx. Tinkerer.

Fixes merged upstream:

- **vLLM** [#31057](https://github.com/vllm-project/vllm/pull/31057): CUDA-graph replay runs only the captured kernels, so the Python-side `wait_for_layer_load()` never ran and attention could read KV-cache data that had not finished loading. KV connectors can now require piecewise graphs, and the engine falls back to them at startup.
- **ROCm hipDNN** [#3552](https://github.com/ROCm/rocm-libraries/pull/3552): the samples exited 0 even when their output failed validation against the CPU reference, so CI could not catch a wrong answer. Each now returns its validation status across every type and layout variant, and they run under ctest.
- **QuantLib** [#2410](https://github.com/lballabio/QuantLib/pull/2410): `GsrProcessCore` held references to its input arrays, so the temporaries common in the Python bindings left them dangling and path generation segfaulted. It now keeps copies.
- **JAX** [#33602](https://github.com/jax-ml/jax/pull/33602): `jnp.arange` with a non-zero start was built as a NumPy array and embedded in the graph as a constant, so compile time grew with the size of the range. It now uses `iota` plus an offset.

[yashwantbezawada.com](https://yashwantbezawada.com) · [LinkedIn](https://www.linkedin.com/in/yashwantbezawada) · me@yashwantbezawada.com
