# Hi, I'm Rui Sá

**I have 4.5 years of SAP and ABAP experience, I am completing a BSc in Computer Engineering, and I am building my path into AI Engineering.**

I spent approximately 4.5 years at Deloitte working with SAP, ABAP development, functional analysis, requirements, debugging, testing, and technical documentation. I am currently completing my Computer Engineering degree at the Polytechnic Institute of Setúbal, with graduation expected in 2027.

I am especially interested in Large Language Models, AI agents, evaluation systems, NLP, and intelligent automation. I like projects where I can measure whether an AI system is genuinely reliable instead of stopping when the demo looks convincing.

## My featured project: JudgeShift CX

[![JudgeShift CX results dashboard](https://raw.githubusercontent.com/ruimiguelyo/judgeshift-cx/main/.github/assets/dashboard.png?v=9993e42)](https://ruimiguelyo.github.io/judgeshift-cx/)

I built **JudgeShift CX** to test when an LLM can be trusted to evaluate customer-support responses — and when uncertainty or response-order sensitivity should force it to abstain.

[Explore my results dashboard](https://ruimiguelyo.github.io/judgeshift-cx/) · [Read my source code](https://github.com/ruimiguelyo/judgeshift-cx) · [View my v0.1.0 release](https://github.com/ruimiguelyo/judgeshift-cx/releases/tag/v0.1.0)

### The problem I chose to investigate

I did not want to build another thin wrapper around an LLM API. I wanted to investigate a harder question: if I use one AI system to grade another, how do I know that the grader agrees with documented human or policy references rather than following shortcuts such as response length, answer order, or language?

### What I built

- I curated a golden dataset with **36 customer-support evaluations organised into 18 English and Portuguese (Portugal) pairs**.
- I documented the provenance behind every reference, including controlled policy cases, six English HelpSteer3 human-preference examples, and clearly labelled Portuguese preference transfers.
- I compared a deliberately weak length baseline, a holistic LLM judge, a dimension-by-dimension rubric judge, and a selective rubric policy that abstains when the decision changes after reversing response order.
- I ran the LLM judges locally with **Qwen3-4B-Instruct-2507**, greedy decoding, a frozen model revision, and no remote inference API.
- I evaluated every pair in its original and reversed A/B order so I could normalize the chosen response and measure position sensitivity.
- I measured reference agreement, coverage, end-to-end accuracy, Cohen's kappa, Wilson confidence intervals, order-flip rate, parser repairs, and cross-language consistency.
- I added a Braintrust-compatible evaluation entry point without making a hosted Braintrust account necessary to reproduce my results.
- I built a responsive React and TypeScript dashboard that reads directly from the committed experiment artifacts and lets me inspect every decision case by case.

### What I found

| Strategy | Golden-set result | Targeted verbosity stress result |
| --- | ---: | ---: |
| Length baseline | 100.0% agreement | **0.0% agreement** |
| Holistic judge | 88.9% agreement | 94.4% agreement |
| Rubric judge | 94.4% agreement | 97.2% agreement |
| Selective rubric | **100.0% agreement at 86.1% coverage** | **100.0% agreement at 91.7% coverage** |

I found that the apparently perfect length baseline was actually exposing a dataset confound: every preferred response in the original set happened to be at least as long as its alternative. I kept that uncomfortable result and designed a targeted stress test that pads only the losing response until it becomes longer. The baseline immediately collapsed from 100% to 0%.

That is the result I value most in this project. I did not treat a perfect metric as a success until I understood why it was perfect. The experiment gave me evidence that a rubric-based judge was more robust to this shortcut, while the selective policy showed the practical trade-off between higher conditional agreement and lower coverage.

I describe the verbosity perturbation honestly as a label-informed, targeted stress test rather than an independent benchmark. I also document the small sample size, wide confidence intervals, transferred Portuguese labels, and limits of the human-preference subset instead of presenting the study as a universal measure of support quality.

### How I made it reproducible

- I committed the golden dataset, all **432 presentation-level decisions**, raw judge outputs, generated reports, and both base and stress-test artifacts.
- I recorded the exact dataset hash, source revision, model revision, prompt versions, decoding settings, Python environment, CUDA version, and GPU used for the run.
- I made metric rebuilding and Braintrust replay possible without rerunning the model or supplying an API key.
- I added **21 automated tests**, dataset and artifact-integrity checks, strict typing, formatting, linting, and a **75% minimum coverage gate**; the verified release reached **77.66% coverage**.
- I configured separate GitHub Actions pipelines for the Python evaluation system and the TypeScript dashboard, including automatic GitHub Pages deployment.
- I published methodology, dataset, model, results, limitations, security, contribution, licensing, and portfolio documentation alongside the code.

### What I used

I used **Python, Pydantic, scikit-learn, PyTorch, Transformers, Qwen, Braintrust, React, TypeScript, Vite, GitHub Actions, and GitHub Pages**.

### Evaluation foundations I studied and helped me build this
A lot of what I learned while building this project came from Braintrust's material and videos.

I started with their content on evals and LLM-as-a-judge, then searched for other ways to measure agreement between the judges and the expected results. That's how I ended up using Cohen's kappa from scikit-learn, which made more sense for what I wanted to measure than just looking at accuracy.

These were some of the resources that helped me:

- [Intro to Evals with Braintrust](https://www.youtube.com/watch?v=9uEay1jQM3w)
- [Evals 101](https://www.youtube.com/watch?v=bk0TmxoZlUY)
- [Braintrust Evals documentation](https://www.braintrust.dev/docs/evaluate)
- [What is an LLM-as-a-judge?](https://www.braintrust.dev/articles/what-is-llm-as-a-judge)
- [Cohen's kappa — scikit-learn](https://scikit-learn.org/stable/modules/generated/sklearn.metrics.cohen_kappa_score.html)

From there I kept experimenting and adding things as I ran into problems or questions while building the project.

[Read my methodology](https://github.com/ruimiguelyo/judgeshift-cx/blob/main/docs/METHODOLOGY.md) · [Inspect my results analysis](https://github.com/ruimiguelyo/judgeshift-cx/blob/main/docs/RESULTS.md) · [Review my limitations](https://github.com/ruimiguelyo/judgeshift-cx/blob/main/docs/LIMITATIONS.md)

## My professional background

### Deloitte — Developer, SAP ABAP & Functional Analysis

**October 2021 – March 2026 · Portugal · Hybrid · Full-time**

- I developed and maintained enterprise SAP solutions in ABAP from functional requirements.
- I worked across technical development and functional analysis, clarifying business needs and assessing impacts within SAP.
- I investigated incidents and defects through debugging and root-cause analysis.
- I prepared and executed tests, documented changes, and supported validation with business and technical stakeholders.
- I collaborated with multidisciplinary teams throughout structured delivery cycles.

## What I am focusing on now

- I am deepening my practical knowledge of LLM evaluation, NLP, AI agents, RAG, and tool-enabled workflows.
- I am applying software-engineering practices to AI systems whose behaviour, evidence, and limitations I can explain.
- I am continuing to learn Python, machine learning, data analysis, JavaScript, TypeScript, and SQL through my degree and personal work.
- I am looking for opportunities where I can combine my enterprise background with hands-on AI Engineering.

## My education

- I expect to complete my **BSc in Computer Engineering at the Polytechnic Institute of Setúbal in 2027**.
- I completed my **CTeSP in Software Engineering at the Polytechnic Institute of Setúbal in 2023**.

## What I value

- I value clear communication between technical and business teams.
- I value requirements, debugging, testing, documentation, and reproducible evidence.
- I prefer honest limitations and measurable behaviour to claims that a system is simply “intelligent”.
- I enjoy learning new technologies by building something concrete and then testing where it fails.

## Contact

You can find me on [LinkedIn](https://www.linkedin.com/in/rui-s%C3%A1-1243162ab/).

I am interested in Machine Learning and AI Engineering opportunities where I can help build useful, understandable, and reliable systems.
