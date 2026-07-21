---
permalink: /
title: "Junteng Liu"
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---

About Me
======
I am a first-year Ph.D. candidate in Computer Science at the Hong Kong University of Science and Technology (HKUST), where I am a member of the [HKUST NLP Group](https://hkust-nlp.github.io/) advised by Prof. Junxian He. I graduated from Shanghai Jiao Tong University (SJTU) with a Bachelor of Engineering degree in June 2024.

My research interests lie broadly in natural language processing and machine learning, with a particular focus on:
- **LLM Reasoning and Reinforcement Learning**
- **Hallucination in Vision-Language Models (VLM)**
- **LLM Truthfulness and Interpretability**

Prior to starting my Ph.D., I completed research internships at MINIMAX, Tencent WXG, and Shanghai AI Lab.

Contact
======
Email: jliugi [at] connect.ust.hk

Education
======
- **Ph.D. in Computer Science**, Hong Kong University of Science and Technology (HKUST), 2024 – Present
- **B.Eng.**, Shanghai Jiao Tong University (SJTU), 2020 – 2024

Research Experience
======
- **Research Intern, MINIMAX** (Feb 2025 – Present)
- **Research Intern, Tencent WXG** (Jun 2024 – Sep 2024) — advised by Zifei Shan
- **Research Intern, Shanghai AI Lab** (Jun 2023 – Dec 2023) — advised by Prof. Yu Cheng

Selected Publications
======
A full list is available on the [Publications](/publications/) page.

{% if site.author.googlescholar %}
  <div class="wordwrap">You can also find my articles on <a href="{{site.author.googlescholar}}">my Google Scholar profile</a>.</div>
{% endif %}

{% include base_path %}

<!-- New style rendering if publication categories are defined -->
{% if site.publication_category %}
  {% for category in site.publication_category  %}
    {% assign title_shown = false %}
    {% for post in site.publications reversed %}
      {% if post.category != category[0] %}
        {% continue %}
      {% endif %}
      {% unless title_shown %}
        <h2>{{ category[1].title }}</h2><hr />
        {% assign title_shown = true %}
      {% endunless %}
      {% include archive-single.html %}
    {% endfor %}
  {% endfor %}
{% else %}
  {% for post in site.publications reversed %}
    {% include archive-single.html %}
  {% endfor %}
{% endif %}

Honors & Awards
======
- Zhiyuan Honor Scholarship, Shanghai Jiao Tong University
