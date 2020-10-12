---
layout: page
title: About me
cover: false
---

ආයුබෝවන්(āyubōvan), Hi


I am a PhD Student at [Research Group in Computational Linguistics (RGCL)](http://rgcl.wlv.ac.uk/) in [University of Wolverhamton](https://www.wlv.ac.uk/) supervised by [Prof Ruslan Mitkov](https://en.wikipedia.org/wiki/Ruslan_Mitkov) and [Prof Constantin Orasan](http://dinel.org.uk/). My current research focuses on using Deep Learning for applications in machine translation domain.

I received my bachelors degree from [University of Moratuwa, Sri Lanka](http://cse.mrt.ac.lk/), specialising in Computer Science & Engineering. After the graduation, I worked as an Associate Technical Team Lead in the R&D division of [CodeGen International](https://www.codegen.co.uk/) where I lead and managed the Machine Learning and Data Science team. I worked on several machine learning projects related to travel domain, such as Personalisation and Recommendation, Revenue Management, Review Mining, Chat bots etc.

I am interested in Deep Learning Applications in Natural Language Processing.


## Recent News

* On September 30th 2020, Our work on Translation Quality Estimation - "TransQuest: Translation Quality Estimation with Cross-lingual Transformers" was accepted to [COLING 2020](https://coling2020.org/) as a long paper. We release a QE framework for sentence-level quality estimation.

* On September 15th 2020, a short paper accepted to [EMNLP 2020](https://2020.emnlp.org/): "Multilingual Offensive Language Identification with Cross-lingual Embeddings" - We present our initial experiments on transfer learning for Offensive Language Identification in low resource languages.

* In August 2020, Our framework developed for Quality Estimation: [TransQuest](https://github.com/TharinduDR/TransQuest) won the first place in [WMT 2020](http://www.statmt.org/wmt20/) sentence-level DA shared task in all the language pairs and the multilingual track out of 50 participants. 

* On April 21st 2020, A paper titled "Intelligent Translation Memory Matching and Retrieval with Sentence Encoders" was accepted in [EAMT 2020](https://eamt2020.inesc-id.pt/). We release our early findings on using deep learning for translation memory matching and retrieval.

* On February 15th 2020. A paper titled "Offensive Language Identification in Greek" was accepted in [LREC 2020](https://lrec2020.lrec-conf.org/en/). We release an Offensive Language Identification dataset for Greek as well as several baseline models to tackle the task.

* In October 2019, my team (BRUMS) participated in [HASOC 2019](https://hasoc2019.github.io/) to identify Hate Speech and Offensive Content in Indo-European Languages. We achieved third place out of 174 teams in English subtask. Also BRUMS were 8th from 93 teams in Hindi subtask and 8th out of 54 teams in German subtask.

* In October 2019, my team (RGCL) participated in [IDAT 2019](https://www.irit.fr/IDAT2019/) to detect irony in Arabic tweets. We achived 4th place out of 18 teams. 

* On July 6, 2019. Four papers accepted to [RANLP 2019](http://lml.bas.bg/ranlp2019/start.php): Emoji Powered Capsule Network to Detect Type and Target of Offensive Posts in Social Media; Enhancing Unsupervised Sentence Similarity Methods with Deep Contextualised Word Representations; Toponym Detection in the Bio-Medical Domain: A Hybrid Approach with Deep Learning; Semantic Textual Similarity with Siamese Neural Networks.




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

