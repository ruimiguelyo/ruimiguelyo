<p align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="./assets/profile-header.svg">
    <source media="(prefers-color-scheme: light)" srcset="./assets/profile-header.svg">
  <img src="./assets/profile-header.svg" alt="Rui Sá - AI engineering, LLM evaluation and reliable systems" width="100%">
  </picture>
</p>

<p align="center">
  <a href="https://www.linkedin.com/in/rui-s%C3%A1-1243162ab/"><img src="https://img.shields.io/badge/LinkedIn-connect-0B1627?style=for-the-badge&logo=linkedin&logoColor=F8FAFC&labelColor=E8B4CA" alt="Connect on LinkedIn"></a>
  <a href="mailto:ruimiguelsa.stb@gmail.com"><img src="https://img.shields.io/badge/Email-say%20hello-0B1627?style=for-the-badge&logo=gmail&logoColor=F8FAFC&labelColor=93D8E8" alt="Send Rui an email"></a>
  <a href="https://github.com/ruimiguelyo"><img src="https://img.shields.io/badge/GitHub-ruimiguelyo-0B1627?style=for-the-badge&logo=github&logoColor=F8FAFC&labelColor=F4C95D" alt="Rui's GitHub profile"></a>
</p>

<p align="center">
  <a href="#what-i-build">what I build</a> &nbsp;&middot;&nbsp;
  <a href="#featured-work">featured work</a> &nbsp;&middot;&nbsp;
  <a href="#toolbox">toolbox</a> &nbsp;&middot;&nbsp;
  <a href="#contact">contact</a>
</p>

<h2 id="what-i-build">A bridge between enterprise software and inspectable AI</h2>

<p>
  I am <strong>Rui Sá</strong>, a Computer Engineering student in Setúbal, Portugal, moving deliberately into AI Engineering. I spent 4.5 years at Deloitte building and debugging SAP/ABAP systems, and I now apply that same discipline to language models: define the question, control the comparison, measure the behaviour, and document the limits.
</p>

<blockquote>
  <strong>I build AI systems that can be inspected from the metric to the mechanism.</strong>
</blockquote>

<table>
  <tr>
    <td align="center" width="25%"><strong>4.5 years</strong><br><sub>enterprise software</sub></td>
    <td align="center" width="25%"><strong>3.3M</strong><br><sub>model parameters</sub></td>
    <td align="center" width="25%"><strong>36 cases</strong><br><sub>bilingual evaluation set</sub></td>
    <td align="center" width="25%"><strong>10 tests</strong><br><sub>JAX lab checks</sub></td>
  </tr>
</table>

<p align="center">
  <img src="./assets/research-loop.svg" alt="Rui's method: question, control, measure and document" width="100%">
</p>

<h2 id="featured-work">Featured work</h2>

