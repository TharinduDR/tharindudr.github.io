---
layout: page
title: Offensive Language and Hate Speech Detection
cover: false
---

<div class="ol-project">

<p>
My research on offensive language and hate speech detection has developed across four
connected themes: <strong>modelling</strong>, <strong>resources</strong>,
<strong>explainability</strong>, and <strong>perspectives</strong>. The diagram below
shows how each theme has progressed over a common timeline, together with related
shared-task organisation, keynotes and tutorials.
</p>

<style>
.ol-project {
  --ol-blue: #eaf3fb;
  --ol-blue-border: #8bb4d5;
  --ol-yellow: #fff6d9;
  --ol-yellow-border: #d6b85d;
  --ol-purple: #f1eafa;
  --ol-purple-border: #9a86c5;
  --ol-pink: #fdebed;
  --ol-pink-border: #cb8b98;
  --ol-activity: #f5f5f5;
  --ol-activity-border: #a9a9a9;
  --ol-line: #27496d;
  --ol-text: #333;
}

.ol-project .ol-breakout {
  width: min(94vw, 118rem);
  position: relative;
  left: 50%;
  transform: translateX(-50%);
  padding-inline: 2rem;
  box-sizing: border-box;
}

.ol-project .ol-scroll {
  overflow-x: auto;
  overflow-y: visible;
  padding: 1rem 5rem 2rem 8rem;
  scroll-padding-left: 8rem;
  scroll-padding-right: 5rem;
  -webkit-overflow-scrolling: touch;
}

.ol-project .ol-board {
  width: max-content;
  min-width: 100%;
  display: grid;
  grid-template-columns:
    11rem
    25rem   /* 2019 */
    31rem   /* 2020 */
    37rem   /* 2021 */
    14rem   /* 2022 */
    42rem   /* 2023 */
    38rem   /* 2024 */
    28rem;  /* 2025 */
  column-gap: .8rem;
  row-gap: .85rem;
  align-items: start;
  color: var(--ol-text);
}

/* Theme labels */
.ol-project .ol-lane-label {
  font-weight: 700;
  font-size: .9rem;
  padding: .6rem .65rem;
  border-left: 5px solid;
  line-height: 1.25;
}

.ol-project .theme-modelling {
  background: var(--ol-blue);
  border-color: var(--ol-blue-border);
}
.ol-project .theme-resources {
  background: var(--ol-yellow);
  border-color: var(--ol-yellow-border);
}
.ol-project .theme-explainability {
  background: var(--ol-purple);
  border-color: var(--ol-purple-border);
}
.ol-project .theme-perspectives {
  background: var(--ol-pink);
  border-color: var(--ol-pink-border);
}

/* Year cells above the timeline */
.ol-project .ol-cell {
  min-width: 0;
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(11.5rem, 1fr));
  gap: .42rem;
  align-content: start;
}

.ol-project .ol-paper {
  background: rgba(255,255,255,.92);
  border: 1px solid rgba(40,50,60,.20);
  padding: .52rem .58rem;
  line-height: 1.27;
  font-size: .76rem;
  min-width: 0;
}

.ol-project .ol-paper-title {
  display: block;
  font-weight: 700;
  font-size: .78rem;
  margin-bottom: .15rem;
}

.ol-project .ol-venue {
  display: block;
  margin-top: .25rem;
  font-style: italic;
  color: #666;
  font-size: .7rem;
}

/* The common timeline */
.ol-project .ol-axis-label {
  font-weight: 700;
  color: #555;
  align-self: center;
  text-align: right;
  padding-right: .65rem;
}

.ol-project .ol-year {
  position: relative;
  text-align: center;
  font-weight: 700;
  padding: 1rem .2rem .15rem;
  border-top: 3px solid var(--ol-line);
}

.ol-project .ol-year::before {
  content: "";
  position: absolute;
  top: -8px;
  left: 50%;
  width: 12px;
  height: 12px;
  transform: translateX(-50%);
  border-radius: 50%;
  background: white;
  border: 3px solid var(--ol-line);
}

