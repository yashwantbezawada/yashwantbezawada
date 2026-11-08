### Yashwant Bezawada

Software engineer at FedEx, working as a forward deployed engineer. Tinkerer.

Fixes merged upstream:

- **vLLM** [#31057](https://github.com/vllm-project/vllm/pull/31057): CUDA-graph replay skipped the wait in layer-wise KV-cache loading, so attention could read cache data before it arrived. Those setups now fall back to piecewise graphs.
- **JAX** [#33602](https://github.com/jax-ml/jax/pull/33602): `jnp.arange` with a non-zero start was folded into a constant array, blowing up compile times for large ranges. It now builds the range from `iota`.
- **Transformers** [#42051](https://github.com/huggingface/transformers/pull/42051): tokenizers shared one `model_input_names` list, so changing it on one tokenizer changed every other one of that class.
- **QuantLib** [#2410](https://github.com/lballabio/QuantLib/pull/2410): `GsrProcessCore` kept references to temporary arrays, so path generation crashed. It now keeps copies.

[yashwantbezawada.com](https://yashwantbezawada.com) · [LinkedIn](https://www.linkedin.com/in/yashwantbezawada) · me@yashwantbezawada.com
