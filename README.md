# Hi, I'm Rui Sa

I have 4.5 years of SAP and ABAP experience, I am completing a BSc in Computer Engineering, and I am building my path into AI Engineering.

I spent approximately 4.5 years at Deloitte working with SAP, ABAP development, functional analysis, requirements, debugging, testing, and technical documentation. I am currently completing my Computer Engineering degree at the Polytechnic Institute of Setubal, with graduation expected in 2027.

I am especially interested in language models, evaluation systems, NLP, and AI engineering. I prefer projects where the model behaviour, measurements, and limitations can be inspected directly.

## Featured project: JAX Language Model Lab

[Read the repository](https://github.com/ruimiguelyo/jax-language-model-lab)

[![General-domain validation perplexity](https://raw.githubusercontent.com/ruimiguelyo/jax-language-model-lab/main/results/continual/figures/general_perplexity.png)](https://github.com/ruimiguelyo/jax-language-model-lab)

After building JudgeShift CX, I wanted to move one layer down. I could evaluate whether a language model's outputs were reliable, but I was still treating model training as a black box.

That led to a concrete question:

> If a language model learns a new domain continuously, can replay preserve its performance on the original domain when the adaptation token budget is fixed?

I built a small decoder-only Transformer in JAX and Flax instead of starting with a pretrained model or an inference API. The repository contains the training loop, checkpointing, evaluation, data packing, reservoir sampling, and the experiment that compares sequential adaptation, reservoir replay, and a joint-training reference.

### What I built

- A decoder-only Transformer with causal attention, learned positional embeddings, GELU MLP blocks, residual connections, normalization, tied embeddings, and language-modeling loss.
- A JAX training path using `jax.jit` and `jax.value_and_grad`, with Optax scheduling, clipping, checkpoint save/resume, and JSONL metrics.
- A fixed GPT-2 tokenizer used consistently across the general and target domains.
- Tests for output shapes, causal masking, finite losses and gradients, checkpoint resume, data packing, reservoir capacity, and tiny-dataset overfitting.
- A controlled continual-pretraining setup using WikiText-2 raw as the general corpus and AG News as the target corpus.
- Online reservoir sampling with a fixed buffer, replay ratio, token budget, initial checkpoint, optimizer, sequence length, and evaluation schedule.

### What I measured

The recorded run used a 3.3M-parameter model, one CPU device, and one seed.

| Strategy | General validation PPL | Target validation PPL | Forgetting |
| --- | ---: | ---: | ---: |
| Sequential | 4,474.44 | 7,534.90 | -0.5731 |
| Reservoir replay | 4,217.56 | 7,358.84 | -0.6322 |
| Joint-training reference | 4,258.46 | 7,433.48 | -0.6226 |

Forgetting is defined as `L_general,t - L_general,0`. The first run did not enter a forgetting regime: general-domain loss decreased during adaptation for every strategy. I kept that result because it identified a limitation in the setup rather than supporting a stronger conclusion than the experiment justified. The base model is small and undertrained, and the next useful experiment would use longer pretraining or a more separated target domain.

The tiny overfit test reduced loss from `2.0787` to `0.0009`. General-domain validation perplexity fell from `51,075.04` at initialization to `7,936.39` after the checkpoint was resumed to step 110.

### Reproducibility

- The configuration, seed, environment, hardware backend, metrics, and generated figures are stored with the recorded results.
- Raw datasets and checkpoints are not committed. Download and training commands are documented in the repository README.
- The project has 10 automated tests and passes `ruff check .`.
- The current environment did not provide an appropriate BF16 accelerator, so no BF16, CUDA, TPU, or distributed-training result is claimed.

## Technical resources

These papers, tutorials, and documentation were useful while implementing and checking the project:

- [Attention Is All You Need](https://arxiv.org/abs/1706.03762) for the Transformer formulation.
- [The Annotated Transformer](https://nlp.seas.harvard.edu/annotated-transformer/) for a readable implementation reference.
- [JAX documentation](https://docs.jax.dev/en/latest/) for transformations, arrays, and the execution model.
- [JAX asynchronous dispatch](https://docs.jax.dev/en/latest/async_dispatch.html) for synchronizing the precision benchmark before measuring elapsed time.
- [Flax documentation](https://flax.readthedocs.io/en/latest/) for Linen modules and training state structure.
- [Optax documentation](https://optax.readthedocs.io/en/latest/) for schedules, AdamW, and gradient clipping.
- [Hugging Face Datasets documentation](https://huggingface.co/docs/datasets/) for local dataset preparation and split handling.
- [Don't Stop Pretraining](https://arxiv.org/abs/2004.10964) for the motivation behind domain-adaptive pretraining.
- [Random Sampling with a Reservoir](https://doi.org/10.1145/3147.3165) for the reservoir-sampling algorithm.
- [WikiText dataset card](https://huggingface.co/datasets/Salesforce/wikitext) and [AG News dataset card](https://huggingface.co/datasets/fancyzhx/ag_news) for data provenance and usage limitations.

## Previous project: JudgeShift CX

[Read JudgeShift CX](https://github.com/ruimiguelyo/judgeshift-cx)

JudgeShift CX grew out of a practical question from running an Etsy store: if an AI system eventually helps answer customer messages, how do I know which generated responses are safe and useful enough to send? I built a bilingual evaluation bench comparing LLM judges, position sensitivity, and targeted stress tests.

The project taught me to investigate suspiciously good metrics instead of treating them as success. A length heuristic initially reached perfect agreement because the preferred responses were longer; after padding the losing responses, it collapsed to 0%. That experience led directly to the emphasis on controlled comparisons and negative results in the JAX language-model project.

## Professional background

### Deloitte - Developer, SAP ABAP and Functional Analysis

**October 2021 - March 2026 - Portugal - Hybrid - Full-time**

- I developed and maintained enterprise SAP solutions in ABAP from functional requirements.
- I worked across technical development and functional analysis, debugging, testing, documentation, and validation.
- I investigated incidents and defects through root-cause analysis.
- I collaborated with multidisciplinary teams throughout structured delivery cycles.

## What I am focusing on now

- Language-model training and evaluation.
- Continual learning, NLP, and AI agents.
- Reproducible experiments with measurable behaviour and explicit limitations.
- Combining enterprise software experience with hands-on machine-learning engineering.

## Education

- BSc in Computer Engineering, Polytechnic Institute of Setubal, expected 2027.
- CTeSP in Software Engineering, Polytechnic Institute of Setubal, 2023.

## Contact

[LinkedIn](https://www.linkedin.com/in/rui-s%C3%A1-1243162ab/)
