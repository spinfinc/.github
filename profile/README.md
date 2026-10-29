# spinf

**Bulk classification and decision inference on one GPU.**

We built spinf-serve for our own work, reading millions of news articles a day with dozens of calibrated questions each,
and publish it because people asked to run it themselves. The content is read once, every question about it is answered
in the same pass, and each answer is a probability over the options you give instead of generated text. The same API runs
hosted at [spinf.com](https://spinf.com).

| | |
|---|---|
| [**spinf-serve**](https://github.com/spinfinc/spinf-serve) | The engine and server. One 24 GB GPU, an OpenAI-compatible API, scoring, extraction and prompt packs. `pip install "spinf-serve[server]"`, or the image `ghcr.io/spinfinc/spinf-serve` |
| [**spinf-prompts**](https://github.com/spinfinc/spinf-prompts) | The official prompt packs: calibrated question sets for content moderation, triage, products, reviews, brand and entertainment. Every known pack, ours and others', is listed in spinf-serve's [PACKS.md](https://github.com/spinfinc/spinf-serve/blob/main/PACKS.md) |
| [**spinf-client**](https://github.com/spinfinc/spinf-client) | The Python client, for the hosted API or your own server. `pip install spinf-client` |
| [**skills**](https://github.com/spinfinc/skills) | Agent skills for coding agents: calling the API, running the server, authoring packs. `claude plugin marketplace add spinfinc/skills && claude plugin install spinf@spinfinc`, or `npx skills add spinfinc/skills` |
| [**Models on Hugging Face**](https://huggingface.co/spinf) | The quantized checkpoints the engine serves: Gemma 4 12B and 31B in calibrated fp8, Qwen3.8 27B in int4, and Perplexity's decision model |

Start with the [quickstart](https://github.com/spinfinc/spinf-serve/blob/main/docs/quickstart.md). Questions, ideas, bugs and
packs to list go to the [issues of spinf-serve](https://github.com/spinfinc/spinf-serve/issues): there is no forum or chat, and
nothing is too small. The code and the packs are Apache 2.0; the skills are MIT.
