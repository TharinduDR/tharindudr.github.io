---
layout: page
title: About me
cover: false
---

ආයුබෝවන්(āyubōvan), Hi


I am a PhD Student at [Research Group in Computational Linguistics (RGCL)](http://rgcl.wlv.ac.uk/) in [University of Wolverhamton](https://www.wlv.ac.uk/) supervised by [Prof. Ruslan Mitkov](https://en.wikipedia.org/wiki/Ruslan_Mitkov) and [Dr Constantin Orasan](http://dinel.org.uk/). My current research focuses on using Deep Learning for applications in translation domain.

I received my bachelors degree from [University of Moratuwa, Sri Lanka](http://cse.mrt.ac.lk/), specializing in Computer Science & Engineering. After graduation, I worked as a Associate Technical Team Lead in R&D division of [CodeGen International](https://www.codegen.co.uk/) where I lead and managed Machine Learning and Data Science team. I worked on several machine learning projects related to travel domain, such as Personalization and Recommendation, Revenue Management, Review Mining, Chat bots etc.

I am interested in Deep Learning Applications in Natural Language Processing.


## Recent News
* In October 2019, my team (BRUMS) participated in [HASOC 2019](https://hasoc2019.github.io/) achieved third place out of 174 teams in English subtask. Also BRUMS were 8th from 93 teams in Hindi subtask and 8th out of 54 teams in German subtask.

* In October 2019, my team (RGCL) participated in [IDAT 2019](https://www.irit.fr/IDAT2019/) to detect irony in Arabic tweets. We achived 4th place out of 18 teams. 

* On August 26, 2019. A paper titled “RGCL at GermEval 2019: Offensive Language Detection with Deep Learning” was accepted at [KONVENS 2019.](https://2019.konvens.org/)

* On July 6, 2019. Four papers accepted to [RANLP 2019](http://lml.bas.bg/ranlp2019/start.php): Emoji Powered Capsule Network to Detect Type and Target of Offensive Posts in Social Media; Enhancing Unsupervised Sentence Similarity Methods with Deep Contextualised Word Representations; Toponym Detection in the Bio-Medical Domain: A Hybrid Approach with Deep Learning; Semantic Textual Similarity with Siamese Neural Networks.

* On March 10, 2019. A paper titled “RGCL-WLV at SemEval-2019 Task 12: Toponym Detection” was accepted at SemEval-2019.

* On March 4, 2019. A paper titled “Concept Discovery through Information Extraction in Restaurant Domain” was accepted at [CICLing 2019.](https://www.cicling.org/2019/)




## Recent Research Highlights

<ul>
{% for paper in site.data.papers.papers %}
  {% if paper.selected %}
  <li>
  {% include paper.html paper=paper %}
  </li>
  {% endif %}
{% endfor %}
</ul>

