# spinf

**Decision models: one input read once, hundreds of questions answered as probabilities.**

spinf turns open models into decision models. Instead of generating text, the model scores: a piece of content is read once and
every question about it is answered in the same pass with a probability, calibrated and batch-invariant. We publish the engine,
the question sets and the client; the same API runs hosted at [spinf.com](https://spinf.com).

| | |
|---|---|
| [**spinf-serve**](https://github.com/spinfinc/spinf-serve) | The open-source inference engine and server. One 24 GB GPU, an OpenAI-compatible API, scoring, extraction and prompt packs. `pip install "spinf-serve[server]"` |
| [**spinf-prompts**](https://github.com/spinfinc/spinf-prompts) | The official prompt packs: ready-made, calibrated question sets (content moderation, triage, products, reviews, brand, entertainment) preloaded into the server |
| [**spinf-client**](https://github.com/spinfinc/spinf-client) | The Python client, for the hosted API or your own server. `pip install spinf-client` |
| [**Models on Hugging Face**](https://huggingface.co/spinf) | The quantized checkpoints the engine serves: Gemma 4 12B and 31B in calibrated fp8, Qwen3.8 27B in int4, and the decision model |

Start with the [quickstart](https://github.com/spinfinc/spinf-serve/blob/main/docs/quickstart.md); questions and ideas go to the
issues of the repository they concern. Everything here is Apache 2.0.