.ol-project .ol-year:last-child::after {
  content: "→";
  position: absolute;
  right: -1.4rem;
  top: -.95rem;
  color: var(--ol-line);
  font-size: 1.8rem;
  font-weight: 700;
}

/* Activities below */
.ol-project .ol-activities-label {
  font-weight: 700;
  padding: .6rem .65rem;
  border-left: 5px solid #777;
  background: var(--ol-activity);
  line-height: 1.25;
}

.ol-project .ol-activity-cell {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(11rem, 1fr));
  gap: .42rem;
  align-content: start;
}

.ol-project .ol-activity {
  border: 1px solid var(--ol-activity-border);
  background: var(--ol-activity);
  padding: .52rem .58rem;
  font-size: .75rem;
  line-height: 1.27;
}

.ol-project .ol-activity-title {
  font-weight: 700;
  display: block;
  margin-bottom: .12rem;
}

.ol-project .ol-note {
  margin-top: 1rem;
  font-size: .78rem;
  color: #666;
}

@media screen and (max-width: 64em) {
  .ol-project .ol-breakout {
    width: 100%;
    left: auto;
    transform: none;
    padding-inline: 0;
  }

  .ol-project .ol-scroll {
    padding: 1rem 1.25rem 2rem;
    scroll-padding-inline: 1.25rem;
  }
}
</style>

