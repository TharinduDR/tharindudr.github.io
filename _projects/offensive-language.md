---
layout: page
title: Offensive Language and Hate Speech Detection
cover: false
---

<style>
/* Offensive-language project timeline: scoped so it does not affect other pages */
.ol-project {
  --ol-blue: #eaf4ff;
  --ol-blue-border: #8fc3ef;
  --ol-green: #edf8ee;
  --ol-green-border: #9fcfa3;
  --ol-gold: #fff7df;
  --ol-gold-border: #e4c36b;
  --ol-purple: #f3edff;
  --ol-purple-border: #b9a1e9;
  --ol-pink: #fff0f3;
  --ol-pink-border: #e8a4b3;
  --ol-activity: #f7f7f7;
  --ol-activity-border: #b9bec7;
  --ol-navy: #183b63;
  --ol-muted: #5f6975;
  --ol-line: #284a70;
}

.ol-project .ol-intro {
  max-width: 62rem;
  margin-bottom: 1.75rem;
}

.ol-project .ol-legend {
  display: grid;
  grid-template-columns: repeat(5, minmax(10rem, 1fr));
  gap: .7rem;
  margin: 1.25rem 0 1rem;
}

.ol-project .ol-legend-item,
.ol-project .ol-activity-legend {
  border-radius: 0;
  padding: .7rem .8rem;
  border: 1px solid;
  font-size: .78rem;
  line-height: 1.3;
}

.ol-project .ol-legend-item strong,
.ol-project .ol-activity-legend strong {
  display: block;
  font-size: .92rem;
  margin-bottom: .15rem;
}

.ol-project .theme-modelling { background: var(--ol-blue); border-color: var(--ol-blue-border); }
.ol-project .theme-resource { background: var(--ol-gold); border-color: var(--ol-gold-border); }
.ol-project .theme-explain { background: var(--ol-purple); border-color: var(--ol-purple-border); }
.ol-project .theme-perspective { background: var(--ol-pink); border-color: var(--ol-pink-border); }

.ol-project .ol-activity-legend {
  margin: 0 0 1.4rem;
  background: var(--ol-activity);
  border-color: var(--ol-activity-border);
}

.ol-project .ol-activity-legend span {
  margin-right: 1.2rem;
  white-space: nowrap;
}

/* Hydejack's content column is intentionally narrow. This lets just the
   timeline make use of the available viewport without changing site-wide widths. */
.ol-project .ol-breakout {
  width: min(92vw, 112rem);
  position: relative;
  left: 50%;
  transform: translateX(-50%);
  padding-inline: 1.25rem;
  box-sizing: border-box;
}

.ol-project .ol-scroll {
  overflow-x: auto;
  overflow-y: visible;
  padding: 1rem 2rem 2rem;
  scroll-padding-inline: 2rem;
  -webkit-overflow-scrolling: touch;
}

/* Years deliberately have different widths. Busy years get more horizontal
   room, so theme groups and individual papers can sit beside one another
   instead of forming one very tall stack. */
.ol-project .ol-canvas {
  width: max-content;
  min-width: 100%;
  display: grid;
  grid-template-columns:
    420px   /* 2019 */
    640px   /* 2020 */
    820px   /* 2021 */
    260px   /* 2022 */
    860px   /* 2023 */
    720px   /* 2024 */
    400px;  /* 2025 */
  column-gap: 1.1rem;
  padding-inline: 1rem;
  box-sizing: content-box;
}

.ol-project .ol-research {
  grid-column: 1 / -1;
  display: grid;
  grid-template-columns: subgrid;
  align-items: end;
  min-height: 31rem;
}

.ol-project .ol-year-research {
  padding: 0 .2rem .8rem;
  align-self: end;
  display: grid;
  grid-template-columns: repeat(2, minmax(0, 1fr));
  gap: .55rem;
  align-content: end;
}

.ol-project .ol-year-research > .ol-theme-group:only-child {
  grid-column: 1 / -1;
}

.ol-project .ol-theme-group {
  border: 1px solid;
  border-radius: 0;
  padding: .45rem;
  margin: 0;
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(175px, 1fr));
  gap: .35rem;
  align-content: start;
}