<table>
  <tr>
    <td valign="top" width="50%">
      <h3><a href="https://github.com/ruimiguelyo/jax-language-model-lab">JAX Language Model Lab</a></h3>
      <p><strong>Decoder-only Transformer &middot; continual pretraining</strong></p>
      <p>A small language-model training stack built from the mechanism up instead of hiding behind a pretrained API. It compares sequential adaptation, reservoir replay and a joint-training reference under a fixed token budget.</p>
      <p>
        <img src="https://img.shields.io/badge/JAX-07111F?style=flat-square&logo=google&logoColor=93D8E8" alt="JAX">
        <img src="https://img.shields.io/badge/Flax-07111F?style=flat-square&logo=google&logoColor=E8B4CA" alt="Flax">
        <img src="https://img.shields.io/badge/Optax-07111F?style=flat-square&logoColor=F4C95D" alt="Optax">
        <img src="https://img.shields.io/badge/Python-07111F?style=flat-square&logo=python&logoColor=F4C95D" alt="Python">
      </p>
      <p><a href="https://github.com/ruimiguelyo/jax-language-model-lab">source code&nbsp;↗</a> &nbsp; <a href="https://github.com/ruimiguelyo/jax-language-model-lab/blob/main/README.md#results">results&nbsp;↗</a></p>
    </td>
    <td valign="top" width="50%">
      <h3><a href="https://github.com/ruimiguelyo/judgeshift-cx">JudgeShift CX</a></h3>
      <p><strong>LLM-as-a-judge evaluation platform</strong></p>
      <p>A bilingual benchmark and dashboard for testing whether LLM judges can be trusted. It makes order sensitivity, confidence, coverage, cross-language consistency and failure modes visible instead of reducing them to one headline score.</p>
      <p>
        <img src="https://img.shields.io/badge/Python-07111F?style=flat-square&logo=python&logoColor=F4C95D" alt="Python">
        <img src="https://img.shields.io/badge/TypeScript-07111F?style=flat-square&logo=typescript&logoColor=93D8E8" alt="TypeScript">
        <img src="https://img.shields.io/badge/React-07111F?style=flat-square&logo=react&logoColor=E8B4CA" alt="React">
        <img src="https://img.shields.io/badge/Braintrust-07111F?style=flat-square&logoColor=F4C95D" alt="Braintrust">
      </p>
      <p><a href="https://ruimiguelyo.github.io/judgeshift-cx/">live dashboard&nbsp;↗</a> &nbsp; <a href="https://github.com/ruimiguelyo/judgeshift-cx/releases/tag/v0.1.0">v0.1.0 study&nbsp;↗</a></p>
    </td>
  </tr>
</table>

<p align="center">
  <a href="https://github.com/ruimiguelyo/jax-language-model-lab">
    <img src="https://raw.githubusercontent.com/ruimiguelyo/jax-language-model-lab/main/results/continual/figures/general_perplexity.png" alt="General-domain validation perplexity for the JAX continual-pretraining experiment" width="82%">
  </a>
  <br>
  <sub>One recorded experiment, one CPU device, one seed: the chart stays because honest limitations are part of the result.</sub>
</p>

<h2>What I am working on</h2>

<table>
  <tr>
    <td valign="top" width="50%">
      <h3>Now / 2026</h3>
      <ul>
        <li>Language-model training, evaluation and continual learning.</li>
        <li>LLM agents with explicit measurements and useful abstention.</li>
        <li>Reproducible experiments where negative results are still informative.</li>
      </ul>
    </td>
    <td valign="top" width="50%">
      <h3>Before / 2021&ndash;2026</h3>
      <ul>
        <li>Developer at Deloitte working with SAP and ABAP.</li>
        <li>Functional analysis, requirements, debugging and root-cause work.</li>
        <li>Testing, technical documentation and multidisciplinary delivery.</li>
      </ul>
    </td>
  </tr>
</table>

<h2 id="toolbox">Toolbox</h2>

<p align="center">
  <img src="https://img.shields.io/badge/Python-07111F?style=for-the-badge&logo=python&logoColor=F4C95D" alt="Python">
  <img src="https://img.shields.io/badge/JAX-07111F?style=for-the-badge&logo=google&logoColor=93D8E8" alt="JAX">
  <img src="https://img.shields.io/badge/PyTorch-07111F?style=for-the-badge&logo=pytorch&logoColor=E8B4CA" alt="PyTorch">
  <img src="https://img.shields.io/badge/Hugging%20Face-07111F?style=for-the-badge&logo=huggingface&logoColor=F4C95D" alt="Hugging Face">
  <img src="https://img.shields.io/badge/TypeScript-07111F?style=for-the-badge&logo=typescript&logoColor=93D8E8" alt="TypeScript">
  <img src="https://img.shields.io/badge/React-07111F?style=for-the-badge&logo=react&logoColor=E8B4CA" alt="React">
</p>

<details>
  <summary><strong>Engineering detail</strong> &mdash; the tools behind the work</summary>
  <br>
  <table>
    <tr><td><strong>AI / ML</strong></td><td>JAX, Flax, Optax, PyTorch, Transformers, Qwen, NLP, generative AI, causal Transformers</td></tr>
    <tr><td><strong>Evaluation</strong></td><td>Braintrust, golden datasets, order swaps, Wilson intervals, Cohen's kappa, stress tests</td></tr>
    <tr><td><strong>Software</strong></td><td>Python, TypeScript, React, Pydantic, Typer, pytest, MyPy, Ruff, Vite, JSONL</td></tr>
    <tr><td><strong>Enterprise</strong></td><td>SAP, ABAP, functional analysis, requirements, debugging, testing, documentation</td></tr>
  </table>
