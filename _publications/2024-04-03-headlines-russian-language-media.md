---
title: "The Role of Computer Technologies in Formulating Effective Headlines for Russian-Language Media"
collection: publications
category: conferences
permalink: /publication/2024-headlines-russian-language-media
excerpt: 'Computational methods for analyzing and generating effective Russian-language media headlines, with a Telegram bot that suggests better headlines. Placed 2nd among 27 AI research papers. [IEEE Xplore](https://ieeexplore.ieee.org/document/10585477)'
date: 2024-04-03 # conference date (Astana, 3–4 April 2024)
venue: '2024 IEEE AITU: Digital Generation'
paperurl:   # PDF link if you want to host the accepted version, e.g. '/files/alkhaidar2024headlines.pdf'
bibtexurl:  # e.g. '/files/alkhaidar2024headlines.bib'
citation: 'D. Alkhaidar, <b>A. Geniyat</b>, I. Akhmetvaliyeva. (2024). &quot;The Role of Computer Technologies in Formulating Effective Headlines for Russian-Language Media.&quot; In <i>2024 IEEE AITU: Digital Generation</i>, Astana, Kazakhstan, pp. 140–145. <a href="https://doi.org/10.1109/IEEECONF61558.2024.10585477">doi:10.1109/IEEECONF61558.2024.10585477</a>'
---

**Links:** [IEEE Xplore](https://ieeexplore.ieee.org/document/10585477) · [DOI](https://doi.org/10.1109/IEEECONF61558.2024.10585477)

Peer-reviewed IEEE paper from my time as a research assistant at Astana IT University (supervisor: Ida Akhmetvaliyeva). I contributed to experimental design, data analysis, evaluation and manuscript preparation, and presented the work at the conference, where it placed **2nd among 27 AI research papers**.

**The idea**

A headline is the first thing a reader sees. We studied what makes Russian-language news headlines work, through content analysis, reader surveys and interviews, and turned it into a tool: a Telegram bot that takes a text and proposes a headline, with an explanation of why it should work.

**How it works**

<figure>
  <img src="/images/research/headline-bot-pipeline.jpg" alt="Pipeline: dataset, preprocessing, model training, compile and save model, model generates a headline in Telegram" style="max-width: 360px">
  <figcaption>A model is trained on a dataset of over a million news headlines (TensorFlow, pandas, NumPy), saved, and served through a Telegram bot.</figcaption>
</figure>

<figure>
  <img src="/images/research/headline-bot-telegram.jpg" alt="Telegram chat: the bot proposes a headline for a text and explains its choice point by point" style="max-width: 520px">
  <figcaption>The bot in action: it proposes a headline and explains the choice (informativeness, appeal, universality, keywords).</figcaption>
</figure>

**Examples from the paper**

| Original headline | Bot's version |
|---|---|
| Fresh news about Mbappe's presentation at Real Madrid | The deal of the century on the horizon: Mbappe moving to "Real"? |
| Pep Guardiola will leave Manchester City | Pep Guardiola leaves Manchester City after a historic treble: an era ends! |

Along the way I studied collaborative filtering and recommender systems (cosine and Tanimoto similarity, k-nearest neighbours) for personalizing headline suggestions.

<small>Figures © 2024 IEEE, from Alkhaidar, Geniyat & Akhmetvaliyeva, *2024 IEEE AITU: Digital Generation*, pp. 140–145.</small>