.ol-project .ol-theme-heading {
  grid-column: 1 / -1;
  font-weight: 700;
  font-size: .82rem;
  margin: 0 0 .1rem;
  line-height: 1.2;
}

.ol-project .ol-paper {
  background: rgba(255,255,255,.86);
  border: 1px solid rgba(20,30,40,.13);
  border-radius: 0;
  padding: .48rem .52rem;
  margin: 0;
  box-shadow: 0 1px 2px rgba(0,0,0,.035);
}

.ol-project .ol-paper-title {
  font-size: .75rem;
  line-height: 1.25;
  font-weight: 650;
}

.ol-project .ol-venue {
  display: block;
  margin-top: .18rem;
  font-size: .69rem;
  line-height: 1.2;
  font-style: italic;
  color: var(--ol-muted);
}

/* Central horizontal timeline */
.ol-project .ol-axis {
  grid-column: 1 / -1;
  display: grid;
  grid-template-columns: subgrid;
  position: relative;
  padding-top: 1.15rem;
  padding-bottom: 1rem;
}

.ol-project .ol-axis::before {
  content: "";
  position: absolute;
  left: .5rem;
  right: .5rem;
  top: .9rem;
  height: 3px;
  background: var(--ol-line);
  border-radius: 3px;
}

.ol-project .ol-axis::after {
  content: "";
  position: absolute;
  right: .15rem;
  top: .55rem;
  width: .75rem;
  height: .75rem;
  border-top: 3px solid var(--ol-line);
  border-right: 3px solid var(--ol-line);
  transform: rotate(45deg);
}

.ol-project .ol-year {
  text-align: center;
  position: relative;
  z-index: 1;
}

.ol-project .ol-year::before {
  content: "";
  display: block;
  width: .85rem;
  height: .85rem;
  margin: -.65rem auto .35rem;
  border-radius: 50%;
  background: var(--ol-line);
  border: 3px solid #fff;
  box-shadow: 0 0 0 2px var(--ol-line);
}

.ol-project .ol-year span {
  display: inline-block;
  background: #eef2f6;
  color: #25384d;
  border-radius: 1rem;
  padding: .15rem .65rem;
  font-weight: 700;
  font-size: .9rem;
}

.ol-project .ol-activities {
  grid-column: 1 / -1;
  display: grid;
  grid-template-columns: subgrid;
  align-items: start;
  min-height: 15rem;
}

.ol-project .ol-year-activities {
  padding: .5rem .2rem 0;
  display: grid;
  grid-template-columns: repeat(2, minmax(0, 1fr));
  gap: .45rem;
  align-content: start;
}

.ol-project .ol-activity-card {
  background: var(--ol-activity);
  border: 1px solid var(--ol-activity-border);
  border-radius: 0;
  padding: .5rem .55rem;
  margin: 0;
  font-size: .73rem;
  line-height: 1.25;
}

.ol-project .ol-activity-icon {
  display: inline-block;
  width: 1.25rem;
  font-size: 1rem;
  vertical-align: top;
}

.ol-project .ol-activity-card strong {
  color: #26374a;
}

.ol-project .ol-note {
  font-size: .76rem;
  color: var(--ol-muted);
  margin-top: .4rem;
}

@media screen and (max-width: 64em) {
  .ol-project .ol-legend {
    grid-template-columns: repeat(2, minmax(0, 1fr));
  }
  .ol-project .ol-breakout {
    width: 100%;
    left: auto;
    transform: none;
    padding-inline: 0;
  }

  .ol-project .ol-scroll {
    padding-inline: 1rem;
    scroll-padding-inline: 1rem;
  }
}

@media screen and (max-width: 38em) {
  .ol-project .ol-legend {
    grid-template-columns: 1fr;
  }
}
</style>

<div class="ol-project">

<p class="ol-intro">
My research on offensive language and hate speech detection spans four main themes:
model development, the creation of resources, explainability, and perspectives on
offensiveness. The timeline below groups publications by these themes while showing
related shared-task organisation, keynotes, and tutorials separately.
</p>