</details>

<details>
  <summary><strong>Other builds</strong> &mdash; beyond the main research thread</summary>
  <br>
  <ul>
    <li><a href="https://github.com/ruimiguelyo/splitfx"><strong>SplitFX</strong></a> &mdash; explainable cross-currency settlements built with React and TypeScript.</li>
    <li><a href="https://github.com/ruimiguelyo/candidaturas-ai-scraper"><strong>Candidaturas AI Scraper</strong></a> &mdash; a local, transparent job-search workflow that exports deduplicated results.</li>
  </ul>
</details>

<details>
  <summary><strong>Live GitHub signal</strong> &mdash; updated from public activity</summary>
  <br>
  <p align="center">
    <picture>
      <source media="(prefers-color-scheme: dark)" srcset="https://github-profile-summary-cards.vercel.app/api/cards/stats?username=ruimiguelyo&amp;theme=github_dark&amp;hide_border=true&amp;bg_color=00000000&amp;title_color=E8B4CA&amp;text_color=CBD5E1&amp;icon_color=93D8E8">
      <source media="(prefers-color-scheme: light)" srcset="https://github-profile-summary-cards.vercel.app/api/cards/stats?username=ruimiguelyo&amp;theme=default&amp;hide_border=true&amp;bg_color=00000000&amp;title_color=9B496A&amp;text_color=334155&amp;icon_color=167B8F">
      <img src="https://github-profile-summary-cards.vercel.app/api/cards/stats?username=ruimiguelyo&amp;theme=github_dark&amp;hide_border=true&amp;bg_color=00000000&amp;title_color=E8B4CA&amp;text_color=CBD5E1&amp;icon_color=93D8E8" alt="Rui's GitHub public activity summary" width="49%">
    </picture>
    <picture>
      <source media="(prefers-color-scheme: dark)" srcset="https://github-profile-summary-cards.vercel.app/api/cards/repos-per-language?username=ruimiguelyo&amp;theme=github_dark&amp;hide_border=true&amp;bg_color=00000000&amp;title_color=E8B4CA&amp;text_color=CBD5E1&amp;icon_color=93D8E8">
      <source media="(prefers-color-scheme: light)" srcset="https://github-profile-summary-cards.vercel.app/api/cards/repos-per-language?username=ruimiguelyo&amp;theme=default&amp;hide_border=true&amp;bg_color=00000000&amp;title_color=9B496A&amp;text_color=334155&amp;icon_color=167B8F">
      <img src="https://github-profile-summary-cards.vercel.app/api/cards/repos-per-language?username=ruimiguelyo&amp;theme=github_dark&amp;hide_border=true&amp;bg_color=00000000&amp;title_color=E8B4CA&amp;text_color=CBD5E1&amp;icon_color=93D8E8" alt="Rui's public repositories by language" width="49%">
    </picture>
  </p>
  <p align="center"><sub>Public activity only. The project metrics above are the signal I use to describe the work.</sub></p>
</details>

<h2 id="contact">Let's build something measurable</h2>

<p>
  I am interested in ML/AI engineering roles and collaborations where software quality, model behaviour and evaluation matter. If you are working on reliable AI, language models, evaluation or agents, I would be glad to compare notes.
</p>

<p align="center">
  <a href="mailto:ruimiguelsa.stb@gmail.com"><strong>email</strong></a> &nbsp;&middot;&nbsp;
  <a href="https://www.linkedin.com/in/rui-s%C3%A1-1243162ab/"><strong>LinkedIn</strong></a> &nbsp;&middot;&nbsp;
  <a href="https://github.com/ruimiguelyo"><strong>GitHub</strong></a>
</p>

<p align="center"><sub>Profile README / maintained as a living lab notebook.</sub></p>
