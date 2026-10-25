---
layout: archive
title: "CV"
permalink: /cv/
author_profile: true
redirect_from:
  - /resume
---

{% include base_path %}

[Download the full CV (PDF)]({{ base_path }}/files/Assylkhan_Geniyat_CV.pdf)

**Research interests:** Large Language Models, Retrieval-Augmented Generation, Agentic AI, Reasoning, Efficient AI Systems

Education
======
* **M.S. in Artificial Intelligence**, Boston University, Jan 2026 – May 2027 (expected)
  * GPA: 4.00 / 4.00
* **B.S. in Computer Science**, Astana IT University, Kazakhstan, Sep 2022 – Jun 2025
  * GPA: 3.65 / 4.00; graduated with Honors; ranked 2nd of 120 in the major
  * Bachelor's thesis: *AI for Drug Discovery Using Molecular Docking*

Research experience
======
* **2026: First-author research, retrieval-augmented generation**, Boston University
  * **Research mentor: [Prof. Aaron Mueller](https://aaronmueller.github.io/)**, Department of Computer Science
  * Asked whether training a RAG reranker on answer-bearing passages (literal-match labels) yields better generated answers than document-level labels ([paper page]({{ base_path }}/publication/2026-literal-match-reranker-supervision)).
  * Controlled experiments with frozen protocols and a prespecified success criterion: Qwen3-Reranker-0.6B with LoRA, hybrid BM25/dense retrieval, 4 chunking strategies, fixed Qwen3.5-9B generator.
  * Evaluated in-domain (208 held-out TechQA questions) and under transfer (273 Doc2Dial dialogue turns, 3 paired seeds).
  * **Key finding:** clear gains in retrieval quality barely changed answer F1, so retrieval metrics alone are an unreliable guide for reranker supervision.

* **Dec 2023 – Jul 2024: Research Assistant**, Astana IT University (supervisor: Ida Akhmetvaliyeva)
  * Computational methods for effective Russian-language media headlines, combining content analysis with reader surveys and interviews.
  * Co-developed a Telegram bot that suggests and explains more engaging headlines, trained on 1M+ news headlines ([paper page]({{ base_path }}/publication/2024-headlines-russian-language-media)).
  * Studied collaborative filtering and recommender systems for personalizing headline suggestions.
  * Co-authored a peer-reviewed IEEE paper ([IEEE Xplore](https://ieeexplore.ieee.org/document/10585477)); presented it and won 2nd place among 27 AI research papers.

Publications & manuscripts
======
  <ul>{% for post in site.publications reversed %}
    {% include archive-single-cv.html %}
  {% endfor %}</ul>

Professional experience
======
* **Sep 2026 – present: Lecturer, AI & Data Science (part-time)**, Astana Hub, Tech Orda program
  * Designed the AI and data science curriculum and training program for the course.
  * Teach AI, data science and machine learning to a cohort of 40 students.

* **Jan 2026 – present: Instructional Technology Developer (Data & Automation)**, Boston University
  * AI agents, automation workflows and data pipelines for teaching evaluation and university operations.

* **Jul 2025 – Dec 2025: Machine Learning Engineer (Primary AI/ML Engineer)**, National Bank of Kazakhstan
  * Owned five production AI/ML systems end to end.
  * Enterprise AI-agent and retrieval system over 80,000+ financial and legal documents for 6+ departments.
  * Anti-fraud ML pipeline for cross-border transactions: 89% recall on suspicious chains above $500K.

* **Mar 2025 – May 2025: Machine Learning Engineer**, Ministry of Energy of Kazakhstan
  * Multilingual news classifier: about 25,000 articles a day in three languages at 97.2% accuracy.
  * Classification systems for five ministries; average recall raised from 78% to 90%.

Honors & scholarships
======
* **[Bolashak Presidential Scholarship](https://www.bolashak.gov.kz/en/o-stipendii)** (International Scholarship of the President of the Republic of Kazakhstan): fully funded graduate study at Boston University
* **Boston University Merit Scholarship**: $20,000
* **2nd Place, AI Research Paper Competition**, 2024: among 27 AI research papers
* **Full-Tuition Merit Scholarship**, Astana IT University
* **Samsung Innovation Campus Microqualification**: GPA 3.91 / 4.00; final project rated Excellent

Leadership & service
======
* **Sep 2023 – Apr 2024: Conference Organizer, [2024 IEEE AITU: Digital Generation](https://web.archive.org/web/20250126092743/http://student-conference.astanait.edu.kz/2024year)**, IEEE Student Branch, Astana IT University
  * Led IT operations and built the official conference website.
  * Listed in the conference committee of the IEEE proceedings ([IEEE Xplore](https://ieeexplore.ieee.org/document/10585419)).
  * 200 paper submissions from authors in 7 countries; 83 accepted into the IEEE proceedings.

* **2022 – 2025: Vice President, SIAM Student Chapter**, Astana IT University
  * Mentored 400+ first-year students in Linear Algebra through peer-led sessions.
  * Organized a student meeting with Boston University and Huawei representatives, plus seminars and workshops.

Outside research
======
* Anime, literature and running.