<div class="ol-legend">
  <div class="ol-legend-item theme-modelling">
    <strong>⚙ Modelling</strong>
    Discriminative, multilingual, cross-lingual, generative, multi-task, knowledge-distillation, robustness, and privacy-preserving approaches.
  </div>
  <div class="ol-legend-item theme-resource">
    <strong>▤ Resources</strong>
    Datasets and evaluation resources, particularly for under-resourced languages and language varieties.
  </div>
  <div class="ol-legend-item theme-explain">
    <strong>⌕ Explainability</strong>
    Offensive spans, targets, and other work that explains what a model identifies as offensive.
  </div>
  <div class="ol-legend-item theme-perspective">
    <strong>◉ Perspectives</strong>
    Human disagreement, vicarious offence, annotator perspectives, and subjectivity.
  </div>
</div>

<div class="ol-activity-legend">
  <strong>Activities</strong>
  <span>🏆 Shared-task organisation</span>
  <span>🎤 Keynote / tutorial</span>
</div>

<div class="ol-breakout">
<div class="ol-scroll">
<div class="ol-canvas">

  <!-- ===================== RESEARCH OUTPUTS ===================== -->
  <div class="ol-research">

    <!-- 2019 -->
    <div class="ol-year-research">
      <div class="ol-theme-group theme-modelling">
        <div class="ol-theme-heading">⚙ Modelling</div>

        <div class="ol-paper">
          <div class="ol-paper-title">Emoji Powered Capsule Network to Detect Type and Target of Offensive Posts in Social Media</div>
          <span class="ol-venue">RANLP 2019</span>
        </div>

        <div class="ol-paper">
          <div class="ol-paper-title">BRUMS at HASOC 2019: Deep Learning Models for Multilingual Hate Speech and Offensive Language Identification</div>
          <span class="ol-venue">FIRE 2019</span>
        </div>

        <div class="ol-paper">
          <div class="ol-paper-title">RGCL at GermEval 2019: Offensive Language Detection with Deep Learning</div>
          <span class="ol-venue">GermEval 2019</span>
        </div>
      </div>
    </div>

    <!-- 2020 -->
    <div class="ol-year-research">
      <div class="ol-theme-group theme-modelling">
        <div class="ol-theme-heading">⚙ Modelling</div>

        <div class="ol-paper">
          <div class="ol-paper-title">Multilingual Offensive Language Identification with Cross-lingual Embeddings</div>
          <span class="ol-venue">EMNLP 2020</span>
        </div>

        <div class="ol-paper">
          <div class="ol-paper-title">BRUMS at SemEval-2020 Task 12: Transformer Based Multilingual Offensive Language Identification in Social Media</div>
          <span class="ol-venue">SemEval 2020</span>
        </div>

        <div class="ol-paper">
          <div class="ol-paper-title">WLV-RIT at HASOC-Dravidian-CodeMix-FIRE2020: Offensive Language Identification in Code-switched YouTube Comments</div>
          <span class="ol-venue">FIRE 2020</span>
        </div>
      </div>

      <div class="ol-theme-group theme-resource">
        <div class="ol-theme-heading">▤ Resources</div>

        <div class="ol-paper">
          <div class="ol-paper-title">Offensive Language Identification in Greek</div>
          <span class="ol-venue">LREC 2020</span>
        </div>
      </div>
    </div>

    <!-- 2021 -->
    <div class="ol-year-research">
      <div class="ol-theme-group theme-modelling">
        <div class="ol-theme-heading">⚙ Modelling</div>

        <div class="ol-paper">
          <div class="ol-paper-title">FBERT: A Neural Transformer for Identifying Offensive Content</div>
          <span class="ol-venue">EMNLP Findings 2021</span>
        </div>

        <div class="ol-paper">
          <div class="ol-paper-title">WLV-RIT at GermEval 2021: Multitask Learning with Transformers to Detect Toxic, Engaging, and Fact-Claiming Comments</div>
          <span class="ol-venue">GermEval 2021</span>
        </div>
      </div>

      <div class="ol-theme-group theme-modelling">
        <div class="ol-theme-heading">⚙ Modelling</div>

        <div class="ol-paper">
          <div class="ol-paper-title">Multilingual Offensive Language Identification for Low-resource Languages</div>
          <span class="ol-venue">ACM TALLIP 2021</span>
        </div>

        <div class="ol-paper">
          <div class="ol-paper-title">An Evaluation of Multilingual Offensive Language Identification Methods for the Languages of India</div>
          <span class="ol-venue">Information 2021</span>
        </div>

        <div class="ol-paper">
          <div class="ol-paper-title">Cross-lingual Offensive Language Identification for Low Resource Languages: The Case of Marathi</div>
          <span class="ol-venue">RANLP 2021</span>
        </div>
      </div>

      <div class="ol-theme-group theme-explain">
        <div class="ol-theme-heading">⌕ Explainability</div>

        <div class="ol-paper">
          <div class="ol-paper-title">MUDES: Multilingual Detection of Offensive Spans</div>
          <span class="ol-venue">NAACL Demo 2021</span>
        </div>

        <div class="ol-paper">
          <div class="ol-paper-title">WLV-RIT at SemEval-2021 Task 5: A Neural Transformer Framework for Detecting Toxic Spans</div>
          <span class="ol-venue">SemEval 2021</span>
        </div>
      </div>

      <div class="ol-theme-group theme-resource">
        <div class="ol-theme-heading">▤ Resources</div>

        <div class="ol-paper">
          <div class="ol-paper-title">Transformer Models for Offensive Language Identification in Marathi</div>
          <span class="ol-venue">FIRE 2021</span>
        </div>
      </div>
    </div>

    <!-- 2022: no research-output cards; activities are shown below the axis -->
    <div class="ol-year-research"></div>

    <!-- 2023 -->
    <div class="ol-year-research">
      <div class="ol-theme-group theme-explain">
        <div class="ol-theme-heading">⌕ Explainability</div>

        <div class="ol-paper">
          <div class="ol-paper-title">Target-Based Offensive Language Identification</div>
          <span class="ol-venue">ACL 2023</span>
        </div>
      </div>

      <div class="ol-theme-group theme-perspective">
        <div class="ol-theme-heading">◉ Perspectives</div>

        <div class="ol-paper">
          <div class="ol-paper-title">Vicarious Offense and Noise Audit of Offensive Speech Classifiers: Unifying Human and Machine Disagreement on What is Offensive</div>
          <span class="ol-venue">EMNLP 2023</span>
        </div>
      </div>

      <div class="ol-theme-group theme-modelling">
        <div class="ol-theme-heading">⚙ Modelling</div>

        <div class="ol-paper">
          <div class="ol-paper-title">A Text-to-Text Model for Multilingual Offensive Language Identification</div>
          <span class="ol-venue">AACL Findings 2023</span>
        </div>

        <div class="ol-paper">
          <div class="ol-paper-title">Teacher and Student Models of Offensive Language in Social Media</div>
          <span class="ol-venue">ACL Findings 2023</span>
        </div>

        <div class="ol-paper">
          <div class="ol-paper-title">Offensive Language Identification with Multi-task Learning</div>
          <span class="ol-venue">Journal of Intelligent Information Systems 2023</span>
        </div>
      </div>

      <div class="ol-theme-group theme-modelling">
        <div class="ol-theme-heading">⚙ Modelling</div>

        <div class="ol-paper">
          <div class="ol-paper-title">Offensive Language Identification in Transliterated and Code-Mixed Bangla</div>
          <span class="ol-venue">BanglaLP at EMNLP 2023</span>
        </div>

        <div class="ol-paper">
          <div class="ol-paper-title">Publish or Hold? Automatic Comment Moderation in Luxembourgish News Articles</div>
          <span class="ol-venue">RANLP 2023</span>
        </div>
      </div>
    </div>

    <!-- 2024 -->
    <div class="ol-year-research">
      <div class="ol-theme-group theme-modelling">
        <div class="ol-theme-heading">⚙ Modelling</div>

        <div class="ol-paper">
          <div class="ol-paper-title">A Federated Learning Approach to Privacy Preserving Offensive Language Identification</div>
          <span class="ol-venue">TRAC at LREC-COLING 2024</span>
        </div>

        <div class="ol-paper">
          <div class="ol-paper-title">Towards Generalized Offensive Language Identification</div>
          <span class="ol-venue">ASONAM 2024</span>
        </div>
      </div>

      <div class="ol-theme-group theme-resource">
        <div class="ol-theme-heading">▤ Resources</div>

        <div class="ol-paper">
          <div class="ol-paper-title">SOLD: Sinhala Offensive Language Dataset</div>
          <span class="ol-venue">Language Resources and Evaluation 2024</span>
        </div>
      </div>

      <div class="ol-theme-group theme-modelling">
        <div class="ol-theme-heading">⚙ Modelling</div>

        <div class="ol-paper">
          <div class="ol-paper-title">On the Effects of Machine Translation on Offensive Language Detection</div>
          <span class="ol-venue">Social Network Analysis and Mining 2024</span>
        </div>
      </div>

      <div class="ol-theme-group theme-perspective">
        <div class="ol-theme-heading">◉ Perspectives</div>

        <div class="ol-paper">
          <div class="ol-paper-title">Rater Cohesion and Quality from a Vicarious Perspective</div>
          <span class="ol-venue">EMNLP Findings 2024</span>
        </div>
      </div>
    </div>

    <!-- 2025 -->
    <div class="ol-year-research">
      <div class="ol-theme-group theme-modelling">
        <div class="ol-theme-heading">⚙ Modelling</div>

        <div class="ol-paper">
          <div class="ol-paper-title">Does Machine Translation Impact Offensive Language Identification? The Case of Indo-Aryan Languages</div>
          <span class="ol-venue">LoResLM at COLING 2025</span>
        </div>
      </div>
    </div>

  </div>

  <!-- ===================== YEAR AXIS ===================== -->
  <div class="ol-axis">
    <div class="ol-year"><span>2019</span></div>
    <div class="ol-year"><span>2020</span></div>
    <div class="ol-year"><span>2021</span></div>
    <div class="ol-year"><span>2022</span></div>
    <div class="ol-year"><span>2023</span></div>
    <div class="ol-year"><span>2024</span></div>
    <div class="ol-year"><span>2025</span></div>
  </div>

  <!-- ===================== ACTIVITIES ===================== -->
  <div class="ol-activities">

    <!-- 2019 -->
    <div class="ol-year-activities"></div>

    <!-- 2020 -->
    <div class="ol-year-activities"></div>

    <!-- 2021 -->
    <div class="ol-year-activities">
      <div class="ol-activity-card">
        <span class="ol-activity-icon">🏆</span>
        <strong>Co-organised HASOC 2021</strong><br>
        Shared task on hate speech and offensive content identification in English and Indo-Aryan languages, including conversational hate speech.
      </div>
    </div>

    <!-- 2022 -->
    <div class="ol-year-activities">
      <div class="ol-activity-card">
        <span class="ol-activity-icon">🏆</span>
        <strong>Co-organised HASOC 2022</strong><br>
        Shared task covering English, Indo-Aryan languages, and offensive language identification in Marathi.
      </div>
    </div>

    <!-- 2023 -->
    <div class="ol-year-activities">
      <div class="ol-activity-card">
        <span class="ol-activity-icon">🏆</span>
        <strong>Co-organised HASOC 2023</strong><br>
        Shared task covering Assamese, Bengali, Bodo, Gujarati, and Sinhala.
      </div>

      <div class="ol-activity-card">
        <span class="ol-activity-icon">🏆</span>
        <strong>Co-organised OffensEval 2023</strong><br>
        Offensive language identification in the age of large language models.
      </div>

      <div class="ol-activity-card">
        <span class="ol-activity-icon">🎤</span>
        <strong>Keynote: Responsible Machine Learning: Challenges and Way Forward?</strong><br>
        RANLP 2023.
      </div>

      <div class="ol-activity-card">
        <span class="ol-activity-icon">🎤</span>
        <strong>Tutorial: Hate or not Hate? Beyond Binary Hate Speech Detection</strong><br>
        RANLP 2023.
      </div>
    </div>

    <!-- 2024 -->
    <div class="ol-year-activities"></div>

    <!-- 2025 -->
    <div class="ol-year-activities"></div>

  </div>

</div>
</div>
</div>

<p class="ol-note">
On smaller screens, the timeline can be scrolled horizontally. Each publication remains a separate square card, while related papers are visually grouped under Modelling, Resources, Explainability, or Perspectives within each year.
</p>

</div>