<div class="ol-breakout">
<div class="ol-scroll">
<div class="ol-board">

  <!-- MODELLING -->
  <div class="ol-lane-label theme-modelling">⚙ Modelling</div>

  <div class="ol-cell theme-modelling">
    <div class="ol-paper">
      <span class="ol-paper-title">Emoji Powered Capsule Network to Detect Type and Target of Offensive Posts in Social Media</span>
      <span class="ol-venue">RANLP 2019</span>
    </div>
    <div class="ol-paper">
      <span class="ol-paper-title">BRUMS at HASOC 2019: Deep Learning Models for Multilingual Hate Speech and Offensive Language Identification</span>
      <span class="ol-venue">FIRE 2019</span>
    </div>
    <div class="ol-paper">
      <span class="ol-paper-title">RGCL at GermEval 2019: Offensive Language Detection with Deep Learning</span>
      <span class="ol-venue">GermEval 2019</span>
    </div>
  </div>

  <div class="ol-cell theme-modelling">
    <div class="ol-paper">
      <span class="ol-paper-title">Multilingual Offensive Language Identification with Cross-lingual Embeddings</span>
      <span class="ol-venue">EMNLP 2020</span>
    </div>
    <div class="ol-paper">
      <span class="ol-paper-title">BRUMS at SemEval-2020 Task 12: Transformer Based Multilingual Offensive Language Identification in Social Media</span>
      <span class="ol-venue">SemEval 2020</span>
    </div>
    <div class="ol-paper">
      <span class="ol-paper-title">WLV-RIT at HASOC-Dravidian-CodeMix-FIRE2020: Offensive Language Identification in Code-switched YouTube Comments</span>
      <span class="ol-venue">FIRE 2020</span>
    </div>
  </div>

  <div class="ol-cell theme-modelling">
    <div class="ol-paper">
      <span class="ol-paper-title">FBERT: A Neural Transformer for Identifying Offensive Content</span>
      <span class="ol-venue">EMNLP Findings 2021</span>
    </div>
    <div class="ol-paper">
      <span class="ol-paper-title">Multilingual Offensive Language Identification for Low-resource Languages</span>
      <span class="ol-venue">ACM TALLIP 2021</span>
    </div>
    <div class="ol-paper">
      <span class="ol-paper-title">An Evaluation of Multilingual Offensive Language Identification Methods for the Languages of India</span>
      <span class="ol-venue">Information 2021</span>
    </div>
    <div class="ol-paper">
      <span class="ol-paper-title">Cross-lingual Offensive Language Identification for Low Resource Languages: The Case of Marathi</span>
      <span class="ol-venue">RANLP 2021</span>
    </div>
    <div class="ol-paper">
      <span class="ol-paper-title">WLV-RIT at GermEval 2021: Multitask Learning with Transformers to Detect Toxic, Engaging, and Fact-Claiming Comments</span>
      <span class="ol-venue">GermEval 2021</span>
    </div>
  </div>

  <div class="ol-cell"></div>

  <div class="ol-cell theme-modelling">
    <div class="ol-paper">
      <span class="ol-paper-title">A Text-to-Text Model for Multilingual Offensive Language Identification</span>
      <span class="ol-venue">AACL Findings 2023</span>
    </div>
    <div class="ol-paper">
      <span class="ol-paper-title">Teacher and Student Models of Offensive Language in Social Media</span>
      <span class="ol-venue">ACL Findings 2023</span>
    </div>
    <div class="ol-paper">
      <span class="ol-paper-title">Offensive Language Identification with Multi-task Learning</span>
      <span class="ol-venue">Journal of Intelligent Information Systems 2023</span>
    </div>
    <div class="ol-paper">
      <span class="ol-paper-title">Publish or Hold? Automatic Comment Moderation in Luxembourgish News Articles</span>
      <span class="ol-venue">RANLP 2023</span>
    </div>
  </div>

  <div class="ol-cell theme-modelling">
    <div class="ol-paper">
      <span class="ol-paper-title">A Federated Learning Approach to Privacy Preserving Offensive Language Identification</span>
      <span class="ol-venue">TRAC at LREC-COLING 2024</span>
    </div>
    <div class="ol-paper">
      <span class="ol-paper-title">Towards Generalized Offensive Language Identification</span>
      <span class="ol-venue">ASONAM 2024</span>
    </div>
    <div class="ol-paper">
      <span class="ol-paper-title">On the Effects of Machine Translation on Offensive Language Detection</span>
      <span class="ol-venue">Social Network Analysis and Mining 2024</span>
    </div>
  </div>

  <div class="ol-cell theme-modelling">
    <div class="ol-paper">
      <span class="ol-paper-title">Does Machine Translation Impact Offensive Language Identification? The Case of Indo-Aryan Languages</span>
      <span class="ol-venue">LoResLM at COLING 2025</span>
    </div>
  </div>


  <!-- RESOURCES -->
  <div class="ol-lane-label theme-resources">▤ Resources</div>

  <div class="ol-cell"></div>

  <div class="ol-cell theme-resources">
    <div class="ol-paper">
      <span class="ol-paper-title">Offensive Language Identification in Greek</span>
      <span class="ol-venue">LREC 2020</span>
    </div>
  </div>

  <div class="ol-cell theme-resources">
    <div class="ol-paper">
      <span class="ol-paper-title">Marathi Offensive Language Dataset (MOLD)</span>
      <span class="ol-venue">RANLP 2021</span>
    </div>
    <div class="ol-paper">
      <span class="ol-paper-title">Transformer Models for Offensive Language Identification in Marathi</span>
      <span class="ol-venue">FIRE 2021</span>
    </div>
  </div>

  <div class="ol-cell"></div>

  <div class="ol-cell theme-resources">
    <div class="ol-paper">
      <span class="ol-paper-title">Offensive Language Identification in Transliterated and Code-Mixed Bangla</span>
      <span class="ol-venue">BanglaLP at EMNLP 2023</span>
    </div>
  </div>

  <div class="ol-cell theme-resources">
    <div class="ol-paper">
      <span class="ol-paper-title">SOLD: Sinhala Offensive Language Dataset</span>
      <span class="ol-venue">Language Resources and Evaluation 2024</span>
    </div>
  </div>

  <div class="ol-cell"></div>


  <!-- EXPLAINABILITY -->
  <div class="ol-lane-label theme-explainability">⌕ Explainability</div>

  <div class="ol-cell"></div>
  <div class="ol-cell"></div>

  <div class="ol-cell theme-explainability">
    <div class="ol-paper">
      <span class="ol-paper-title">MUDES: Multilingual Detection of Offensive Spans</span>
      <span class="ol-venue">NAACL Demo 2021</span>
    </div>
    <div class="ol-paper">
      <span class="ol-paper-title">WLV-RIT at SemEval-2021 Task 5: A Neural Transformer Framework for Detecting Toxic Spans</span>
      <span class="ol-venue">SemEval 2021</span>
    </div>
  </div>

  <div class="ol-cell"></div>

  <div class="ol-cell theme-explainability">
    <div class="ol-paper">
      <span class="ol-paper-title">Target-Based Offensive Language Identification</span>
      <span class="ol-venue">ACL 2023</span>
    </div>
  </div>

  <div class="ol-cell"></div>
  <div class="ol-cell"></div>


  <!-- PERSPECTIVES -->
  <div class="ol-lane-label theme-perspectives">◉ Perspectives</div>

  <div class="ol-cell"></div>
  <div class="ol-cell"></div>
  <div class="ol-cell"></div>
  <div class="ol-cell"></div>

  <div class="ol-cell theme-perspectives">
    <div class="ol-paper">
      <span class="ol-paper-title">Vicarious Offense and Noise Audit of Offensive Speech Classifiers: Unifying Human and Machine Disagreement on What is Offensive</span>
      <span class="ol-venue">EMNLP 2023</span>
    </div>
  </div>

  <div class="ol-cell theme-perspectives">
    <div class="ol-paper">
      <span class="ol-paper-title">Rater Cohesion and Quality from a Vicarious Perspective</span>
      <span class="ol-venue">EMNLP Findings 2024</span>
    </div>
  </div>

  <div class="ol-cell"></div>


  <!-- COMMON TIMELINE -->
  <div class="ol-axis-label">Timeline</div>
  <div class="ol-year">2019</div>
  <div class="ol-year">2020</div>
  <div class="ol-year">2021</div>
  <div class="ol-year">2022</div>
  <div class="ol-year">2023</div>
  <div class="ol-year">2024</div>
  <div class="ol-year">2025</div>


  <!-- ACTIVITIES -->
  <div class="ol-activities-label">Activities</div>

  <div class="ol-activity-cell"></div>
  <div class="ol-activity-cell"></div>

  <div class="ol-activity-cell">
    <div class="ol-activity">
      <span class="ol-activity-title">🏆 HASOC 2021</span>
      Co-organised the shared task on hate speech and offensive content identification in English and Indo-Aryan languages.
    </div>
  </div>

  <div class="ol-activity-cell">
    <div class="ol-activity">
      <span class="ol-activity-title">🏆 HASOC 2022</span>
      Co-organised the shared task, including offensive language identification in Marathi.
    </div>
  </div>

  <div class="ol-activity-cell">
    <div class="ol-activity">
      <span class="ol-activity-title">🏆 HASOC 2023</span>
      Co-organised hate speech and offensive content identification across Assamese, Bengali, Bodo, Gujarati and Sinhala.
    </div>
    <div class="ol-activity">
      <span class="ol-activity-title">🏆 OffensEval 2023</span>
      Co-organised offensive language identification in the era of large language models.
    </div>
    <div class="ol-activity">
      <span class="ol-activity-title">🎙 Responsible Machine Learning: Challenges and Way Forward?</span>
      Keynote at RANLP 2023.
    </div>
    <div class="ol-activity">
      <span class="ol-activity-title">🎙 Hate or not Hate? Beyond Binary Hate Speech Detection</span>
      Tutorial at RANLP 2023.
    </div>
  </div>

  <div class="ol-activity-cell"></div>
  <div class="ol-activity-cell"></div>

</div>
</div>
</div>

<p class="ol-note">
Each publication is shown as a separate card. Years with more work are deliberately given
more horizontal space so that progression within each theme remains visible without creating
very tall columns.
</p>

</div>
