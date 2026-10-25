---
title: "Does Literal-Match Reranker Supervision Improve Generated Answers in RAG? An In-Domain and Transfer Study"
collection: publications
category: manuscripts
permalink: /publication/2026-literal-match-reranker-supervision
excerpt: '**First author.** Tests whether training a RAG reranker on passages that contain the exact answer improves generated answers, in-domain and under transfer to a new domain.'
date: 2026-09-02 # only the year is shown; the date orders the list
venue: 'Engineering Applications of Artificial Intelligence'
status: 'Under review'
# Fill these in when available; empty fields are hidden on the site.
paperurl:   # arXiv or PDF link, e.g. 'https://arxiv.org/abs/XXXX.XXXXX'
bibtexurl:  # e.g. '/files/geniyat2026evidence.bib'
slidesurl:  # e.g. '/files/geniyat2026evidence-slides.pdf'
citation: '<b>A. Geniyat</b>, Z. Fakhriddinov, A. Gulati. (2026). &quot;Does Literal-Match Reranker Supervision Improve Generated Answers in RAG? An In-Domain and Transfer Study.&quot; Manuscript under review, <i>Engineering Applications of Artificial Intelligence</i>.'
---

**Status:** under review at [*Engineering Applications of Artificial Intelligence*](https://www.sciencedirect.com/journal/engineering-applications-of-artificial-intelligence) (Elsevier). First-author research at Boston University.

**The question**

A reranker decides which passages a RAG system shows to its language model. To train it you need relevance labels, and question–answer data gives two kinds for free:

* **Document-level labels** mark every passage of the right document as relevant, even passages that don't contain the answer.
* **Literal-match labels** reward only passages that contain the reference answer word for word. They look more precise.

Does the more precise signal actually produce better answers? I tested it end to end, with the protocol frozen in advance and a clear success bar: at least +1 point of answer F1, statistically significant.

**Study design**

<figure>
  <img src="/images/research/rag-study-design.png" alt="Study design: rerankers adapted on TechQA, evaluated in-domain on TechQA and under transfer on Doc2Dial with a fixed Qwen3.5-9B generator">
  <figcaption>Rerankers (Qwen3-Reranker-0.6B with LoRA) are adapted on TechQA and evaluated with the same retrieval pipeline and a fixed Qwen3.5-9B generator. H = hybrid retrieval, U = unadapted reranker, B = document-level labels, L = literal-match labels.</figcaption>
</figure>

**Key findings**

* **In-domain** (208 held-out TechQA questions): passage ranking improves over hybrid retrieval, but the answer gain is small and not significant (+0.68 F1).
* **Transfer** (273 Doc2Dial dialogue turns, 3 paired seeds): literal-match labels rank evidence worse than document-level labels and give slightly lower answer F1 (−0.22).
* **In both studies**, clear differences in retrieval quality barely moved answer F1.

<figure>
  <img src="/images/research/rag-primary-estimates.png" alt="Answer F1 differences with 95% confidence intervals for both studies, below the +1 target">
  <figcaption>Primary estimates with 95% intervals. Neither study reached the prespecified +1 F1 target.</figcaption>
</figure>

<figure>
  <img src="/images/research/rag-method-means.png" alt="Bar charts: answer F1 is nearly flat across methods while evidence NDCG@4 varies">
  <figcaption>Under transfer, retrieval quality (right) differs clearly between methods, while answer F1 (left) barely moves.</figcaption>
</figure>

**Why it matters:** better retrieval scores did not reliably mean better answers. Reranker supervision should be judged by the answers it produces, not by retrieval metrics alone.

**Scale**

| | |
|---|---|
| TechQA questions (development / held-out) | 400 / 208 |
| Doc2Dial dialogue turns (dependency families) | 273 (235) |
| Generation records / reranker candidate scores | 8,736 / 152,880 |
| Bootstrap resamples / paired sign-flip tests | 20,000 / 100,000 |

**My role:** conceptualization, methodology, software, experiments, formal analysis, visualization, project administration and manuscript preparation.
